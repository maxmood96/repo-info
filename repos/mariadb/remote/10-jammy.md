## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:41d89394db8e777d96058d4cf5cf4daf1ed87f76192154f3d89572676f1e2327
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
$ docker pull mariadb@sha256:912ea5d17d351c994d927f9cd7981b185c7ba4f49ea5dff9fcea9936c15022af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99697151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31d622db920740ab873d5a3b9f643919a3eb61ea73f2d200f324bf771f97ee7`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad7fd04bcfca240498c7c5cb9b2dcdc39faff0b42bc40e63c9a5e28e89b91a1`  
		Last Modified: Tue, 04 Feb 2025 10:07:11 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16cf76cb563417ed145801a277217ea3fbb793824bd7df9c5ba330b78143826`  
		Last Modified: Tue, 04 Feb 2025 10:07:11 GMT  
		Size: 5.5 MB (5466736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24515a17f2f197502ffafe77924931726bf523a5e5f59b4cd08c8632170412bb`  
		Last Modified: Tue, 04 Feb 2025 10:07:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9739233311f234a8a15a3db11ec1fc6c88251d88eda6a07805ca5c72b6fe9c88`  
		Last Modified: Tue, 04 Feb 2025 10:07:54 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfcdcfdc995d1af5369e7171c5a851bd6a5122b5af194aa197dce75ce7397f1`  
		Last Modified: Tue, 04 Feb 2025 10:07:56 GMT  
		Size: 66.9 MB (66857673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0587b1895d1d26c609de2c1f3f3676c47501dc9ecce6b0920a7997daff478a1`  
		Last Modified: Tue, 04 Feb 2025 10:07:54 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025707cd71fe7e4afc72d712799ad54a81b322782812fc974ddd65b5141cae09`  
		Last Modified: Tue, 04 Feb 2025 10:07:54 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:fa89b42f587473d6dd337b5b04fe165763108028c5700586ad37077558ca1ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863187e4513f455bdd433cb9706320871da1c85541aef72c82fd2e2888de52e7`

```dockerfile
```

-	Layers:
	-	`sha256:804dbb84844ace6bb98c3d8346a1f0c28aa2209644551f1f32dd5950687a5a08`  
		Last Modified: Tue, 04 Feb 2025 10:07:55 GMT  
		Size: 4.6 MB (4613031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db5e9889f64df7caa129d08069ed1804dcddb7f49d1c868fd61e3557c7d9c62d`  
		Last Modified: Tue, 04 Feb 2025 10:07:54 GMT  
		Size: 30.9 KB (30881 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1cd9c53104e10c50eae1407fa020aafc92f3ece091a5d309ca0b096d12f9433f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.9 MB (112938246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e74693739323506ca0e8bbdc7e15895f060405f759768df61988dcf5eeebe7`
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
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
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
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357a16632e4de6288d9bb2734f3de6fdc5e5b3a424d30f6efdb7b704028cc65c`  
		Last Modified: Tue, 04 Feb 2025 08:33:44 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89041ca393a386d0528ca971b916e645f3b894a0906b4015db31f649478e983`  
		Last Modified: Tue, 04 Feb 2025 08:33:44 GMT  
		Size: 6.1 MB (6083770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dea452277118e89b2c39ef112985efffa26ee3ba08fd44ac2d18e037748a65`  
		Last Modified: Tue, 04 Feb 2025 08:33:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4b52626aefef0bbb65bc796b274f95740063facbd211a050f9e8ffeb5c9183`  
		Last Modified: Tue, 04 Feb 2025 08:35:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e243cc20ec6bc4a5851f4cf611666d45083c904afbf8d16be5b2e8fd09c1471`  
		Last Modified: Tue, 04 Feb 2025 08:35:15 GMT  
		Size: 72.4 MB (72391973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df4c799507501fc8f707939bffdd97da04ad64d1111c7a34da433662676b19`  
		Last Modified: Tue, 04 Feb 2025 08:35:12 GMT  
		Size: 4.0 KB (4021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b16df2bd4233d479af2da3c4cf501c83c0830592cc8c4ed3e104473c792501a`  
		Last Modified: Tue, 04 Feb 2025 08:35:12 GMT  
		Size: 8.4 KB (8370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:7732dbe9b9fd2bfc2a0e8495467c3cd4fe85c393bf1c67dd0a18006131190b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eda42092ed211698875c72700f43e5a08de126cb639c5eba08a0b2a76c39077`

```dockerfile
```

-	Layers:
	-	`sha256:fb32cbdfc191b1886b153b43c7c9c5f3c6c47838e6d31d06b6569d373d7a19a5`  
		Last Modified: Tue, 04 Feb 2025 08:35:12 GMT  
		Size: 4.6 MB (4614227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:894dfe91fed15a51a5d6c8154eb9d6133a936f1dba6e82727bf44ab5d1648a6c`  
		Last Modified: Tue, 04 Feb 2025 08:35:12 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:a56a1af654a00ca95b88e6a83d7eaf665bb7c5deeeb55ddc602356cbc88cc1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103123178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf638005ff53f87268bbe9bbee5f12f752c4452261643931e5f85d78c54b7cf`
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
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
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
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d224b13d530b9856a1b176c7734a0e9649c9bca377e70870c5ff240adaa96f`  
		Last Modified: Tue, 04 Feb 2025 08:39:48 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffc9064cdbe5960ffce39870efd0efc62f243105812d88aafd97eb564b781ba`  
		Last Modified: Tue, 04 Feb 2025 08:39:48 GMT  
		Size: 5.5 MB (5533225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16128eb5ceae7e75c56ede8079e61f5f007ad6274c6de897fb5670c63f7cc94a`  
		Last Modified: Tue, 04 Feb 2025 08:39:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfbb2fa421c7f3fe54cd77a478bb9e8ac23b3269c2fd34785500c07ce8f9b04`  
		Last Modified: Tue, 04 Feb 2025 08:41:07 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3fc5ab4960d2412e87e49f7ba092ff32be92472f4567f256ba280a0277435b`  
		Last Modified: Tue, 04 Feb 2025 08:41:08 GMT  
		Size: 69.6 MB (69574462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d756d483973b581b7262abc6d78e4388d3c3c6c46f014d9681aaf8f47d299efa`  
		Last Modified: Tue, 04 Feb 2025 08:41:07 GMT  
		Size: 4.0 KB (4018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5381b3f084105f912e00e3a4f6c43ba25ef815ea397ea46e1cbca65df83fc1e`  
		Last Modified: Tue, 04 Feb 2025 08:41:07 GMT  
		Size: 8.4 KB (8369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:43ff3dca75be029abeec61c1d981c67454f6662d5d60971828cc53019eb591d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288a008cc73f512bf18a4a746de91ea319d5822ea0c65b89292c950c48c67b72`

```dockerfile
```

-	Layers:
	-	`sha256:b07fe4660198bbdcbfb28e4a390cd786dc60821c83857d12b743f9fb51342237`  
		Last Modified: Tue, 04 Feb 2025 08:41:07 GMT  
		Size: 4.6 MB (4606922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4793a17c57283092258e7d52f1cb85d64c5ddeea63ee3b9fee57418d823e88ff`  
		Last Modified: Tue, 04 Feb 2025 08:41:06 GMT  
		Size: 30.7 KB (30693 bytes)  
		MIME: application/vnd.in-toto+json
