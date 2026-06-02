## `mariadb:lts`

```console
$ docker pull mariadb@sha256:b1c7bf836e64ed9406a8984af29509f40089d55cea14b32f12c4726a1f17104b
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

### `mariadb:lts` - linux; amd64

```console
$ docker pull mariadb@sha256:181bbc639b0bef9ded18543efba92730b6ae8815102e090bf2c98aea7a247099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105319980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca20b0713cc87f0e9a75d154f677e3f9469e1281f21dd68dc551bf3d93467e27`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:18:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 02 Jun 2026 08:19:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Jun 2026 08:19:05 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Jun 2026 08:19:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jun 2026 08:19:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jun 2026 08:19:05 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:19:05 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 02 Jun 2026 08:19:05 GMT
ARG MARIADB_VERSION=1:12.3.2+maria~ubu2404
# Tue, 02 Jun 2026 08:19:05 GMT
ENV MARIADB_VERSION=1:12.3.2+maria~ubu2404
# Tue, 02 Jun 2026 08:19:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
# Tue, 02 Jun 2026 08:19:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.3.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 02 Jun 2026 08:19:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.3.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server-galera="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 02 Jun 2026 08:19:20 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jun 2026 08:19:20 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 02 Jun 2026 08:19:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:19:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:19:20 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 02 Jun 2026 08:19:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7275653b898c2fb6ae681d9a9050d14bfa4c4c9b04307eb7ea5323b7fed891`  
		Last Modified: Tue, 02 Jun 2026 08:19:35 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a12dae938a68d5fd61ff6484888369b8bd74c2048e12e38e3d3dff6563de88`  
		Last Modified: Tue, 02 Jun 2026 08:19:35 GMT  
		Size: 5.3 MB (5288227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01caa79697196ba6db451bde1d881f20b57fc43e2d74caac25ac2a2e0d66aa52`  
		Last Modified: Tue, 02 Jun 2026 08:19:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b0fe90f305ad010fef24f8c123ef8b32f79d5434b878b5c7384e4643a094d9`  
		Last Modified: Tue, 02 Jun 2026 08:19:35 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e250ad06377550c5ebd82a1a5f44d2f4ff70d55f40d0db093e45985110cf91`  
		Last Modified: Tue, 02 Jun 2026 08:19:38 GMT  
		Size: 70.3 MB (70284628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7641d15fcba655a8a20d70a0cf329cb08b124c1962a3ccdfbc9bed4ecd77fe9a`  
		Last Modified: Tue, 02 Jun 2026 08:19:36 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709e495b90065dfcfeed59f8ddba0706f56d81910828e72799e25712f474fab9`  
		Last Modified: Tue, 02 Jun 2026 08:19:36 GMT  
		Size: 8.5 KB (8495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:d356c88fbf5bfee541ce1017082dc905bed9e21a97b86b68f2521f6ec60f9eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67831f4d4b2c3fc563e494958e6ccf83262303f984cc099d1d2d7258acf9b494`

```dockerfile
```

-	Layers:
	-	`sha256:aa986e03abd8870a70e8715aebadc6f5e094945f833a354493baeda0df632bed`  
		Last Modified: Tue, 02 Jun 2026 08:19:35 GMT  
		Size: 4.3 MB (4282805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a33132d9d5571429f1e821ea2127d6914fd82bc013d5a15148fe3e0d7ec979ca`  
		Last Modified: Tue, 02 Jun 2026 08:19:35 GMT  
		Size: 32.1 KB (32068 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:767055483e6932d70cd7bbc079906b5f64065760034c37d59913862b136a5390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103106414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e89ecfbc1b0bf47c6884dad10b1cde0d631fcae4261387335ace673564d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:19:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 02 Jun 2026 08:19:17 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Jun 2026 08:19:17 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Jun 2026 08:19:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jun 2026 08:19:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jun 2026 08:19:18 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:19:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 02 Jun 2026 08:19:18 GMT
ARG MARIADB_VERSION=1:12.3.2+maria~ubu2404
# Tue, 02 Jun 2026 08:19:18 GMT
ENV MARIADB_VERSION=1:12.3.2+maria~ubu2404
# Tue, 02 Jun 2026 08:19:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
# Tue, 02 Jun 2026 08:19:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.3.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 02 Jun 2026 08:19:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.3.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server-galera="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 02 Jun 2026 08:19:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jun 2026 08:19:32 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 02 Jun 2026 08:19:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:19:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:19:32 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 02 Jun 2026 08:19:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb27e2d9b088a22618dcefc18136788e360501e7e99c36aadf9891061cf35ae`  
		Last Modified: Tue, 02 Jun 2026 08:19:47 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1e545b0d628fbff44b0a67164f68709e67be2d3f1e3fcd8139cfae87a179be`  
		Last Modified: Tue, 02 Jun 2026 08:19:47 GMT  
		Size: 5.1 MB (5098653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2896145ec1460e5b79e3c2786cdc1e5eb6bfbca889ba1eece388a9623f33dd`  
		Last Modified: Tue, 02 Jun 2026 08:19:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c39d8eb161ae1d3afbf72363595d589b634dd82ac1ae5c204c9b0287549e88b`  
		Last Modified: Tue, 02 Jun 2026 08:19:47 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc10798aaf28766994810a2323b0d968c5d89da4727619e4ff5b04288b174f`  
		Last Modified: Tue, 02 Jun 2026 08:19:50 GMT  
		Size: 69.1 MB (69117028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d2b5ba22171618acf58241baf2a2a889c1a9142406fe39adb51cd62cf943b2`  
		Last Modified: Tue, 02 Jun 2026 08:19:49 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c0067f2e3e56faf8ebfcbccba2e7c5bcdd95b84867638615a87d305ab82737`  
		Last Modified: Tue, 02 Jun 2026 08:19:48 GMT  
		Size: 8.5 KB (8496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:91eed9d6e9f0bc37ba3e3849c64d7ce734890b966285a11fe91ea254bee48d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4322410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c586122c6fc7967fdd3b8cf97b6da6869da902c95e879e56e9c43d31f07b42a2`

```dockerfile
```

-	Layers:
	-	`sha256:e5393fdac2a0603369b923dda891de2a4708adfbfed6a89d3a342dd8915a8f91`  
		Last Modified: Tue, 02 Jun 2026 08:19:47 GMT  
		Size: 4.3 MB (4290106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8393f78db4dc84000b01198fbb442a23d35cff916d84cf3470b75ae367659c06`  
		Last Modified: Tue, 02 Jun 2026 08:19:47 GMT  
		Size: 32.3 KB (32304 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f9a7185b5f8a64d520ec28f1ab121b057b694b14113d6f3d2101d5ca02e1f367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115073040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0597f1566f3168e30b0547b0d154336884669970721cbc12c6eb9fb6c62db5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:24:21 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 02 Jun 2026 08:24:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Jun 2026 08:24:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Jun 2026 08:24:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jun 2026 08:24:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jun 2026 08:24:51 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:24:51 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 02 Jun 2026 08:24:51 GMT
ARG MARIADB_VERSION=1:12.3.2+maria~ubu2404
# Tue, 02 Jun 2026 08:24:51 GMT
ENV MARIADB_VERSION=1:12.3.2+maria~ubu2404
# Tue, 02 Jun 2026 08:24:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
# Tue, 02 Jun 2026 08:24:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.3.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 02 Jun 2026 08:25:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.3.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server-galera="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 02 Jun 2026 08:25:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jun 2026 08:25:23 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 02 Jun 2026 08:25:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:25:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:25:23 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 02 Jun 2026 08:25:23 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454d9c4eac43b674a7c40356ef3622d3b6065861008a1fdf328e22e4cec5f262`  
		Last Modified: Tue, 02 Jun 2026 08:25:54 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbe3c0857294d47e91369d47b1271269c4fe735882c661254ec360e4525caed`  
		Last Modified: Tue, 02 Jun 2026 08:25:54 GMT  
		Size: 5.9 MB (5927479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f780480a7db94f8a3c5f98741daba1466610eef11bbaa58bea6dd13cac1cf93`  
		Last Modified: Tue, 02 Jun 2026 08:25:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f476d17cdcdbe713b4210be37e9e4f1b0d999255a5145a1ddf34e76661277d26`  
		Last Modified: Tue, 02 Jun 2026 08:25:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03808b5daeb700519257220d39e4140d912789decb41e569a3fa6aaaf3ce1336`  
		Last Modified: Tue, 02 Jun 2026 08:25:57 GMT  
		Size: 74.8 MB (74817130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d01a1d95f0adb11b804908548800bd0a279e63771f5a8e639ca90ff752bf9c`  
		Last Modified: Tue, 02 Jun 2026 08:25:55 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c77aea3a9793949077db4caa1a0671006e665476f49f283e85db7aea74fde0`  
		Last Modified: Tue, 02 Jun 2026 08:25:55 GMT  
		Size: 8.5 KB (8493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:c03a52677d8211cbbcc0eb20be4f09c5a68d635b63e6a6ad868b89309ef3edcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4322908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d9a3c50baf69b97cd399d56c70ff4a8a5d18aa5cccd02a65bab8c6abf1dcea`

```dockerfile
```

-	Layers:
	-	`sha256:c484dad432c6c096e6a67379ee3fe856794cf3b0d08c2c4cd762bc3e62dae2d3`  
		Last Modified: Tue, 02 Jun 2026 08:25:54 GMT  
		Size: 4.3 MB (4290752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d13a0a5dd3d59bbaccbb2e7c2ad786afcb3481d5bb14fb824345e7cc2e17f50`  
		Last Modified: Tue, 02 Jun 2026 08:25:54 GMT  
		Size: 32.2 KB (32156 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; s390x

```console
$ docker pull mariadb@sha256:3f3bff271ef5580b2ab5075c9981a0b194864c11df03838f5b7628d86bd22f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109584896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9543544edfb21b440c822f179320eac7fb08feb584927bb6c66049a770fa3fa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 20 May 2026 01:37:09 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:11 GMT
ADD file:b574b1e436c2db4e4d66f69c75e47a9aebf0da1ad375147eb2c0b7ff76c6ab7e in / 
# Wed, 20 May 2026 01:37:11 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:15:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 02 Jun 2026 08:15:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Jun 2026 08:15:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 02 Jun 2026 08:15:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jun 2026 08:15:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jun 2026 08:15:47 GMT
ENV LANG=C.UTF-8
# Tue, 02 Jun 2026 08:15:47 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 02 Jun 2026 08:15:47 GMT
ARG MARIADB_VERSION=1:12.3.2+maria~ubu2404
# Tue, 02 Jun 2026 08:15:47 GMT
ENV MARIADB_VERSION=1:12.3.2+maria~ubu2404
# Tue, 02 Jun 2026 08:15:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
# Tue, 02 Jun 2026 08:15:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.3.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 02 Jun 2026 08:15:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.3.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.3.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server-galera="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 02 Jun 2026 08:15:55 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jun 2026 08:15:56 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 02 Jun 2026 08:15:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:15:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:15:56 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 02 Jun 2026 08:15:56 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:c8ebd0a624851e8502e41ee64db2b6a45537554969784d82ebbc91c905cbc2ef`  
		Last Modified: Wed, 20 May 2026 02:16:00 GMT  
		Size: 29.9 MB (29912835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba1de334d77ee6b2dbe70de446413ca95a0c33d62ebddb84399c143053c6d5`  
		Last Modified: Tue, 02 Jun 2026 08:16:18 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7058a5d9cc32ed515dbc9aba3239d46d0a761a756dd18efee75b0f32741a488`  
		Last Modified: Tue, 02 Jun 2026 08:16:18 GMT  
		Size: 5.4 MB (5443860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbc36e0f5632e0a7da88eaf8585286964a453ab21bfcf06dff149e29ccc785`  
		Last Modified: Tue, 02 Jun 2026 08:16:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce911d2eef1e52afa6d8458cf2441ad64173d83350f4542141a37d0836369d89`  
		Last Modified: Tue, 02 Jun 2026 08:16:19 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2202482f8c72a0abdacb02cc272f54df65877adbed726f333ee8f3fdf78fe4`  
		Last Modified: Tue, 02 Jun 2026 08:16:21 GMT  
		Size: 74.2 MB (74213881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf087058c78358e2b340774be99da5bb88f55ab1271ddeb5bde16488cd0d09`  
		Last Modified: Tue, 02 Jun 2026 08:16:19 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c689004bb41bef93c94adb12f69d364048cc35f8e67bc5f7f21399dbf66aff1`  
		Last Modified: Tue, 02 Jun 2026 08:16:19 GMT  
		Size: 8.5 KB (8494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:e71daa1420c1b59b5657c6301004b608ee329807b7154105a8ae76f22d6fad98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4316591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347c25531987df81d621e4baf5fd361b9561fff12a1caa68cb2229478fc4cf01`

```dockerfile
```

-	Layers:
	-	`sha256:da69c92a259f87a215fb135233469491cabed7bef77561736465e5c200adc383`  
		Last Modified: Tue, 02 Jun 2026 08:16:18 GMT  
		Size: 4.3 MB (4284524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6300b8c37226f17557eee55f7d6ca0441dcdd50a17e0bff6df01654ff74ca415`  
		Last Modified: Tue, 02 Jun 2026 08:16:18 GMT  
		Size: 32.1 KB (32067 bytes)  
		MIME: application/vnd.in-toto+json
