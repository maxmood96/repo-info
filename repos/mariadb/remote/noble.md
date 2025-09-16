## `mariadb:noble`

```console
$ docker pull mariadb@sha256:8a061ef9813cf960f94a262930a32b190c3fbe5c8d3ab58456ef1df4b90fd5dc
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

### `mariadb:noble` - linux; amd64

```console
$ docker pull mariadb@sha256:1c44d063b05eec0c35a9bc35ff2ac6a489b29305e4f6ae095ec9dbf46938f14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105535217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccf43d36f1dd3e4a345d7d9844067f85b095098812b9ac2199ebc41df7be4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 08:15:27 GMT
ARG RELEASE
# Fri, 08 Aug 2025 08:15:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 08:15:27 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf2e947a240b04cc89f2963acb60fc8638614bbe20bd8a1cdf0f31a2ad0f547`  
		Last Modified: Mon, 15 Sep 2025 22:21:40 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cbc8a9ec6be2cbe66edf112dd4556daf28d94de08b3d4bd59410d37a607808`  
		Last Modified: Mon, 15 Sep 2025 22:21:42 GMT  
		Size: 5.3 MB (5349861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c69925a3f99cca11333fc11b3beff81f7add2e1d78ddea5711d21b240d69302`  
		Last Modified: Mon, 15 Sep 2025 22:21:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb61de4991e7b42324e332616ec59f20f990212b6ee5f56887dafa860e2a20a`  
		Last Modified: Mon, 15 Sep 2025 22:21:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ac881f9b787ba9fc30b9136e739402bc82622f0dcebf5475e9cfd3348a517`  
		Last Modified: Mon, 15 Sep 2025 22:21:45 GMT  
		Size: 70.4 MB (70447700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52364fc3563c9f1472bca43dca932fee178a75f25aefa4caefd93de7c3dd1918`  
		Last Modified: Mon, 15 Sep 2025 22:21:42 GMT  
		Size: 4.0 KB (4032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1051e818021c8e718bc2313c6e80a4afbf5ae11b2695a9974d9d6c0ea4f826`  
		Last Modified: Mon, 15 Sep 2025 22:21:42 GMT  
		Size: 8.4 KB (8394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:56ad9f003969c5beb222fba1e3f3f8f6b519bd79425c8c051a01d46338697d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea13996445087eef0c71da4778b7eee6c267f5ffea78df099c86bc0419d4d8a`

```dockerfile
```

-	Layers:
	-	`sha256:e7b081104599feb4ce313dab049cdd97a2228ddb68cffd408b4689ce65fd86b7`  
		Last Modified: Tue, 16 Sep 2025 00:36:46 GMT  
		Size: 4.3 MB (4263647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c06cd656130bdcc56a61df9d9e5e5a4414080b1205d3c6cc31fc13da5cf572`  
		Last Modified: Tue, 16 Sep 2025 00:36:47 GMT  
		Size: 31.2 KB (31212 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c25bda6f70d9cfb3f4ccbdd8ed89f1f0a8d7f233c9dd0deb7591be2ce178ceac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103468732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51178528bdb7a3d537e254bfa7e4eb10b36e9e899ccf0cea0077d41c934386ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 08:15:27 GMT
ARG RELEASE
# Fri, 08 Aug 2025 08:15:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 08:15:27 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0115ed7fe7459d70b554a13395aaba1b247a4460e9ceaed0b27a6269d0b5819f`  
		Last Modified: Mon, 15 Sep 2025 22:20:35 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc479ffc7fdec88fc689199dfae6112a8226af2926fab0cbeabaa7b6c6c9b621`  
		Last Modified: Mon, 15 Sep 2025 22:20:35 GMT  
		Size: 5.1 MB (5130885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ed21e071a448e63b9e2b3404d3fbd72502bf65dd7c017fd1d2ad1e2f7dc6e9`  
		Last Modified: Mon, 15 Sep 2025 22:20:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed6ff4de1cd7ba8842fac677b5521a477216408f9e0d203f313f1f34c81c7af`  
		Last Modified: Mon, 15 Sep 2025 22:20:35 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a514bd98772da05ede68791deff998f5040e66540471c0a513f7080c4b42af4`  
		Last Modified: Mon, 15 Sep 2025 22:20:40 GMT  
		Size: 69.5 MB (69462310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba70be8eb856c3489d4b2d4f4e0f5f39621e37dc7b390af6cac761069c81be75`  
		Last Modified: Mon, 15 Sep 2025 22:20:34 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ce498e87970c74e9d6ec4d8166643b1bdc17638cbe484a7d1f5feb7d8fd8d2`  
		Last Modified: Mon, 15 Sep 2025 22:20:34 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:e15beea4c9f04dff06e54ccac050c87790a263925bfc075be2b0e136f5b83119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa74388d53606a43619193b7d20d435c5c10ee6333e51a18008a35318bed6850`

```dockerfile
```

-	Layers:
	-	`sha256:97184b6fc659fad84245a6ee6c1200abf303c2bc35836b3d74093686439ff565`  
		Last Modified: Tue, 16 Sep 2025 00:36:52 GMT  
		Size: 4.3 MB (4270922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b016aeb961d59b993759911c1bae336cf93c90a70c31083d5e53ce8768cc753b`  
		Last Modified: Tue, 16 Sep 2025 00:36:53 GMT  
		Size: 31.4 KB (31423 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3cb679b9acb40f68b7cb230e15191a83d5f5adf35065f4a06abb0218742f057d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115671850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fcf4b3753bdb63c15348fa7955844f2b05bf0335fbbcb4e302bb94d1a525db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 08:15:27 GMT
ARG RELEASE
# Fri, 08 Aug 2025 08:15:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 08:15:27 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8505483604766aa1fb0de489c3be4a1d33f81f8ef9444e024739edd2da8c0407`  
		Last Modified: Mon, 15 Sep 2025 22:54:30 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e145d9e2007363bb9492c49e0357a1681402d8d48a2b9be860786f8e5ce62b98`  
		Last Modified: Mon, 15 Sep 2025 22:54:31 GMT  
		Size: 5.9 MB (5914364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a85231ca838eb2a2dc3db3fc75fb92fc010df4d70a72cc21d99b95e19787ff`  
		Last Modified: Mon, 15 Sep 2025 22:54:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e199fa80e06755598c77965ad55f85a1795c731c0f78fac1fb15b028b8a695b`  
		Last Modified: Mon, 15 Sep 2025 22:55:35 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038f5c33a9ca1439cfb9da4687470295260ddd2ff36293745a3782fb903b4a1f`  
		Last Modified: Mon, 15 Sep 2025 22:55:42 GMT  
		Size: 75.4 MB (75440134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acae1add26d470249c5e9110e8a0f2421807566ed11baa966e7ac03b6e16d4b8`  
		Last Modified: Mon, 15 Sep 2025 22:55:36 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4dcb5002212f7b80892918079296d2f8aa8af0e5a8b53b737bf18f1e114ca4`  
		Last Modified: Mon, 15 Sep 2025 22:55:36 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:376947101abf73f123c6505ae4409e4cd4a2482c4571da0702e21311e9dfa7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1489869c9d2f379c68c8b43b9e9c43c879207cedf143324fcf3f6f89367be05d`

```dockerfile
```

-	Layers:
	-	`sha256:eb0dbcc04b191a75b3929057454ea2bed0d3ea192c96c8d571cd83acf75e8c5b`  
		Last Modified: Tue, 16 Sep 2025 00:36:57 GMT  
		Size: 4.3 MB (4271568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:733b39d0e8684b23ecac1aac04f121dd171d5060409f248907e0b67e12659f1e`  
		Last Modified: Tue, 16 Sep 2025 00:36:58 GMT  
		Size: 31.3 KB (31288 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; s390x

```console
$ docker pull mariadb@sha256:ff4915bb21e62d02630f15cf29b246b11e52353c41725cfc8bb22a81d59541bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110916943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799aa465be0e543e8900a4b070a8afa6fe167b9b4950aeeed75481eaafbee65c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 08:15:27 GMT
ARG RELEASE
# Fri, 08 Aug 2025 08:15:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 08:15:27 GMT
ADD file:c24f61277b8ba0fc6a9f5e3c821b272fa1878e300fa010e5e8c6bb6b789470a0 in / 
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:1d6a499251c4e5e59ef209845254eb72c5efde9542271f270cf1a08fa823dfda`  
		Last Modified: Wed, 10 Sep 2025 16:24:53 GMT  
		Size: 29.9 MB (29906591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed6bc89de27b57059612588ba3efaac3d194c1fbc79eee021bb6277e45b0e6`  
		Last Modified: Mon, 15 Sep 2025 23:00:35 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226a8f538d3b54cfbea655ef0a25b972fba56e050aac0d58c27de213db54dd04`  
		Last Modified: Mon, 15 Sep 2025 23:00:36 GMT  
		Size: 5.5 MB (5483565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fad414b5868ea9911c24b3df887ea453b253b8919e581e66e299e1c77ab92a`  
		Last Modified: Mon, 15 Sep 2025 23:00:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b385168a933b08298ac3b6f202a9aff56de13213350da3d814a42c9d747dae`  
		Last Modified: Mon, 15 Sep 2025 23:02:01 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3958a0e53f1e93e0ff6cacd1978c271c4ed85834c531dcfa20dc5bd3de6e7b1a`  
		Last Modified: Mon, 15 Sep 2025 23:02:06 GMT  
		Size: 75.5 MB (75512558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58c13e68a9bae14712fee0c02d093e2965380f29e2ed536896284eabfcdead9`  
		Last Modified: Mon, 15 Sep 2025 23:02:02 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0202fa26fa6a0191a73856b49072e6e013427556ddcc760b1859a2a1c4cbe0ea`  
		Last Modified: Mon, 15 Sep 2025 23:02:02 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:3e074949bf93628644cee75f35f07c4e7549c082fc7d337cb86f0fe44cbb2aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939dd8c3186a5e57daf17de5685c0f2dc2ac58e3adebde8b803b8c2c35b1c304`

```dockerfile
```

-	Layers:
	-	`sha256:dfac76158b60fcd4c388f3931e276c45e4467b8f3ee7d727486da7e3e38df7e2`  
		Last Modified: Tue, 16 Sep 2025 00:37:02 GMT  
		Size: 4.3 MB (4265368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b2f85bec9c581574a8564c381f5fdc62cb79574699d6d5a7ef6d421f2baa6f`  
		Last Modified: Tue, 16 Sep 2025 00:37:03 GMT  
		Size: 31.2 KB (31212 bytes)  
		MIME: application/vnd.in-toto+json
