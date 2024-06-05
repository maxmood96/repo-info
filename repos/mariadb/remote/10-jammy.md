## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:628994c8ec66a32c9375cc34611f8b11fa0acadb6cc13229934be34058adb385
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
$ docker pull mariadb@sha256:e82bf01d27cbb06a02ea6dbd4875bd448f44da0b70cf3143ae04c007d6190a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122565893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a30d8fce9cebfe4aed164e7ce4f09eb96bb2965e96ba54f8ac9233b911c3564`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sun, 19 May 2024 23:36:24 GMT
ARG RELEASE
# Sun, 19 May 2024 23:36:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 19 May 2024 23:36:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 19 May 2024 23:36:24 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 19 May 2024 23:36:24 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Sun, 19 May 2024 23:36:24 GMT
CMD ["/bin/bash"]
# Sun, 19 May 2024 23:36:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 19 May 2024 23:36:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENV LANG=C.UTF-8
# Sun, 19 May 2024 23:36:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 19 May 2024 23:36:24 GMT
ARG MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Sun, 19 May 2024 23:36:24 GMT
ENV MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Sun, 19 May 2024 23:36:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 19 May 2024 23:36:24 GMT
VOLUME [/var/lib/mysql]
# Sun, 19 May 2024 23:36:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 19 May 2024 23:36:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 May 2024 23:36:24 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 19 May 2024 23:36:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346ad58366eb0df3d6d7beef2cc236ba3176ea11f26dd1cde4f916e30740e72e`  
		Last Modified: Wed, 05 Jun 2024 02:20:35 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e7fb155c9e04abeec8967b510224acf341544e1ca861d139c791d3f23b288a`  
		Last Modified: Wed, 05 Jun 2024 02:20:35 GMT  
		Size: 5.6 MB (5647726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108599824eb0fe669e22c2c68d09b2e223c56c2c7c84038ad43d7d3c7b0f61a4`  
		Last Modified: Wed, 05 Jun 2024 02:20:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afd4e6e737a7f7845830375c4b3e8ff7d4b256002e217d10355911d668d4587`  
		Last Modified: Wed, 05 Jun 2024 02:20:35 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f60965fcfb7ce837609f1824d6b33873247e378be41477a68d648a0cb01b69`  
		Last Modified: Wed, 05 Jun 2024 02:20:37 GMT  
		Size: 87.4 MB (87370290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd7bb4afa5dc57da3f5b9a2485e354f439d4851e31d3e445a2f1cff396ea3ea`  
		Last Modified: Wed, 05 Jun 2024 02:20:36 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da10c7b00df6a1dd22266d03f29a117efa4f328c10e966d69cd4fa946b59d94`  
		Last Modified: Wed, 05 Jun 2024 02:20:36 GMT  
		Size: 8.3 KB (8339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3225977e0ad97f1e6721ad31492fbd3cbf4774605312a131e56bd64b907b7242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4582542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f2d7635011241e114cf62543ee43c7f564a9065030e10efcc0ad631ad8b0a8`

```dockerfile
```

-	Layers:
	-	`sha256:a799d029dfbed3a11f40388bb023462b70ecdc1dbd3f7dba1e09e417286540e8`  
		Last Modified: Wed, 05 Jun 2024 02:20:35 GMT  
		Size: 4.6 MB (4552164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d72013819c9400633b3f483d59618e9adaf14ac8334b09fd2eeebde29ae247b`  
		Last Modified: Wed, 05 Jun 2024 02:20:35 GMT  
		Size: 30.4 KB (30378 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:063a3c684815a2d6e85aaf94ea28072584fec0a87afecb0fe4c052b55de7aa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117008944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f508da8d76b04a5ab52067f0a4a8f766c87e0cdc7f08fec44912e8a59a69ed2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Sun, 19 May 2024 23:36:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 19 May 2024 23:36:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENV LANG=C.UTF-8
# Sun, 19 May 2024 23:36:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 19 May 2024 23:36:24 GMT
ARG MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Sun, 19 May 2024 23:36:24 GMT
ENV MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Sun, 19 May 2024 23:36:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 19 May 2024 23:36:24 GMT
VOLUME [/var/lib/mysql]
# Sun, 19 May 2024 23:36:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 19 May 2024 23:36:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 May 2024 23:36:24 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 19 May 2024 23:36:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc56fc8d32a5ec7d2a9313dafc9131783cb8fa2dab2c6e8c7f64a8421bc13776`  
		Last Modified: Fri, 24 May 2024 00:19:19 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42de1ff02ccd3e4470515a00a56c1115c368ee9fdf17a4f367b7e4dec7dcfa4`  
		Last Modified: Fri, 24 May 2024 00:19:19 GMT  
		Size: 5.5 MB (5461420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc2f8eb89fa3d54128f989955f2977af953fc5ed198e810fb3cbb64eaf887f5`  
		Last Modified: Fri, 24 May 2024 00:19:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bff9185e82b14d436ab7a7d319097664af500332ec53c45bd79b39518c6d663`  
		Last Modified: Fri, 24 May 2024 00:23:39 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90e0f4f1401577af6a25182749b31996a5ecbdf6655c3dfce42594933150c5e`  
		Last Modified: Fri, 24 May 2024 00:23:42 GMT  
		Size: 84.2 MB (84172868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5108c7d84d82be69b58661c2f4476a072f1e2eaf23f801b545ec812052b4487`  
		Last Modified: Fri, 24 May 2024 00:23:40 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0224b2ce27d0d408a66dbdc94f15c5737cf1e0008e94ff132136cc83db5d0d29`  
		Last Modified: Fri, 24 May 2024 00:23:40 GMT  
		Size: 8.3 KB (8337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:4427c6f29ef4b7f99775e4c9f49255bfce0e8986336d83d096f37063eb0368ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4590141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbcba5c85e2f8b3360f8c5f602d4437628fc3651cab999c9973dd320f6044d2`

```dockerfile
```

-	Layers:
	-	`sha256:96cf9f1c9c12dd8d8c74cf0a0df9f01ba2346d5704354718b8daeadc57c923c7`  
		Last Modified: Fri, 24 May 2024 00:23:40 GMT  
		Size: 4.6 MB (4559145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5569d1335d22bb2d5d61f47060602a085203ebfa093d2c193718650ec81b61e7`  
		Last Modified: Fri, 24 May 2024 00:23:39 GMT  
		Size: 31.0 KB (30996 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d8dbd8e2c054d2f555d0be494bde10ec3d3c096440ce556303b798115848d145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130627043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f61b31e007f5dee308a3a75eaba2e2c6aaa87b4c9d4df516afbd88c23d1f5d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Sun, 19 May 2024 23:36:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 19 May 2024 23:36:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENV LANG=C.UTF-8
# Sun, 19 May 2024 23:36:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 19 May 2024 23:36:24 GMT
ARG MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Sun, 19 May 2024 23:36:24 GMT
ENV MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Sun, 19 May 2024 23:36:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 19 May 2024 23:36:24 GMT
VOLUME [/var/lib/mysql]
# Sun, 19 May 2024 23:36:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 19 May 2024 23:36:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 May 2024 23:36:24 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 19 May 2024 23:36:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5b7cf94291ea168ccdc203965a79f54603a4fe2e0738a3acf0f7a8d860e51f32`  
		Last Modified: Sat, 27 Apr 2024 14:45:49 GMT  
		Size: 34.5 MB (34461223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45d038541689ce6b752103faee94eba9ddf7b21a0f13502f3e8df1b5ba25ab1`  
		Last Modified: Fri, 24 May 2024 00:08:27 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c126afe695ef0d4141255a17434f135b91e6d89ef2d8a141e25462cffe8ac5`  
		Last Modified: Fri, 24 May 2024 00:08:28 GMT  
		Size: 6.1 MB (6079529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1abe445e77e3543379da71cae86e37dc19e04cffe3cb548451ec1518f33824e`  
		Last Modified: Fri, 24 May 2024 00:08:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62728d95c99e6a02c3b5b3c4228f42f627eb6f35d0d53ce297df3b7c80c294f`  
		Last Modified: Fri, 24 May 2024 00:16:32 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6295803b8e3ac551b79f427409f9016282098c0a09b1e8de183121b5f8b79b0`  
		Last Modified: Fri, 24 May 2024 00:16:35 GMT  
		Size: 90.1 MB (90072162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2aed792666bb8bb941ce65a5faf707667efe5e3ae4e02d175e82a9163b3ab9`  
		Last Modified: Fri, 24 May 2024 00:16:32 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66958ce224e586ab018d418dc47bf19da25137e75e97db90b4fb584b18a631f`  
		Last Modified: Fri, 24 May 2024 00:16:32 GMT  
		Size: 8.3 KB (8336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:b9a1237e8b2b6c54d84e6b8debebba57a782b38b90136a26581ff0094b8daaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0c199fb2c6eba68173156a4a1466ad2d374a7aafd38dcef68cbf1393310dbc`

```dockerfile
```

-	Layers:
	-	`sha256:b77790b85ac5d28c2fd8a622cdc64f9d5f5d62d70beca31727e078ab85fe7de1`  
		Last Modified: Fri, 24 May 2024 00:16:32 GMT  
		Size: 4.6 MB (4560408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62fb39551ac281b19c937c33813582de4cf4d021f6b8289702da7fce33979bd0`  
		Last Modified: Fri, 24 May 2024 00:16:31 GMT  
		Size: 31.0 KB (31048 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:101266913498ee0671a18a8762c878c798d4aa2ca9c2622874bdb5c387047dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121545759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f24222792514fab7d651f9c7677f8c01daf4375e79a509679b6ce58967e913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Sat, 27 Apr 2024 13:52:56 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:52:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:52:56 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:52:58 GMT
ADD file:7d693ab3b1f45d4992a119ec94444efc96c176ad954375f3bc1299ab813a46a0 in / 
# Sat, 27 Apr 2024 13:52:58 GMT
CMD ["/bin/bash"]
# Sun, 19 May 2024 23:36:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENV GOSU_VERSION=1.17
# Sun, 19 May 2024 23:36:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENV LANG=C.UTF-8
# Sun, 19 May 2024 23:36:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 19 May 2024 23:36:24 GMT
ARG MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Sun, 19 May 2024 23:36:24 GMT
ENV MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Sun, 19 May 2024 23:36:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 19 May 2024 23:36:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 19 May 2024 23:36:24 GMT
VOLUME [/var/lib/mysql]
# Sun, 19 May 2024 23:36:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 19 May 2024 23:36:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 19 May 2024 23:36:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 May 2024 23:36:24 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 19 May 2024 23:36:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:01c7fcca5fd930108d469aeb9d86249eb7f2cdc75699dfa8dd132d9b5f55d29f`  
		Last Modified: Sat, 27 Apr 2024 14:45:56 GMT  
		Size: 28.0 MB (28000423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c57d5f8ff3fa99cbae96ee36a781742286bd3a2c79be02f63999c23225a493`  
		Last Modified: Tue, 28 May 2024 23:15:51 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b007f9f8461a2ce012bc88aa60ad8023a8a0cc2df19a284c45cb6af17f3b9d`  
		Last Modified: Tue, 28 May 2024 23:15:52 GMT  
		Size: 5.5 MB (5531752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563a77f45a0a4d9494e8437d504dcecb50694bbf49514e4c7186779867780fbb`  
		Last Modified: Tue, 28 May 2024 23:15:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7457d4583cd14777ddeb2c5eacf51c2eac7a778acfa4b08b06e672eaeec7cd3`  
		Last Modified: Wed, 29 May 2024 00:37:02 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1898678278e6d6134ceeea15521a8dd5f0376deda253c9d5f84e4fa3a73893`  
		Last Modified: Wed, 29 May 2024 00:37:05 GMT  
		Size: 88.0 MB (87999449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee80c46ab5aa61d3e042ebe2ce0380dce73f0e007ad891de936bd8110a3aaad9`  
		Last Modified: Wed, 29 May 2024 00:37:02 GMT  
		Size: 3.6 KB (3617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f19fd03fc8c80a41c834a8733688538bad382b34c7f4e112d1166a74f10cef`  
		Last Modified: Wed, 29 May 2024 00:37:02 GMT  
		Size: 8.3 KB (8344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:7633d532ffd3de81e74a71f250b70e1627ad13c390408b703b08c3a887aa6734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4584071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2db351cfae1306df3e70c6fab673d8d099a0733537571e83c99b90435067028`

```dockerfile
```

-	Layers:
	-	`sha256:66947590e95718b676fe988706ee3bdceb263c3adab1179898f3644743b68ec8`  
		Last Modified: Wed, 29 May 2024 00:37:02 GMT  
		Size: 4.6 MB (4553093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff22d7bd81216a388aa4bc95ff0d797ba9ebb929a95cb41377feadf63548f8d0`  
		Last Modified: Wed, 29 May 2024 00:37:02 GMT  
		Size: 31.0 KB (30978 bytes)  
		MIME: application/vnd.in-toto+json
