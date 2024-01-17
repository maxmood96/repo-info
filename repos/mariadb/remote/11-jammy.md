## `mariadb:11-jammy`

```console
$ docker pull mariadb@sha256:02c68e5ce1010eccd7db21b3c8bd47d1654dd853be5fbc4fe29adf31158b9a78
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

### `mariadb:11-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:e4a9a6f3644538084d84aa6ad99a0466d34457b095d06099a99e61f3a73e886c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122622452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b54778e06a3050394a36e4dfcd153796f404397b84cb1737fd044b74c3bccbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:29202e855b2021a2d7f92800619ed5f5e8ac402e267cfbb3d29a791feb13c1ee`  
		Last Modified: Thu, 11 Jan 2024 17:48:58 GMT  
		Size: 29.5 MB (29546295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6305f82a1a5c4b2b8ebf8bcef1797efb0f65fbd5794b335a11994248e93396`  
		Last Modified: Wed, 17 Jan 2024 03:48:36 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982674206dbc53388abd0c8145c3685460759f76b12c9cad660ba76198ff407c`  
		Last Modified: Wed, 17 Jan 2024 03:48:37 GMT  
		Size: 5.6 MB (5649847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd973152fe952ad13c2695d37148e5c4fa73a64141879980a1b82a17cd985486`  
		Last Modified: Wed, 17 Jan 2024 03:48:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68ec0ab192d786deba89f058afe07873df0845b828a4884c2387cb564c4dce8`  
		Last Modified: Wed, 17 Jan 2024 03:48:36 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109f95e6f99d3eec1fda81bac0f75bb19921a5d86c71cb90005fdf9d3f911625`  
		Last Modified: Wed, 17 Jan 2024 03:48:40 GMT  
		Size: 87.4 MB (87412668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cbe76a82c5af4965f2d5bbbbafa5153443b32f93b7ea8a6f2886cb605884be`  
		Last Modified: Wed, 17 Jan 2024 03:48:37 GMT  
		Size: 3.6 KB (3615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9320d52b65039d3deaa0948de86b8bfdc9b634058c7527ec9ca5980a90570cb`  
		Last Modified: Wed, 17 Jan 2024 03:48:37 GMT  
		Size: 7.9 KB (7861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:43174692c7e4a20ee089fd0853b1b17711039b36da740ca1c947362446f95631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f82b38ab2d7aed00e24c0914fcaccb7ad1792ad0dbf931a9ea3aaef1f50c3a`

```dockerfile
```

-	Layers:
	-	`sha256:f63bd057a7d76809f1c871c25bae7952cc0b63054510d0bbff73333303792e73`  
		Last Modified: Wed, 17 Jan 2024 03:48:37 GMT  
		Size: 4.0 MB (3978817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e624bf9a7908fd89eb0eb8fc9cf3714f3be406b7b5f692b78656bad529e137`  
		Last Modified: Wed, 17 Jan 2024 03:48:36 GMT  
		Size: 31.1 KB (31114 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9f1c3fcd60ccc922d2a677df6006025306b77d5b9879a9f9c96e69bf81f1ca4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116991229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ecc79370039b3276c27029f123c0ec709d45846a95b4c23c5b0871c6fea4c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:005e2837585d0b391170fd9faf2e0c279d64ba0eb011cda8dedf28cb5839861e`  
		Last Modified: Tue, 12 Dec 2023 11:55:31 GMT  
		Size: 27.4 MB (27358237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e465b63f30111127b4c2f1a4297c9733c1c225e40ea2d3ae600e63f33832f4`  
		Last Modified: Tue, 09 Jan 2024 00:06:30 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b23153065d5051a31b841a91174e0590015049d53824f29f3316e88163dde4`  
		Last Modified: Tue, 09 Jan 2024 00:06:31 GMT  
		Size: 5.5 MB (5461267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31229f1eeda20a67714a58c055710e7c4e138cb8a3bc9be09eaeae3819fb4f`  
		Last Modified: Tue, 09 Jan 2024 00:06:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53caa7aeb6a7320d9e20ea94d89fc59bfbb829218309315480d91e9c66b09b8`  
		Last Modified: Tue, 09 Jan 2024 00:07:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c364798bab8186525ecf838e75cea57d8b96240685d3f4e592e28839612c34`  
		Last Modified: Tue, 09 Jan 2024 00:07:54 GMT  
		Size: 84.2 MB (84158074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87530ae889523be6d692e1fff9126ac5e2b4eb6f5db14779320ac63fb8c5e61e`  
		Last Modified: Tue, 09 Jan 2024 00:07:49 GMT  
		Size: 3.6 KB (3615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a291ebca907ad9384fca5ffc710ba1b590c2063c2c38d0c418af0ed1c423db`  
		Last Modified: Tue, 09 Jan 2024 00:07:50 GMT  
		Size: 7.9 KB (7861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:506955e61f772725685c5957e986a8568152d7bfef70f05cbd3bdb6e0bf21b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fed9ebe77fd7a78710c1c40938a3ed13ac02016edb8d4813be0fdbe227a912d`

```dockerfile
```

-	Layers:
	-	`sha256:1fb95f4b6587a87d7cc3a318973f33a3849ffe4cbd99efc4c28dd96458eeb1ce`  
		Last Modified: Tue, 09 Jan 2024 00:07:50 GMT  
		Size: 4.0 MB (3984058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d90563de16e20f8d80301a912c04102a9ba895786392c1e33269a9a67012b4`  
		Last Modified: Tue, 09 Jan 2024 00:07:49 GMT  
		Size: 31.0 KB (30971 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:dfecfc41706d8d58957a9670bba8947fd6454105132bd2f217455cd852d1ebe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130719719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58da00cfe7cbeac096fc020ba65fe5b2968d16f2f2b92a5e8a5477f2306dd142`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eb06c458f1bcffd534bd10415f36af10d84ad0223c7840a052931ee0238f62ee`  
		Last Modified: Thu, 11 Jan 2024 17:49:17 GMT  
		Size: 34.5 MB (34519608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bfdf8789332dce06539e3c09d832818de741f1416ec9b0ee53c4d813c167d2`  
		Last Modified: Wed, 17 Jan 2024 04:09:54 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd5103548409201bc89f22e40f9f805c84d6f64448e65c9e44124d74124f5d5`  
		Last Modified: Wed, 17 Jan 2024 04:09:55 GMT  
		Size: 6.1 MB (6082046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5be8e8412bf8f27e37aaff3f316a1cd2e751299859f08488ab018cc63db6ca`  
		Last Modified: Wed, 17 Jan 2024 04:09:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046600ef4d58e7f44a605174bffb59364fc78029d2b938070df177571fd64689`  
		Last Modified: Wed, 17 Jan 2024 08:32:44 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d985ee92f6b9fb10fae36fb5517eadc944a56302ede7654bd3ee9637f28f644`  
		Last Modified: Wed, 17 Jan 2024 08:32:47 GMT  
		Size: 90.1 MB (90104426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07409d31c9321e9e0c7c59da0cd60440d0ea63ba0802516d35ced1789e0afb36`  
		Last Modified: Wed, 17 Jan 2024 08:32:44 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fe1681f05da1c869752765e67566feac6d0d5fad3a6916c4eb5c7ce43b3924`  
		Last Modified: Wed, 17 Jan 2024 08:32:44 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:a4e8bc9eb524a663313b6b63f812ff986afe4a45b303e6e6a721169d2ada74e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4017511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f205206145ead344e716217692438af9f537ffd3435d461da930c801125583c2`

```dockerfile
```

-	Layers:
	-	`sha256:1f440883de2fe5762cd90b8b33708ab56047ea18e996e495cda6719b91a03609`  
		Last Modified: Wed, 17 Jan 2024 08:32:44 GMT  
		Size: 4.0 MB (3986488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca332b64b0a4b719161f577558c9b167844e4380dae9ee668a12ae106f940ee3`  
		Last Modified: Wed, 17 Jan 2024 08:32:44 GMT  
		Size: 31.0 KB (31023 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:d8742ae144417bb60601589ba5fbe5aa8d2e3797d0b1c5685010132367b512cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121418107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41688aa8e06165baf4a544da6f0cea0eb990ba403de8cac3d697185bb915ce1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8cf433553d1d6625c1509159e9502639154da459bba2d5aadeb708dbe9637230`  
		Last Modified: Tue, 12 Dec 2023 11:55:50 GMT  
		Size: 28.0 MB (28027192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0585c95fb8c14557239710cff2bcbe2bb41092592fe516d12f59655090a375`  
		Last Modified: Mon, 08 Jan 2024 23:10:00 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ccf50449c795b6798ec8592b12cc3c4e7cf094455d8a086aefa37d0700532d`  
		Last Modified: Mon, 08 Jan 2024 23:10:00 GMT  
		Size: 5.5 MB (5530655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07704ca35080050de0a45a34808769825631ba57e4ec6e9e7820c42845f9c5a`  
		Last Modified: Mon, 08 Jan 2024 23:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e02c7abf642703e5d706d69ca41fb8edad78771e75035d187746be0934f58be`  
		Last Modified: Tue, 09 Jan 2024 00:05:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef42a79ada28b86b0337d5632259e650f602b7a956250b8a1f51ed5c0823307e`  
		Last Modified: Tue, 09 Jan 2024 00:05:09 GMT  
		Size: 87.8 MB (87846613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acc86807e440c5acb372fe415779ddad3558c5e56f8dba99426ae4193f5b39e`  
		Last Modified: Tue, 09 Jan 2024 00:05:07 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83049a3d7f31153689dbbc0ba9f4a293d6a079cb088531ca951c1bc9d23213b`  
		Last Modified: Tue, 09 Jan 2024 00:05:07 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:6eaee9e6bc056924f0854ae5d89a8312d25363620e93d4adf66df7aa78fff7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9edd63a480bf7c3f02386a9a79d688d9e5e0892bed613637661f94477306eb14`

```dockerfile
```

-	Layers:
	-	`sha256:0d1aa214d414fbbb118b2b52ad2396eec568814b2aeec0c0b5db5a90bd38b953`  
		Last Modified: Tue, 09 Jan 2024 00:05:07 GMT  
		Size: 4.0 MB (3956306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f994656fb2e891201e3faf15f1a581cb48515f97443f8a14404e7a7227a463`  
		Last Modified: Tue, 09 Jan 2024 00:05:07 GMT  
		Size: 31.0 KB (30953 bytes)  
		MIME: application/vnd.in-toto+json
