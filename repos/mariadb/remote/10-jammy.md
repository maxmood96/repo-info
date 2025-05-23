## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:e725b24af143c6b30e78eab99441e4cabac7494a69186effc2f506ea85401e2a
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

### `mariadb:10-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:28f18938626ab619743177bb506dfb49d8774dc018cf5029cab51575101f951d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105286857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f35fb53850edf00d0795c57c0dd43e828eab2b86dd97550bc498fa72f092f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 23:31:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 May 2025 23:31:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV LANG=C.UTF-8
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.13 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 21 May 2025 23:31:53 GMT
ARG MARIADB_VERSION=1:10.11.13+maria~ubu2204
# Wed, 21 May 2025 23:31:53 GMT
ENV MARIADB_VERSION=1:10.11.13+maria~ubu2204
# Wed, 21 May 2025 23:31:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.13+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.13+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 21 May 2025 23:31:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 May 2025 23:31:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 21 May 2025 23:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 23:31:53 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 21 May 2025 23:31:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e033e8731614743de4b2953315891d7c95bb67836be9d3b112fb4d588b1a3b4`  
		Last Modified: Thu, 22 May 2025 22:09:12 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d63e3aa9cd66ce946b1eaa9fb6c3887aceb665cbf4d36acb15b52ccf3e431`  
		Last Modified: Thu, 22 May 2025 22:09:12 GMT  
		Size: 5.7 MB (5659714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b20e9ac537098d4a231e8901a4e3ca6b8c725fc84015c6ab1567354fda9a6`  
		Last Modified: Thu, 22 May 2025 22:09:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552cd46b3c5840c4b120a5b18b40dd840df5e8b88e4b991e7c50f4b8658640ed`  
		Last Modified: Thu, 22 May 2025 22:09:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d54c7d9f776483565e4e181b8e73a6817954d9b5ed9f02a741db1688318f7da`  
		Last Modified: Thu, 22 May 2025 22:09:14 GMT  
		Size: 70.1 MB (70079966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2338c117b7c33f8f78654c58a6038ea9e90632ae6cf858fba169dbd6f423d5`  
		Last Modified: Thu, 22 May 2025 22:09:13 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11887dc0ca84eb6e68afd9876bc2d78b4dee4fbe3a8d67215a145aa78b26dcea`  
		Last Modified: Thu, 22 May 2025 22:09:13 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:60edb15bf1a7e320b472f55d6878c3aa39126ff4d63a99e0c7f6558116335956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85b8a4054b12a920c0fb547888374ef1109ebc8c4cba161b74a12244c40c70b`

```dockerfile
```

-	Layers:
	-	`sha256:3bf282c381c1ea5e8a4e624420e7ab7a0bdf65d7954d3e3edabc5b5bbeaf983d`  
		Last Modified: Thu, 22 May 2025 22:09:12 GMT  
		Size: 4.6 MB (4636563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1e9c44e6fecafc6f53cb0c21b6b87547b514639cb2198d5b57c9b4e84177da`  
		Last Modified: Thu, 22 May 2025 22:09:12 GMT  
		Size: 30.7 KB (30693 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:eddd39b9fe4296f7a10cdec055c7a34bc52966ea55368c7ac9b402891f9aa072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99674359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26723762aff9e9065561f6302b07b500b7b443289199c49239c42fd19e8dc0b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 23:31:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 May 2025 23:31:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV LANG=C.UTF-8
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.13 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 21 May 2025 23:31:53 GMT
ARG MARIADB_VERSION=1:10.11.13+maria~ubu2204
# Wed, 21 May 2025 23:31:53 GMT
ENV MARIADB_VERSION=1:10.11.13+maria~ubu2204
# Wed, 21 May 2025 23:31:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.13+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.13+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 21 May 2025 23:31:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 May 2025 23:31:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 21 May 2025 23:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 23:31:53 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 21 May 2025 23:31:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfaf7d814b60140b775621bde30aef385b80d91fbd720ecfa9c424c64fc27da`  
		Last Modified: Mon, 05 May 2025 17:42:18 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a05aa8a482986f9af49f0eb72173c507b7a231a2d3627573e5ddb090e5a928`  
		Last Modified: Mon, 05 May 2025 17:42:19 GMT  
		Size: 5.5 MB (5472230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c2dbf00137f847468e0d4988a9336c9cb46d0288f1b2c79d7a9c09701eddf2`  
		Last Modified: Mon, 05 May 2025 17:42:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0243677197e2a4b444b2d4bf3e08746b01b92e27590fdf5f3f831dc37acb16b8`  
		Last Modified: Fri, 23 May 2025 01:04:45 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abca37f92cc8a5ae3fe3d054c809ebab0bced7c94e3a6a40ad4f3ffd164e5e9a`  
		Last Modified: Fri, 23 May 2025 01:04:48 GMT  
		Size: 66.8 MB (66833339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733ef23005fec8bc1e614055e66813f8b7d079e61b7c1bfe9e1be92e2e0ce5f1`  
		Last Modified: Fri, 23 May 2025 01:04:45 GMT  
		Size: 4.0 KB (4025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6315f8e4c0502ed902b37bbcc741730a8a6c3d29932fa61ef04950a2bfe02139`  
		Last Modified: Fri, 23 May 2025 01:04:45 GMT  
		Size: 8.4 KB (8371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:769f1cefbae70ba8aa77ea29d22bfba5b7854c6a0c9ad418ed781a63945c5984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4673879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d13d60d384cdad9ab083aa790ee3475d7c5e0afccef06db9140060652fe76b`

```dockerfile
```

-	Layers:
	-	`sha256:8b05019d0e79d0b8a09972dd8a6e772c0691bb429eaa5f4004bef426403fb742`  
		Last Modified: Fri, 23 May 2025 01:04:46 GMT  
		Size: 4.6 MB (4642998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972ac10f96b95aaaac7d6d32126def61d5f3067caccde0c5912d0e36f53f2573`  
		Last Modified: Fri, 23 May 2025 01:04:45 GMT  
		Size: 30.9 KB (30881 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e160e0baa8ab0e5db1ac3b1d186052228b32fe0e9963f13f081ecf11544bbb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112908585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4c45e25333cce5b1d0a2da5eea9111110abba3c815b53c48a971a8c94d5611`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:54 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:58 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Mon, 28 Apr 2025 09:45:59 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 23:31:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 May 2025 23:31:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV LANG=C.UTF-8
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.13 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 21 May 2025 23:31:53 GMT
ARG MARIADB_VERSION=1:10.11.13+maria~ubu2204
# Wed, 21 May 2025 23:31:53 GMT
ENV MARIADB_VERSION=1:10.11.13+maria~ubu2204
# Wed, 21 May 2025 23:31:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.13+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.13+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 21 May 2025 23:31:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 May 2025 23:31:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 21 May 2025 23:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 23:31:53 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 21 May 2025 23:31:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9452541bb73f90ecc9aeebb28979dfbb5d8064364e1e1dc171ad56bd429458f`  
		Last Modified: Mon, 05 May 2025 17:33:27 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3dc855d9524fcfad795d694887132809b5234fdcb1b2ac154cdf6681682aad`  
		Last Modified: Mon, 05 May 2025 17:33:27 GMT  
		Size: 6.1 MB (6086284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1496641202d761b6e273cd93f5ce181dcb7f19a0d252b8ed80db240f64a058`  
		Last Modified: Mon, 05 May 2025 17:33:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7908dce19149d6b293e51835c6f00dfae8fbdf2f18646aa599515a624a87f84`  
		Last Modified: Fri, 23 May 2025 02:05:45 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a455984a3e6cc80873bdf99fd8d8b2d2f7959d8e615ecb670ed1681fd771ab6b`  
		Last Modified: Fri, 23 May 2025 02:05:47 GMT  
		Size: 72.4 MB (72364510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ac1e393ff9e8703a61b75c2febe438c0f70f724afd8e28fffb083f55282b5`  
		Last Modified: Fri, 23 May 2025 02:05:45 GMT  
		Size: 4.0 KB (4022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0e02d28e8ed8bb7a4d096dc8615e537381577739ee018a02697720cd3e7abd`  
		Last Modified: Fri, 23 May 2025 02:05:45 GMT  
		Size: 8.4 KB (8369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:4a90e9c8893c72bc0047b464558bdd6170390c5d84388067b207f0bd8e7908ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4675105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5c453501bd036f1dc77b9c6741ca45bb85e73232a8168724387e6c2b2e7605`

```dockerfile
```

-	Layers:
	-	`sha256:65c2bb71c6cda15bd084e81c557095626a942c642a51dc914dc890fcea4e4c28`  
		Last Modified: Fri, 23 May 2025 02:05:45 GMT  
		Size: 4.6 MB (4644348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c41680b70561d7324d853b73ed38bbcde44e942e17dbe790c45d803f61f7d06`  
		Last Modified: Fri, 23 May 2025 02:05:45 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:1ec195dd82c65eea94969cb75589eff213072ce0e7b6ab090df0938fbf3a99b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103108650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a82bdf89fa3616b90411bc915581c5b2c1ae4cd2bb40cb03a7252009b6dad7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 28 Apr 2025 09:45:02 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:45:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:45:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:45:04 GMT
ADD file:4be5dde78df6dfb2332aa60bf4714ecf19075f664a5fac89ff50019cbee5434d in / 
# Mon, 28 Apr 2025 09:45:04 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 23:31:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 May 2025 23:31:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV LANG=C.UTF-8
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.13 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 21 May 2025 23:31:53 GMT
ARG MARIADB_VERSION=1:10.11.13+maria~ubu2204
# Wed, 21 May 2025 23:31:53 GMT
ENV MARIADB_VERSION=1:10.11.13+maria~ubu2204
# Wed, 21 May 2025 23:31:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.13+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.13+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.13/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 21 May 2025 23:31:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 May 2025 23:31:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 21 May 2025 23:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 23:31:53 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 21 May 2025 23:31:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:64d717faaf8dba48ef4989d39eb6faef5fe680871a4064f1753d9cc21de5bc3c`  
		Last Modified: Mon, 28 Apr 2025 10:44:16 GMT  
		Size: 28.0 MB (27999984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2154582f3a970f1371c33afe44832f14767d365c5e0f5fec7887b7c778b7887`  
		Last Modified: Mon, 05 May 2025 17:28:36 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a9e489602f07b0306d8805f0d7dd0499308991b54b368317a211ff0e1ed0ae`  
		Last Modified: Mon, 05 May 2025 17:28:36 GMT  
		Size: 5.5 MB (5541416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5ae98e2974d3966fcc550d58098e24f984ea8c21a97f889b5c2e4ab7daddc7`  
		Last Modified: Mon, 05 May 2025 17:28:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef17b46558c8028553e53e087d30b0293317885d1d3c5c178c29e2e079a56ce2`  
		Last Modified: Thu, 22 May 2025 22:13:15 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b230a520b7ab75ca935e28538a812824afd508da0caa4eece0f13f5239d9e896`  
		Last Modified: Thu, 22 May 2025 22:13:16 GMT  
		Size: 69.6 MB (69552678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2261a8138ffd59553f2c6ff4cb87e95fb0a6005d0a70eff29c0c7416abd0ec1f`  
		Last Modified: Thu, 22 May 2025 22:13:15 GMT  
		Size: 4.0 KB (4022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc262b4bdca1800aca7d2256b4acf3c4d097f3969afe222d0451e0f31952b271`  
		Last Modified: Thu, 22 May 2025 22:13:15 GMT  
		Size: 8.4 KB (8370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:768f10a704962ad1f38b9471f061e9baa7295c9985313d29f4e5704971572adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4667582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ec4a4bd2cf8d7e39de923e9cc295a7283cd668dac8fdde1f320ced47cafa0e`

```dockerfile
```

-	Layers:
	-	`sha256:b98aa937aed681e5708bd204df1f9564792b2bfd318c8fc4d75046eec75b0ec0`  
		Last Modified: Thu, 22 May 2025 22:13:15 GMT  
		Size: 4.6 MB (4636889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:740d03a53fe11eed624c53b224a5db67211895828a203e653eb959d430b0a115`  
		Last Modified: Thu, 22 May 2025 22:13:15 GMT  
		Size: 30.7 KB (30693 bytes)  
		MIME: application/vnd.in-toto+json
