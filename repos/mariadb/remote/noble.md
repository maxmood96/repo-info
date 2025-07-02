## `mariadb:noble`

```console
$ docker pull mariadb@sha256:1e4ec03d1b73af8e7a63137b8ef4820ac7d54c654a1e99eb76235f210f7f0a06
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
$ docker pull mariadb@sha256:917907503259da62e19f0919308fa9aec26306c7dd45414e2e2039f84d17fa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105212651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb85a4198e98cd9fce0d981f62ed19192af64758a489185cef3694a1a16bba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 10 Jun 2025 21:48:21 GMT
ARG RELEASE
# Tue, 10 Jun 2025 21:48:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 21:48:21 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 10 Jun 2025 21:48:21 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 10 Jun 2025 21:48:21 GMT
ARG MARIADB_VERSION=1:11.8.2+maria~ubu2404
# Tue, 10 Jun 2025 21:48:21 GMT
ENV MARIADB_VERSION=1:11.8.2+maria~ubu2404
# Tue, 10 Jun 2025 21:48:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 21:48:21 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c97d4030429eb4ccd936764171c1510a78bd95f32678dbd6aff7663f1274197`  
		Last Modified: Wed, 02 Jul 2025 05:34:46 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42aa761ecaac51b50f32f640b582008dadf80bd7f0efbb6c85f4ee04e094ffe2`  
		Last Modified: Wed, 02 Jul 2025 06:36:11 GMT  
		Size: 5.3 MB (5349651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e836d78fc035d8dc1c5b9d572520a0893d092d989be8a74b3ccb91d2f5bf8ad5`  
		Last Modified: Wed, 02 Jul 2025 05:34:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c36e8aa1e11272b104943ffa9c3127fb6a3809487cb6c6ac03d898b3553bb06`  
		Last Modified: Wed, 02 Jul 2025 05:34:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdcdfe66d35295022da0a33d0b561580b1fa1f434109fb44929f9462fd5fac`  
		Last Modified: Wed, 02 Jul 2025 06:36:14 GMT  
		Size: 70.1 MB (70130410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39f6f058529c2336e2386cddcb2ab6665b3a126fa666d0fb73da23bb25ef7c`  
		Last Modified: Wed, 02 Jul 2025 05:34:24 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed96ced3b10e78b5be9f7bc0757589862cb9ff959f171dde5e0324a877a9b2d`  
		Last Modified: Wed, 02 Jul 2025 05:34:55 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:37bc49e7bd470a99ff18b70b06bfec20b5dac74e9384c0bef30968bdbb38487d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4289289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d0fd3f8d1e9783454979d17c922018dc0e6926735c3b2b367d31de98c30860b`

```dockerfile
```

-	Layers:
	-	`sha256:234d1901f3550261c875063e915e1ae173fcadb9ac23db81f18da146a54a6e0d`  
		Last Modified: Wed, 02 Jul 2025 06:36:15 GMT  
		Size: 4.3 MB (4257462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5720047fb3040f67077b4286c51302297ff1a22684b5836a9d96d1ce2a46dad`  
		Last Modified: Wed, 02 Jul 2025 06:36:16 GMT  
		Size: 31.8 KB (31827 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:709e75cdec991997b97ba640146169f61ee51303e37859382794b15c46894aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103158303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd2e2303fe7c6ec49dc8960f96fa432eb416a07a62742077f4bc0905607e79a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 10 Jun 2025 21:48:21 GMT
ARG RELEASE
# Tue, 10 Jun 2025 21:48:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 21:48:21 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 10 Jun 2025 21:48:21 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 10 Jun 2025 21:48:21 GMT
ARG MARIADB_VERSION=1:11.8.2+maria~ubu2404
# Tue, 10 Jun 2025 21:48:21 GMT
ENV MARIADB_VERSION=1:11.8.2+maria~ubu2404
# Tue, 10 Jun 2025 21:48:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 21:48:21 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d0ab51842fcd4835d1197dd08159510aad0b73e62c58b4d8c43909ee98f3b9`  
		Last Modified: Wed, 02 Jul 2025 05:46:58 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed130d71fe76bbaebd16020157b3a8a5aa15ef2ac276d55238364702f82eafe5`  
		Last Modified: Wed, 02 Jul 2025 05:46:59 GMT  
		Size: 5.1 MB (5130462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35426d669ad56385febdf5ad606a46b1363a8386660adcebbcb98fd58f481ee`  
		Last Modified: Wed, 02 Jul 2025 05:46:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4acfa4e7aa53aa321c617c1ccc31edc7797dbc983290ee6cef7dad955a24cb`  
		Last Modified: Wed, 02 Jul 2025 05:47:32 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49abdf238415fb94c5bcd4bcf8f735956e7c9b142832f9fdcc7b610a1d0dbec9`  
		Last Modified: Wed, 02 Jul 2025 05:47:37 GMT  
		Size: 69.2 MB (69157593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5050508f71fea03c0abb116af0b72c1360be63d2ac5dca6e915ed91aeeb72f`  
		Last Modified: Wed, 02 Jul 2025 05:47:32 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc614bd55efc26429dfb4cf90dbe81d8dc1e80df0ae0935b9b2cf19229e2570`  
		Last Modified: Wed, 02 Jul 2025 05:47:32 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:1806aee7b207d0eb8de462e01ca574db4f39a7245d2613009e2ef8de1d78dbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af21e9294181ecf81c72b36c1e1752c9485d97f34b7d7f0bee841642ee332a0`

```dockerfile
```

-	Layers:
	-	`sha256:b6091830aa7847f0374c67a57b0ac360473af383540e069e72977251229b0f30`  
		Last Modified: Wed, 02 Jul 2025 06:36:21 GMT  
		Size: 4.3 MB (4264760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:989177557a9c00a25772ea457cfba8c20a5cff8498f4b092c417b05e44f22ea3`  
		Last Modified: Wed, 02 Jul 2025 06:36:21 GMT  
		Size: 32.1 KB (32064 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:502331aee928722982f4c21f8e3f705ab4b012be2c2b92366822dacf909d70f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.3 MB (115333350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd375c52cd06418c09c3266f95d7a605dd147310d48e8d735f495e7ae988990b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 10 Jun 2025 21:48:21 GMT
ARG RELEASE
# Tue, 10 Jun 2025 21:48:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 21:48:21 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 10 Jun 2025 21:48:21 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 10 Jun 2025 21:48:21 GMT
ARG MARIADB_VERSION=1:11.8.2+maria~ubu2404
# Tue, 10 Jun 2025 21:48:21 GMT
ENV MARIADB_VERSION=1:11.8.2+maria~ubu2404
# Tue, 10 Jun 2025 21:48:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 21:48:21 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724bbc30bc8a3bbda617509c9f4b141802529966957f5f031e3f2a092994c552`  
		Last Modified: Wed, 02 Jul 2025 03:57:57 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a1abee25181ead0c12172ab11adcf249f92fa0e0a0a5b2cf3a8cec489f272f`  
		Last Modified: Wed, 02 Jul 2025 03:57:58 GMT  
		Size: 5.9 MB (5913584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91f8ebf74d591e852fd8486f64e5c3d3f67245c538244d48bfbf8b79262bd9a`  
		Last Modified: Wed, 02 Jul 2025 03:57:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131caf5f6634147cd9f4d8f8029f9fd9bb37ccdc1d6930a24409179c428e78ed`  
		Last Modified: Wed, 02 Jul 2025 03:59:06 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239ce2d4b9d03cc70d1d427b69c553af84ebf00821333de48f2ce22878b1b336`  
		Last Modified: Wed, 02 Jul 2025 03:59:10 GMT  
		Size: 75.1 MB (75084035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d35afdb14e80442c7cc0e1f07d7f1efc5086f4a396d1240fca966511275c2f`  
		Last Modified: Wed, 02 Jul 2025 03:59:06 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc5d5b3a7f23638a91074a360cf97d822e2cac50dfa4c1f9ca51e667926ffa0`  
		Last Modified: Wed, 02 Jul 2025 03:59:05 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:943c87eb0ff155eddc04f6c92c12cb0d5d1f2133f7f359a5cd79cb000f0f345b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4297302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de061a5d7b103273c2e5f3a936031496c9fc3fa7c9b0fc5058aaca5f70dd04a`

```dockerfile
```

-	Layers:
	-	`sha256:5f16a1723ce1cc3e8a26fbbb29fa681d2783bc285bcc164329a01a6d31c6ae8f`  
		Last Modified: Wed, 02 Jul 2025 06:36:26 GMT  
		Size: 4.3 MB (4265386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce5daf5b639ab49a0964ef471ba5073768bc7674850823d0c537798b7472e6ce`  
		Last Modified: Wed, 02 Jul 2025 06:36:27 GMT  
		Size: 31.9 KB (31916 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; s390x

```console
$ docker pull mariadb@sha256:5ec596d633b5b57723864f614d4f532edf10e351f7d1f95c72943bbac56feaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110625128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e10457bd3412240ac574be0e7e3435154ed02c42b317b81cf771f97ead571d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 10 Jun 2025 21:48:21 GMT
ARG RELEASE
# Tue, 10 Jun 2025 21:48:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Jun 2025 21:48:21 GMT
ADD file:80b0b0c2a08a762cf6a520d8428a5c769c29e72f4a51630adb2231f2816c50c4 in / 
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["/bin/bash"]
# Tue, 10 Jun 2025 21:48:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 10 Jun 2025 21:48:21 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENV LANG=C.UTF-8
# Tue, 10 Jun 2025 21:48:21 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 10 Jun 2025 21:48:21 GMT
ARG MARIADB_VERSION=1:11.8.2+maria~ubu2404
# Tue, 10 Jun 2025 21:48:21 GMT
ENV MARIADB_VERSION=1:11.8.2+maria~ubu2404
# Tue, 10 Jun 2025 21:48:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 10 Jun 2025 21:48:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 21:48:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 21:48:21 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 10 Jun 2025 21:48:21 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:30d64ca13d9d94eb48bf3fece3e38a4e60931d72f1a8c633dec981e43a0515a4`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 29.9 MB (29925630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0b4e297691b91b7735e0a3a2664d5dbc1112715861daf73f75c6b8997e162d`  
		Last Modified: Wed, 02 Jul 2025 04:52:12 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e626ae79a27aa63b103bdeee154ee27509ef53bfc4fae1a29def9bb3fbd9597`  
		Last Modified: Wed, 02 Jul 2025 04:52:13 GMT  
		Size: 5.5 MB (5483122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85104a65e442766ada93dddfb525c6001eb36ad85d71509df3c694e946f23e7a`  
		Last Modified: Wed, 02 Jul 2025 04:52:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbe5cb3bbf864bbcba8caedc28040c5ab79c59bf5b8b6bc10abdc1d49e91e5e`  
		Last Modified: Wed, 02 Jul 2025 04:53:05 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df97cbbda5694350097ef5fb2863375fce3126fd0e27bdc89fbaf78b51e9795`  
		Last Modified: Wed, 02 Jul 2025 04:53:11 GMT  
		Size: 75.2 MB (75202147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b570cf95d8482827c22cb708ac717b9626b2c6abaedf1322c0ecd7fe0583844`  
		Last Modified: Wed, 02 Jul 2025 04:53:05 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73701a1dd9e4755b792f7d5a440be185b1de8b5587e80fa5659f7679695fe2bf`  
		Last Modified: Wed, 02 Jul 2025 04:53:05 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:ff3b8e8dc9e022cccaf1a81f08ef3f377df6f5f170de3f8b138147bec0d34e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a81df43f0b6f0fa1b63e61bea97f746b52b1408aa6d0495fe4bf3240ad81a3`

```dockerfile
```

-	Layers:
	-	`sha256:c59ea001955a9cf121e543e8117cef155a0a2adeae0f64ea18db7acd84255bf2`  
		Last Modified: Wed, 02 Jul 2025 06:36:31 GMT  
		Size: 4.3 MB (4259184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a70c34c05e5dc636082da52f05c7048c67c493c42e5f64fb9a2f038701a2557`  
		Last Modified: Wed, 02 Jul 2025 06:36:32 GMT  
		Size: 31.8 KB (31828 bytes)  
		MIME: application/vnd.in-toto+json
