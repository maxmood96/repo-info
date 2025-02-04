## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:e0bbb7578a9fda2882de199f51344ce00f4cc306fc45810648fe009f63c4db24
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
$ docker pull mariadb@sha256:3595c1017b57939d4b5c5bc79f5d4822e607d6408f220c2e50a488caacf0c40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105325231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a5574591812b6d742de7eb66de9499e5d19ca112a3905bcb5e8b3984e861a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 04 Nov 2024 20:52:12 GMT
ARG RELEASE
# Mon, 04 Nov 2024 20:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 04 Nov 2024 20:52:12 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 20:52:12 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.10 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=1:10.11.10+maria~ubu2204
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=1:10.11.10+maria~ubu2204
# Mon, 04 Nov 2024 20:52:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.10+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.10+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Nov 2024 20:52:12 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffca277e11521312c9ff768c73231f64c78567f43d5f1d9bc5ef3af9be1b840a`  
		Last Modified: Tue, 04 Feb 2025 04:25:20 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00220736a08a8dab7872e7a0a89c7e34f55b327f74dc5489df01a6e34a328228`  
		Last Modified: Tue, 04 Feb 2025 04:25:21 GMT  
		Size: 5.7 MB (5651425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c605ef08c0677ab707f4d2b7e3038c0f09f0df3cd4117ff3147851294baea9b`  
		Last Modified: Tue, 04 Feb 2025 04:25:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16e41336a6310585e56c31b9986849884a6297c19713791d5f5575e59d1ea08`  
		Last Modified: Tue, 04 Feb 2025 04:25:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1b93e5163ae50ebea76c0aae1d15c09807e29ffd88615638550856892b92fc`  
		Last Modified: Tue, 04 Feb 2025 04:25:23 GMT  
		Size: 70.1 MB (70123303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837901d0595bb0a49d3b2b3fd45633df4ccff546df62dbca7def98f6ff528a44`  
		Last Modified: Tue, 04 Feb 2025 04:25:21 GMT  
		Size: 4.0 KB (4022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de747544bf8fafd3131db6ea4eedddd3399ec1e0f35621215a59aca51ba4fabb`  
		Last Modified: Tue, 04 Feb 2025 04:25:22 GMT  
		Size: 8.4 KB (8370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:733a1caa06418dbd1e27e5828480ce63de7ef8cd01d19f3a6168f750692676d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1758854e090d62f936580765236396233ad94e5a31736cbc5def0e7a04cab1da`

```dockerfile
```

-	Layers:
	-	`sha256:f36a43217a1ca826f73891b8dd82d7f3c81ac799182f8b2fee4f0f44bb8d0e71`  
		Last Modified: Tue, 04 Feb 2025 04:25:21 GMT  
		Size: 4.6 MB (4606596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32443eabf55480cc5fb94623ab4b3b2605f1a05b7a12bbad47524a5f8283acc6`  
		Last Modified: Tue, 04 Feb 2025 04:25:20 GMT  
		Size: 30.7 KB (30692 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:15b12341aef2d4748a1e850e90991ff8f15b597b33b2f7676d802ecaf844cae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99706275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d261d2eafa6429cc2726155fa0f15d485814c20c6ff79b2a16d3b14e6314a1b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 20:52:12 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.10 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=1:10.11.10+maria~ubu2204
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=1:10.11.10+maria~ubu2204
# Mon, 04 Nov 2024 20:52:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.10+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.10+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Nov 2024 20:52:12 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c38f11f7a7d51c88b952297dbfe9af44325b5359e2fd9428576a8e9dd0423c7`  
		Last Modified: Fri, 15 Nov 2024 01:09:38 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579e9462cd3675105caa390627c13f6abac50dde066fcb397b77c61d60cf394`  
		Last Modified: Fri, 15 Nov 2024 01:09:38 GMT  
		Size: 5.5 MB (5473842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c232dcc0266284bd23e4498851581af74b7855d4ad91d097498ce50e6cef8870`  
		Last Modified: Fri, 15 Nov 2024 01:09:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98204272c2f5c6ade4f0d90e981a897b0ce6db3d7baa91479b22c2e3784eb4e7`  
		Last Modified: Fri, 15 Nov 2024 01:11:39 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cb29f83d29f89c27f6e861f6b1361fa0dc92fa81f02142455c66d072691381`  
		Last Modified: Fri, 15 Nov 2024 01:11:41 GMT  
		Size: 66.9 MB (66859539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919c5864bdb3c29b01a472aff858dcaf985e8e3470d491411b5cc16d75f4df90`  
		Last Modified: Fri, 15 Nov 2024 01:11:39 GMT  
		Size: 4.0 KB (4022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dca10932c1d492fb79535ed817948df6033c31f34d966e09c22664f6a0d4a73`  
		Last Modified: Fri, 15 Nov 2024 01:11:39 GMT  
		Size: 8.4 KB (8370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3b6c9e8a47c272140838a02ae78ecd54cf0cbf570d45715e0d0041d837293a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4651159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e2f399949e9789c3088028a66c3465e41886a04d36d2aacd2f17f26b2ea349`

```dockerfile
```

-	Layers:
	-	`sha256:c81eafc33cd6e097b460a00484bf5fd2ba36cd9f5c1761c672db561c7dc01f5d`  
		Last Modified: Fri, 15 Nov 2024 01:11:39 GMT  
		Size: 4.6 MB (4620278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffbc1cc2822735d77ce6ab22ac1001a073b2adff99832b2600bac1ca3d009b11`  
		Last Modified: Fri, 15 Nov 2024 01:11:39 GMT  
		Size: 30.9 KB (30881 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b6f261135a8edba472d4717eb80340458deea9f3c84ec6a5668e386c71d17168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112945305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44a14ab1e08784f621c74878a80e38ea3a94de171528047ffbf37c9dc893e57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 20:52:12 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.10 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=1:10.11.10+maria~ubu2204
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=1:10.11.10+maria~ubu2204
# Mon, 04 Nov 2024 20:52:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.10+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.10+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Nov 2024 20:52:12 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3132e4d90b0718bbccb21bccf86d8773013bb4d50b5fc4d7e6c915fac9121095`  
		Last Modified: Fri, 15 Nov 2024 01:14:24 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d0415149288eb84d5313cbac50deb1d712416ace45dc72f8d4445ef6dfe9ca`  
		Last Modified: Fri, 15 Nov 2024 01:14:25 GMT  
		Size: 6.1 MB (6092184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827922d68101ad697ebdb4550e6e079767f1be10d3e3d634d98f2a22b9ea469e`  
		Last Modified: Fri, 15 Nov 2024 01:14:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bbb3b48f9444af53ad363c81c73ef6135b4f2162bf627e96513d38f5801e79`  
		Last Modified: Fri, 15 Nov 2024 01:18:28 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c67d676ae006f149fba4262749edee6b25aac723d78532daeee655d691119c`  
		Last Modified: Fri, 15 Nov 2024 01:18:31 GMT  
		Size: 72.4 MB (72390316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6850876bad677c846e54d1a4788e162a91f9aa484682e6d9a41fa0731af64e58`  
		Last Modified: Fri, 15 Nov 2024 01:18:28 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3a903b5857de41e959403110d286edd9fc364e9c1d443506a125d742276d55`  
		Last Modified: Fri, 15 Nov 2024 01:18:28 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:9f5fa9501f6c365ecc17dbe5f81764cd28949b340b0f25177b61a0e4f68ff06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4652225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe2aa9fae41943e68efbffa86d37062c95f887e72c3378c17a5c40b81dafc56`

```dockerfile
```

-	Layers:
	-	`sha256:723ba751b7c23f31e957e83b0ae2fc87f65b9306f586bee976f23530d424c184`  
		Last Modified: Fri, 15 Nov 2024 01:18:28 GMT  
		Size: 4.6 MB (4621468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ed1ca28a63271379783598f2eefb1075795c18581644dca36d1cbbdbec69339`  
		Last Modified: Fri, 15 Nov 2024 01:18:28 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:e88a4797dbfccad9f6a2d78d507fdad108189e60fe45026a6f212e2fd2636078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103134146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99d4a81de0bc503f75a385e6906fc10921e3b3ca454508c089b14bcf961a0fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:31 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:31 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:32 GMT
ADD file:6dc78f1eec678e679ed1d9f92297dbcf99806da788dde329389d5d786006603f in / 
# Wed, 11 Sep 2024 16:25:32 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV GOSU_VERSION=1.17
# Mon, 04 Nov 2024 20:52:12 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENV LANG=C.UTF-8
# Mon, 04 Nov 2024 20:52:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.10 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=1:10.11.10+maria~ubu2204
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=1:10.11.10+maria~ubu2204
# Mon, 04 Nov 2024 20:52:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.10+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.10+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.10/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
VOLUME [/var/lib/mysql]
# Mon, 04 Nov 2024 20:52:12 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Nov 2024 20:52:12 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 04 Nov 2024 20:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:41e9fbd89079d8e47609ae158236d59896fd2503db1ebdfef058864054170e01`  
		Last Modified: Wed, 11 Sep 2024 17:25:11 GMT  
		Size: 28.0 MB (28001475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e73977b46f79de83230eb9f50c12bff7f4015d032ef2789bb7beadfce7b427e`  
		Last Modified: Fri, 15 Nov 2024 01:23:34 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecadbaf2161a23600b43c54fba4df458c4a405859a0aae3c362fa36fd325b50f`  
		Last Modified: Fri, 15 Nov 2024 01:23:35 GMT  
		Size: 5.5 MB (5543637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3675917e6b91ec9049f9b6acd30feb913b7009cfbd63cff1ad6d34962680c568`  
		Last Modified: Fri, 15 Nov 2024 01:23:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8c02cf8e5b6dd6307ace4fe91cbc7582c49f9c54ccaab97cf50fdd9e527013`  
		Last Modified: Fri, 15 Nov 2024 01:26:51 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64d144da38337f29276d46fc9327b5ea5a887e726d86eca8a4c4e5ef30e9176`  
		Last Modified: Fri, 15 Nov 2024 01:26:52 GMT  
		Size: 69.6 MB (69574467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3755aec620b56892940e5e0c690b6d683daba229d4c3dde1c2029f3655b2aaf`  
		Last Modified: Fri, 15 Nov 2024 01:26:51 GMT  
		Size: 4.0 KB (4021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7728347385641ed4c8ffa7b3385bb5a421904d28338825198a35dbfbae889c5a`  
		Last Modified: Fri, 15 Nov 2024 01:26:51 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:d76d73ed42c7ce80d46f5ab7888a9830800e52dc54f600a13d2b42bd4eab31f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deec3ac49d8a34f4a37be75c244e5a842a595ed81a8456badaeea76f7332f416`

```dockerfile
```

-	Layers:
	-	`sha256:d925025305318669d5dfe2fdd39d482f88ff2333a35ce5815aa696246f90755f`  
		Last Modified: Fri, 15 Nov 2024 01:26:51 GMT  
		Size: 4.6 MB (4614165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2568dd871179aefced770fa7de51a3b1cba0dbc0b2ec72dfb9a9c612662ec290`  
		Last Modified: Fri, 15 Nov 2024 01:26:51 GMT  
		Size: 30.7 KB (30693 bytes)  
		MIME: application/vnd.in-toto+json
