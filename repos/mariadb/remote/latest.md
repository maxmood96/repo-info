## `mariadb:latest`

```console
$ docker pull mariadb@sha256:e487701b1f7e3f47319fe005b417c72becb67824a58b7bd35c6505f070f66dcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:310425c03b97479ea6083df11ca8a338a763ad4626db79ca39447b9dfc631ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109060325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028510775a1c518c8c28a2bf76ef13d604e523ce60ef4d25c3ae2696baa751da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:52:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 09 Feb 2026 19:52:56 GMT
ENV GOSU_VERSION=1.19
# Mon, 09 Feb 2026 19:52:56 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 09 Feb 2026 19:52:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Feb 2026 19:52:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:52:57 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:52:57 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.1.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 09 Feb 2026 19:52:57 GMT
ARG MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Mon, 09 Feb 2026 19:52:57 GMT
ENV MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Mon, 09 Feb 2026 19:52:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
# Mon, 09 Feb 2026 19:54:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 09 Feb 2026 19:54:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 09 Feb 2026 19:54:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Feb 2026 19:54:40 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 09 Feb 2026 19:54:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Feb 2026 19:54:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Feb 2026 19:54:40 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 09 Feb 2026 19:54:40 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b146327c8ae4570fe069ac9fd48bf5953df98a13fcac91ecc219d0421775b6da`  
		Last Modified: Mon, 09 Feb 2026 19:53:25 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eaf77e35d67e140009b64a67f012bb9959c32a1b6cfeb8c35bd881740b669f8`  
		Last Modified: Mon, 09 Feb 2026 19:53:25 GMT  
		Size: 7.7 MB (7698686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7b8e9223281e8472d865c96b86fbfed01c931c0e6a43ca9e47e6123c88d83a`  
		Last Modified: Mon, 09 Feb 2026 19:53:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aab4ad906bd5ad8939a0ccfd72ce05efbef70cabdd99528939604b2bdce29fc`  
		Last Modified: Mon, 09 Feb 2026 19:54:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6acba72e6aa27945b8be40707bdb543a8c3af7e4a96c75811b004afa4442e232`  
		Last Modified: Mon, 09 Feb 2026 19:54:56 GMT  
		Size: 71.6 MB (71621406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff90423f32ec065d64bdf7e5644339b19a818dd857d05c2ea142754b62f3d8`  
		Last Modified: Mon, 09 Feb 2026 19:54:53 GMT  
		Size: 4.0 KB (4034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afdd019f892e23601faec5ab891f701f1d8312854bec0620009ae8332b8ba16`  
		Last Modified: Mon, 09 Feb 2026 19:54:53 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:latest` - unknown; unknown

```console
$ docker pull mariadb@sha256:3bf36076d35b5d8a683207c2d31a84c90b27e0d6d08653574d50b322c16e927a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a59074fc03a7c169012c3c9c6a6d5f4e1bd82c78537806cb610be9aa0f50ad7`

```dockerfile
```

-	Layers:
	-	`sha256:bf282c6e4df9061e17e25bf1d53ee25b5eebd535e1ac5576e60b062e1698ec0e`  
		Last Modified: Mon, 09 Feb 2026 19:54:53 GMT  
		Size: 4.3 MB (4273707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc5a4b5a981620fbf7661646c2cf187a0deace76d3f64c0010df0c2c8989eac8`  
		Last Modified: Mon, 09 Feb 2026 19:54:53 GMT  
		Size: 31.4 KB (31441 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:21407e376f311cca4266d9aa94ddedcf5023fd082bc836e3710e8deff9f311c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106790287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8db11dde569bad81702e5d8f73926fd88d37c773c1b205eda2167d16cb31279`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:53:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 09 Feb 2026 19:53:52 GMT
ENV GOSU_VERSION=1.19
# Mon, 09 Feb 2026 19:53:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 09 Feb 2026 19:53:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Feb 2026 19:53:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:53:52 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:53:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.1.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 09 Feb 2026 19:53:52 GMT
ARG MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Mon, 09 Feb 2026 19:53:52 GMT
ENV MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Mon, 09 Feb 2026 19:53:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
# Mon, 09 Feb 2026 19:53:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 09 Feb 2026 19:54:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 09 Feb 2026 19:54:08 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Feb 2026 19:54:08 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 09 Feb 2026 19:54:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Feb 2026 19:54:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Feb 2026 19:54:08 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 09 Feb 2026 19:54:08 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f658b882277fda1f52f15bbcd2d8ced6deae92876ae201de84b5ce7a2c66d129`  
		Last Modified: Mon, 09 Feb 2026 19:54:23 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11df06d4fc7621d97b7ae0e5c31fe333059f074fbc3b31d203ced36a862366e0`  
		Last Modified: Mon, 09 Feb 2026 19:54:24 GMT  
		Size: 7.3 MB (7320109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea28f681874e428f9a88053fd2d94f3775588406609b335f72b5f32e08d57dfe`  
		Last Modified: Mon, 09 Feb 2026 19:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0879e24e0bb182f4196697d87225bbebf88f1de3d8fb39a43109d5cddd58d08`  
		Last Modified: Mon, 09 Feb 2026 19:54:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effa868b967599a05dbe1e95c2d4309831e79abb286f2f4eda02aa4132de14df`  
		Last Modified: Mon, 09 Feb 2026 19:54:26 GMT  
		Size: 70.6 MB (70592129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4946e0bdfebde0d1b832b3e432548b7a3367193b31ccdb9786019abde8b48598`  
		Last Modified: Mon, 09 Feb 2026 19:54:25 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1669c33b0c2a3119cd7aa190b81c4529423d834a6fa083db70feb36980b3ddd`  
		Last Modified: Mon, 09 Feb 2026 19:54:25 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:latest` - unknown; unknown

```console
$ docker pull mariadb@sha256:e3c07f4f6fbcf97d11f995376d49de3df4cb02d9e39d7b2c493714c5da18c481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5570de89e9671a55c31901e1edbd813e3df2888a6c9550383721f167808089c1`

```dockerfile
```

-	Layers:
	-	`sha256:894b510af2960715395f3b96e812a66d0d9918fcde653c69652c6058b48e527e`  
		Last Modified: Mon, 09 Feb 2026 19:54:23 GMT  
		Size: 4.3 MB (4280984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:507c05d53a392672d0a3db80611611c0566e4a33b64752e849e33bb2e8e3d304`  
		Last Modified: Mon, 09 Feb 2026 19:54:23 GMT  
		Size: 31.7 KB (31653 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d1ab2ea5723841f7c1408a23fad88d6d3394fa4f7cdbcfb79a455a57cb8b8342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119494524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a71e077302925ea22d1587ae5f5330869a922c19165f4820e70727e00488a28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:50:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 09 Feb 2026 19:51:34 GMT
ENV GOSU_VERSION=1.19
# Mon, 09 Feb 2026 19:51:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 09 Feb 2026 19:51:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Feb 2026 19:51:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:51:34 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.1.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 09 Feb 2026 19:51:34 GMT
ARG MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Mon, 09 Feb 2026 19:51:34 GMT
ENV MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Mon, 09 Feb 2026 19:51:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
# Mon, 09 Feb 2026 19:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 09 Feb 2026 19:53:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 09 Feb 2026 19:53:49 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Feb 2026 19:53:50 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 09 Feb 2026 19:53:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Feb 2026 19:53:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Feb 2026 19:53:50 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 09 Feb 2026 19:53:50 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e465cb9a54e1e7699159cc33f01a03882245807f55f18ef53cb719757bc6f11c`  
		Last Modified: Mon, 09 Feb 2026 19:52:55 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0c19b57c8161c92150c3193ab496e7d0029f9c7550577de5be2066c20156a0`  
		Last Modified: Mon, 09 Feb 2026 19:52:55 GMT  
		Size: 8.6 MB (8557165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12e091f8859edd88af66534d86dad7b363f844be6b775788238df5e3121729f`  
		Last Modified: Mon, 09 Feb 2026 19:52:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f79354b4700fe7373cda0eb8cfa4447dc8c388f37bfbc387589d020321c4f13`  
		Last Modified: Mon, 09 Feb 2026 19:54:30 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eeb0019d5d02bf9efd9520679b705549075f61a114f0086bf15877f0e7e1857`  
		Last Modified: Mon, 09 Feb 2026 19:54:32 GMT  
		Size: 76.6 MB (76616974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18f5d14dd49d9f313e1327ced1531ab33a9c63736bca5a8923d8d26e41a3c35`  
		Last Modified: Mon, 09 Feb 2026 19:54:31 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5741fd374b78dc714fdd0b09ab3c9dc0f2c4d53c9a9fb156d2bc9c215583fa18`  
		Last Modified: Mon, 09 Feb 2026 19:54:30 GMT  
		Size: 8.4 KB (8396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:latest` - unknown; unknown

```console
$ docker pull mariadb@sha256:8dce27e2a3ab2cc6e60807a3b8fc9d8b2347ba8f19b633b7d6899fec6b0acabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcd89fb21d8dd4795b8f6a52603746be16a8866ad86c15a9d224060ec2cd76d`

```dockerfile
```

-	Layers:
	-	`sha256:4c7d851e3a14a76a31c02c3781b89fad6b66ac62236fba60a2958e357d0243d0`  
		Last Modified: Mon, 09 Feb 2026 19:54:30 GMT  
		Size: 4.3 MB (4281642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4daa1a400e3c620a7c847efc302cec8ca6da0f820a968534d017cd424aea1f12`  
		Last Modified: Mon, 09 Feb 2026 19:54:30 GMT  
		Size: 31.5 KB (31517 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:55828459dd6e730891b4894b33ab8c6fbca587e96057045f88e2c85645b17290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114153844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53744861085c6e291a57f512d02d0615a6e1282b33a050d78bdd8522f3dcf26f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:50:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 09 Feb 2026 19:51:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 09 Feb 2026 19:51:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 09 Feb 2026 19:51:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Feb 2026 19:51:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:51:03 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:51:03 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.1.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 09 Feb 2026 19:51:03 GMT
ARG MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Mon, 09 Feb 2026 19:51:03 GMT
ENV MARIADB_VERSION=1:12.1.2+maria~ubu2404
# Mon, 09 Feb 2026 19:51:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
# Mon, 09 Feb 2026 19:51:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 09 Feb 2026 19:51:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.1.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.1.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 09 Feb 2026 19:51:20 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Feb 2026 19:51:20 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 09 Feb 2026 19:51:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Feb 2026 19:51:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Feb 2026 19:51:20 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 09 Feb 2026 19:51:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 06:36:13 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b998bb69c1a7641e4ec25bb345dc1875dc73ddfad6856c0ea3cf9df3de93a17`  
		Last Modified: Mon, 09 Feb 2026 19:51:45 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e882de07c6fc1297000f60bfe57f38c999227649beedca424a6ba0a00b80f80b`  
		Last Modified: Mon, 09 Feb 2026 19:51:46 GMT  
		Size: 7.5 MB (7540797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43afedd33730718eb80827ffc771cf8ba954d9caca622928639464779a4f2d8`  
		Last Modified: Mon, 09 Feb 2026 19:51:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb33ed1e3fd1a4f09309be37316613d7dd98637f36cd3d08ebb31c0a1117dba`  
		Last Modified: Mon, 09 Feb 2026 19:51:45 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2925cdf5626afc52c2a7e50c1c6b3a313e09a34c82eb085a5563abb021066c`  
		Last Modified: Mon, 09 Feb 2026 19:51:47 GMT  
		Size: 76.7 MB (76689623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4086b35b0c2ca84ee0f663e7fb92e7ea698060f05b08a7c8b816aff405bcc1fc`  
		Last Modified: Mon, 09 Feb 2026 19:51:46 GMT  
		Size: 4.0 KB (4033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5fb252586b90103c246d01cf94508872eff3e702fd19d499060cb890a5a1f1`  
		Last Modified: Mon, 09 Feb 2026 19:51:46 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:latest` - unknown; unknown

```console
$ docker pull mariadb@sha256:035db8957e9386f60c894c60d89b79603750523a52e4fa84bdb3ff414c880def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2013f2b29f33799221386e5b7e912d4888be6a6ecc46525ebf0fad18921be1`

```dockerfile
```

-	Layers:
	-	`sha256:b5bf2c3bbcbc8b012268836dd4e61e74f8d0bc162c57355ae4b3a6625810fb56`  
		Last Modified: Mon, 09 Feb 2026 19:51:45 GMT  
		Size: 4.3 MB (4275426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320f927f9e9405b18b5d3ba41b47456fb46b10f1e489b6cbdf8d361bdd8ac203`  
		Last Modified: Mon, 09 Feb 2026 19:51:45 GMT  
		Size: 31.4 KB (31441 bytes)  
		MIME: application/vnd.in-toto+json
