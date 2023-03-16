## `mariadb:latest`

```console
$ docker pull mariadb@sha256:9ff479f244cc596aed9794d035a9f352662f2caed933238c533024df64569853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:7781ab82c8701e38b7a039ca155beca4574bd36ac19e5f54b99cee9666ac2249
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123074012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a632f970181546d4d3b8c91fe481fe8220206ee2fd96842b16b7607591de916`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:41:17 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 16 Mar 2023 03:41:17 GMT
ENV GOSU_VERSION=1.14
# Thu, 16 Mar 2023 03:41:17 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 16 Mar 2023 03:41:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 16 Mar 2023 03:41:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 16 Mar 2023 03:41:41 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 03:42:15 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 16 Mar 2023 03:42:15 GMT
ARG MARIADB_VERSION=1:10.11.2+maria~ubu2204
# Thu, 16 Mar 2023 03:42:15 GMT
ENV MARIADB_VERSION=1:10.11.2+maria~ubu2204
# Thu, 16 Mar 2023 03:42:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
# Thu, 16 Mar 2023 03:42:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 16 Mar 2023 03:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Thu, 16 Mar 2023 03:42:34 GMT
VOLUME [/var/lib/mysql]
# Thu, 16 Mar 2023 03:42:34 GMT
COPY file:cee75098a882f7d33ad2c4c4325b29adc56fc66450e6cee3711d5a1af1bda714 in /usr/local/bin/healthcheck.sh 
# Thu, 16 Mar 2023 03:42:34 GMT
COPY file:ebdfbcbc74dda1874f1c75d86e1c32733edb402d13440b2b7140a952010bc21f in /usr/local/bin/ 
# Thu, 16 Mar 2023 03:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 03:42:34 GMT
EXPOSE 3306
# Thu, 16 Mar 2023 03:42:34 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8acee20aa1373513bc9fe4dfdb6c018213d0f3237c8096d1a4915576c740a2`  
		Last Modified: Thu, 16 Mar 2023 03:47:31 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b336495e010df48579a484a6eb91e51ed7b4e51f40d1033424da636bb57dae`  
		Last Modified: Thu, 16 Mar 2023 03:47:32 GMT  
		Size: 5.5 MB (5525636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ab1641dd41896db12138b4052cfc443cabbfd14202c3761a2b89d1703b2145`  
		Last Modified: Thu, 16 Mar 2023 03:47:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf0c5c99086a50616aad5ab404cafe547e7ba4761f76cb54e9fa6a0fe7fa505`  
		Last Modified: Thu, 16 Mar 2023 03:47:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23933543020760709388430bba23a6297a98ab0f6a80add63b2853c9a0146bff`  
		Last Modified: Thu, 16 Mar 2023 03:48:09 GMT  
		Size: 87.1 MB (87105687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931baaab2c80db627a95736b62cc238eb791b8464e748de137f04ce4c4fd3193`  
		Last Modified: Thu, 16 Mar 2023 03:47:56 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e86cc8f0528feace8412da9b3442089f5661dd809eac0e02a299d8ddfc709a`  
		Last Modified: Thu, 16 Mar 2023 03:47:56 GMT  
		Size: 7.0 KB (6970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:122c996e2ec3ebb08155641c2c1b9af2f0d631cf165d6ed394af4d0429a172c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117600067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c428f26ac125462d3dbbf48ce7beecf7987593d45470d025451afb9b02390577`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:22:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 16 Mar 2023 02:22:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 16 Mar 2023 02:22:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 16 Mar 2023 02:23:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 16 Mar 2023 02:23:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 16 Mar 2023 02:23:04 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 02:23:40 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 16 Mar 2023 02:23:40 GMT
ARG MARIADB_VERSION=1:10.11.2+maria~ubu2204
# Thu, 16 Mar 2023 02:23:40 GMT
ENV MARIADB_VERSION=1:10.11.2+maria~ubu2204
# Thu, 16 Mar 2023 02:23:40 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
# Thu, 16 Mar 2023 02:23:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 16 Mar 2023 02:23:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Thu, 16 Mar 2023 02:23:58 GMT
VOLUME [/var/lib/mysql]
# Thu, 16 Mar 2023 02:23:58 GMT
COPY file:cee75098a882f7d33ad2c4c4325b29adc56fc66450e6cee3711d5a1af1bda714 in /usr/local/bin/healthcheck.sh 
# Thu, 16 Mar 2023 02:23:59 GMT
COPY file:ebdfbcbc74dda1874f1c75d86e1c32733edb402d13440b2b7140a952010bc21f in /usr/local/bin/ 
# Thu, 16 Mar 2023 02:23:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 02:23:59 GMT
EXPOSE 3306
# Thu, 16 Mar 2023 02:23:59 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13535f17af4cfc7c7c838aed1afc6db1afab1b0a6a9ff31d260072f1e6acb16c`  
		Last Modified: Thu, 16 Mar 2023 02:28:43 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f6d383d1547fb4485b4c42ff1d5b9f538c11e5cff0f036e195ffede952248c`  
		Last Modified: Thu, 16 Mar 2023 02:28:44 GMT  
		Size: 5.3 MB (5338386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9201b45023f0c3e233bf0c07d2db8a8f7b5a5a67ae901e329ad25de99da53ce`  
		Last Modified: Thu, 16 Mar 2023 02:28:41 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb3110e2e7f1bbf4a824aa5c7529cd93f3306d5f00b3d9f60a5c8b3d80f7b4d`  
		Last Modified: Thu, 16 Mar 2023 02:29:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fe94c36f277b758f24284869ebe3bc212bafa031c7dc7b9a8fdc5edb104741`  
		Last Modified: Thu, 16 Mar 2023 02:29:15 GMT  
		Size: 83.9 MB (83861402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb0ef772bd073058d64d059924df0b4cc358e5551f75a18af0cdf1f3a1c46fc`  
		Last Modified: Thu, 16 Mar 2023 02:29:05 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dedfd38b2981c5b95282beb02bb12c11e5434a4e193b3fe59299e64c4132d4e`  
		Last Modified: Thu, 16 Mar 2023 02:29:05 GMT  
		Size: 7.0 KB (6971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ed763ac615af3d3c834b6c5863617a475484aa6e0f4a27f8e9ac88a0ada9fe6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131812206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdde8858e2da37de4826c3da1988b4fa76bd6866640633523495baab35c34083`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:02:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 16 Mar 2023 02:02:13 GMT
ENV GOSU_VERSION=1.14
# Thu, 16 Mar 2023 02:02:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 16 Mar 2023 02:03:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 16 Mar 2023 02:03:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 16 Mar 2023 02:03:10 GMT
ENV LANG=C.UTF-8
# Thu, 16 Mar 2023 02:05:07 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 16 Mar 2023 02:05:07 GMT
ARG MARIADB_VERSION=1:10.11.2+maria~ubu2204
# Thu, 16 Mar 2023 02:05:09 GMT
ENV MARIADB_VERSION=1:10.11.2+maria~ubu2204
# Thu, 16 Mar 2023 02:05:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
# Thu, 16 Mar 2023 02:05:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Thu, 16 Mar 2023 02:06:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Thu, 16 Mar 2023 02:06:34 GMT
VOLUME [/var/lib/mysql]
# Thu, 16 Mar 2023 02:06:35 GMT
COPY file:cee75098a882f7d33ad2c4c4325b29adc56fc66450e6cee3711d5a1af1bda714 in /usr/local/bin/healthcheck.sh 
# Thu, 16 Mar 2023 02:06:35 GMT
COPY file:ebdfbcbc74dda1874f1c75d86e1c32733edb402d13440b2b7140a952010bc21f in /usr/local/bin/ 
# Thu, 16 Mar 2023 02:06:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 02:06:36 GMT
EXPOSE 3306
# Thu, 16 Mar 2023 02:06:37 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba7b9ff42cc872ae552372ca639c9cb2c921b0aeee53754157d1346ccbd089d`  
		Last Modified: Thu, 16 Mar 2023 02:22:18 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ababd0dcad7ffaea41777a968517d8d7825ffc08a95f9ad06869206154e51c`  
		Last Modified: Thu, 16 Mar 2023 02:22:20 GMT  
		Size: 6.0 MB (5952130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a05e1894ef2f0f623c319a6b21d5f7da33f8e8fae52e21203adf796bb1758b8`  
		Last Modified: Thu, 16 Mar 2023 02:22:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac72e6c5daf59c4450527b75311c760eb10a271d6b9951d4852b41561bea4940`  
		Last Modified: Thu, 16 Mar 2023 02:22:57 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8368b769985c3c0968a9d9b788d14b467042f32b15d90e580b143410284484c9`  
		Last Modified: Thu, 16 Mar 2023 02:23:21 GMT  
		Size: 90.1 MB (90135622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e078c18c4e4698646f6fa5c14a957f3141e9e39bacb7fc35393344b1faa507`  
		Last Modified: Thu, 16 Mar 2023 02:22:58 GMT  
		Size: 3.5 KB (3525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad962e31043ab5911b96ac8f0f3b25f17c4d86ac99c9c47f54c6b5a5ec39444`  
		Last Modified: Thu, 16 Mar 2023 02:22:58 GMT  
		Size: 7.0 KB (6970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:6776cef0f480be971c0746153bfc7d3c6a6ba04acb53448303d2ee7fd50b10d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121445424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c39fb429a2411a98cc5e9ce78feeefc35cd3d0d3f948609f9d0d7162e091bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 26 Jan 2023 05:08:35 GMT
ARG RELEASE
# Thu, 26 Jan 2023 05:08:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 05:08:36 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 26 Jan 2023 05:08:37 GMT
ADD file:a9794efc1a102ab6a7160e660a63f4b267797b8b7e0b0bfd9c04ed62846cfb36 in / 
# Thu, 26 Jan 2023 05:08:38 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:42:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Jan 2023 18:42:50 GMT
ENV GOSU_VERSION=1.14
# Tue, 31 Jan 2023 18:42:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 31 Jan 2023 18:43:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 31 Jan 2023 18:43:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Jan 2023 18:43:06 GMT
ENV LANG=C.UTF-8
# Sat, 18 Feb 2023 00:39:43 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sat, 18 Feb 2023 00:39:43 GMT
ARG MARIADB_VERSION=1:10.11.2+maria~ubu2204
# Sat, 18 Feb 2023 00:39:43 GMT
ENV MARIADB_VERSION=1:10.11.2+maria~ubu2204
# Sat, 18 Feb 2023 00:39:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
# Sat, 18 Feb 2023 00:39:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 18 Feb 2023 00:40:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.2/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Sat, 18 Feb 2023 00:40:18 GMT
VOLUME [/var/lib/mysql]
# Sat, 25 Feb 2023 04:00:33 GMT
COPY file:cee75098a882f7d33ad2c4c4325b29adc56fc66450e6cee3711d5a1af1bda714 in /usr/local/bin/healthcheck.sh 
# Sat, 25 Feb 2023 04:00:33 GMT
COPY file:ebdfbcbc74dda1874f1c75d86e1c32733edb402d13440b2b7140a952010bc21f in /usr/local/bin/ 
# Sat, 25 Feb 2023 04:00:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 25 Feb 2023 04:00:33 GMT
EXPOSE 3306
# Sat, 25 Feb 2023 04:00:33 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:dd969ed9de43018fe5442c859bf66eabf23145b966b9338392ea707aed18b26f`  
		Last Modified: Tue, 31 Jan 2023 17:55:34 GMT  
		Size: 28.6 MB (28641926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b702438b56d7a6aaaad49e2be85e1bb2f3beb85406f6b9db1a232f798c558b3`  
		Last Modified: Tue, 31 Jan 2023 18:48:25 GMT  
		Size: 1.8 KB (1751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60737998d0295bde808ca8856933482817ca605937f714f3cfca1ab0b4ca99ed`  
		Last Modified: Tue, 31 Jan 2023 18:48:26 GMT  
		Size: 5.4 MB (5401827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6e12a0288bb0803aeb23e581ca842e1fdf826fa28b4a730dd83585ea125ff8`  
		Last Modified: Tue, 31 Jan 2023 18:48:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36528da402899a29c65aec506cc3573ecd9edf046e710740371ea56b98466ce`  
		Last Modified: Sat, 18 Feb 2023 00:42:04 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c45532e045d6549e8a41f2b8cce4c9cc336de9d1dac3d929d2a7ea3fee6fcf`  
		Last Modified: Sat, 18 Feb 2023 00:42:16 GMT  
		Size: 87.4 MB (87388947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf76dfdfa839489a3b54c3eb3679f8718726a96a30cc2049089b7ac593b41ae`  
		Last Modified: Sat, 25 Feb 2023 04:02:18 GMT  
		Size: 3.5 KB (3526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f477561fbd237479df484d7fc122750ffa7b64e394c3ca9d2cc6e5072810967d`  
		Last Modified: Sat, 25 Feb 2023 04:02:18 GMT  
		Size: 7.0 KB (6971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
