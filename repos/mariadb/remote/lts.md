## `mariadb:lts`

```console
$ docker pull mariadb@sha256:ee0d8acbcfa5ae69bbe5bb12523c894420ba765dbba8613c2e4e06c6bfe4574d
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
$ docker pull mariadb@sha256:60bc836f227905bbd4e5729a10af65e450a2736588844107cac31bf6e9c0f686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122011846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471b74aa31c8968da48d4f77af9c435f227c8cf77f15aebf8f56f41e140b77cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=1:11.4.4+maria~ubu2404
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=1:11.4.4+maria~ubu2404
# Mon, 04 Nov 2024 20:52:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e46408bca3a3b771f3b91f1607d217e59ad7442d78a4a6992b008fbe81e402`  
		Last Modified: Fri, 15 Nov 2024 01:03:06 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440317787c9f101c4ebf7671f985bab8ab6af5746cc0a4c7f4324cbbef2853e3`  
		Last Modified: Fri, 15 Nov 2024 01:03:06 GMT  
		Size: 5.4 MB (5350080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bfbd8605edde9893e2299127eae130848963b47417d0a6f62d1bf6cf6fda77`  
		Last Modified: Fri, 15 Nov 2024 01:02:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7aab60057e1517136bad0065cc89c69dec395526966ad96a7846c5d9f29cbf`  
		Last Modified: Fri, 15 Nov 2024 01:03:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b642accec30a11c8992c67adf3d1ba65f9bf2dc2f796d69b798b1d9fd1f5d9`  
		Last Modified: Fri, 15 Nov 2024 01:03:09 GMT  
		Size: 86.9 MB (86897171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773e3af6d2ccb6c930cb950a463014bd4d97db7f7c1b9be8a032a7a4068ee00f`  
		Last Modified: Fri, 15 Nov 2024 01:03:07 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cac4d61156b0980e8a3bc8f6fa92055fbcdc23663cb19f7dee8da6e99bd9d3`  
		Last Modified: Fri, 15 Nov 2024 01:03:07 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:fa76f37a0b178b85efe0cf860116a845b1a373b82a150136e9abf46ee638fa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb68de940c8dc3197ebfff2865cf8f25743740b88f68fd8e74c6cd66339cb04`

```dockerfile
```

-	Layers:
	-	`sha256:ecda5f5b216ce5d5b28b0cc71f9a4536cef25fbb2788e24d07f23ce806c502a9`  
		Last Modified: Fri, 15 Nov 2024 01:03:06 GMT  
		Size: 4.1 MB (4081392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f897545a71f49aab4a600ef03b2916481fe1a871d95f55bd8c3d17e6d2e531da`  
		Last Modified: Fri, 15 Nov 2024 01:03:06 GMT  
		Size: 30.6 KB (30634 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:782aa2133d690d18c3c2cca3930d72c1f9f7a0c6c4c8d9680b0ec92eb30fd08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120109490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac4e786b503134a65b4673a4d9d0550574ce703337d19a36f3da8918f8c3162`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=1:11.4.4+maria~ubu2404
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=1:11.4.4+maria~ubu2404
# Mon, 04 Nov 2024 20:52:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eabcfaa7ccb5f6b6e3e9da6023938df31a3bf2511800a5977dd022460358f9`  
		Last Modified: Sat, 16 Nov 2024 03:15:14 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4766abebcfb3c3b5abc7e47d92df3d6c113aba1f55efbbff0209ed65eb95ef`  
		Last Modified: Sat, 16 Nov 2024 03:15:15 GMT  
		Size: 5.1 MB (5130947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1f409df817fa7b07e34882ed056eddc429d034e5a7dc8f367c3a9c6b4d00b`  
		Last Modified: Sat, 16 Nov 2024 03:15:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87100dd832325bca5b768ed4d8ad859a91fd1fd44fe077f677459767168cf43`  
		Last Modified: Sat, 16 Nov 2024 03:17:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e904e601389f35822efdb8bd9e2178c04b593a3a8cd5c0fd63c42ff73edcd4`  
		Last Modified: Sat, 16 Nov 2024 03:17:04 GMT  
		Size: 86.1 MB (86071889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a51cbd80fafb441f7e236ba997262aa20102124b2960463d4671ecfb90f724`  
		Last Modified: Sat, 16 Nov 2024 03:17:01 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387a2280044e13670837ccb370d2064fe5a1c6041522bbd2680c39b63558ac85`  
		Last Modified: Sat, 16 Nov 2024 03:17:01 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:b5f05bc7092cf32778e8052b6f5fdb10620d8183f0c718d63276e8bacd80eaa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b66e64b6f190f72ad62d9c856b182f37a57605a2758dc8e7e467d4fda7f2281`

```dockerfile
```

-	Layers:
	-	`sha256:d8bf29bce29c982be45f35fdecc8351c3ec850b704d970a30cfaffb73e5dba97`  
		Last Modified: Sat, 16 Nov 2024 03:17:02 GMT  
		Size: 4.1 MB (4088655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9352245e96b4e7df52076fc2963bba26f00b89e7aa7bd6a8c301b519e7e0889b`  
		Last Modified: Sat, 16 Nov 2024 03:17:01 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:bae394fa5123264cdf9c87f9cf8502236a3a21a2dc4617d4e9c85721bd1d401e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132537555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b0c44ed86e2f701c5d38ab59e5ddae04e956d9145ccab486ccce9d64f1970a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=1:11.4.4+maria~ubu2404
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=1:11.4.4+maria~ubu2404
# Mon, 04 Nov 2024 20:52:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
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
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dfe78f10b46fb930cab6e8339f6bc333fef3b19cd4ef8bb5306765cbdfc5f8`  
		Last Modified: Sat, 16 Nov 2024 03:10:23 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20de38524a6c61f908c6070ec5cebdda40f07ca2bb51d4130e4ed71045c8825f`  
		Last Modified: Sat, 16 Nov 2024 03:10:24 GMT  
		Size: 5.9 MB (5937580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75fc23420819f15d897b25e52419cf3a911bd45c919aeeb7c7c31c377201592`  
		Last Modified: Sat, 16 Nov 2024 03:10:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf089fd0f7c7968e5290c3e3ae87260abed03a0cd0e995ec5bba13ddba67771`  
		Last Modified: Sat, 16 Nov 2024 03:13:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f93579aaa24297f77ba6c40f2edc7e17c36627fe4387ba720c784e48828f66`  
		Last Modified: Sat, 16 Nov 2024 03:13:16 GMT  
		Size: 92.2 MB (92196925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fa222a794abdd10f295900bf0160d625f2d0e0a10eb2dcc171f7e04d0c3845`  
		Last Modified: Sat, 16 Nov 2024 03:13:13 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7b992345d70e3daa239a1f6782de2654c348125cf043986a64385931f9a233`  
		Last Modified: Sat, 16 Nov 2024 03:13:13 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:549b6a1ca83262232ca1c9eafcb59089735212f2547dafc100e109b48d8330d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f9ddb71b449b48adeddfaf1cb2159766544ee0e3680492d299bd5946273f7e`

```dockerfile
```

-	Layers:
	-	`sha256:89f14f704a0474586265ff7e4e9bfa1e90f13fb94e6a1c60e951c396fc4a8a40`  
		Last Modified: Sat, 16 Nov 2024 03:13:13 GMT  
		Size: 4.1 MB (4089136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb02b3cc7103d9aa523db2362b5f02ab54864b49c3815d1a9633f182e9ba981e`  
		Last Modified: Sat, 16 Nov 2024 03:13:13 GMT  
		Size: 30.7 KB (30698 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; s390x

```console
$ docker pull mariadb@sha256:8fd1af8d34d6fa0ff885784a19d1ef8021b22e732478a8f1547011de8f8226a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128664251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cf58bf0b13040033a1953831d9a013afc593c840117bafa887cdffdbd5a3c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:33 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:33 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:34 GMT
ADD file:1c592b6de2557bde912d6291330e1604327193966f24da30f3ecf513f06fd372 in / 
# Wed, 16 Oct 2024 09:25:34 GMT
CMD ["/bin/bash"]
# Mon, 04 Nov 2024 20:52:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 04 Nov 2024 20:52:12 GMT
ARG MARIADB_VERSION=1:11.4.4+maria~ubu2404
# Mon, 04 Nov 2024 20:52:12 GMT
ENV MARIADB_VERSION=1:11.4.4+maria~ubu2404
# Mon, 04 Nov 2024 20:52:12 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 04 Nov 2024 20:52:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
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
	-	`sha256:4d3763c838a1509ac75e9b37aa0fba11067b054033fda0d642f7e32e542b7994`  
		Last Modified: Wed, 16 Oct 2024 12:48:36 GMT  
		Size: 30.0 MB (30021284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29ec7e72011739d93df9620d95a353d6c2a0aaf344e87b6c1f3b613051ac9fd`  
		Last Modified: Sat, 16 Nov 2024 03:05:42 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5d3e39652e2869b119c348709a75534a876363cc4a3bb07c5db1e8746d1b6f`  
		Last Modified: Sat, 16 Nov 2024 03:05:42 GMT  
		Size: 5.5 MB (5507283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aadf03fd44585230061feb5d1540d438343684f926d47d7e1f09a629a3a696`  
		Last Modified: Sat, 16 Nov 2024 03:05:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516e604fe33915c70c1f20dd68f1a485dd7f133d9e89ef6e7e0a8468b3d76f9d`  
		Last Modified: Sat, 16 Nov 2024 03:07:55 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae25846e6d18dda9380f45f4b66a6b249833b078e67d0ef91cad1be66aea76d2`  
		Last Modified: Sat, 16 Nov 2024 03:07:57 GMT  
		Size: 93.1 MB (93121453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54d2c9862454ca0ee501dbfb5d49f36e23605179d07655719aaed58a931ce0b`  
		Last Modified: Sat, 16 Nov 2024 03:07:55 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd752d1c58396e5a2175c2d2d7ada6ca246b911b006a9c812ed40603245b751`  
		Last Modified: Sat, 16 Nov 2024 03:07:55 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:3e63c9cd27c88e72c32273f6b1625c4483678e1d5fd9c6f56b1d61db04f1704a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc76368af6f8f96cb626d83ac29a7200a172b3f9ac5b3614604a97d43870ad4`

```dockerfile
```

-	Layers:
	-	`sha256:43cfe5b9319b55192c6f688fef370aa3439911133f3097d95e31989367310c74`  
		Last Modified: Sat, 16 Nov 2024 03:07:55 GMT  
		Size: 4.1 MB (4083128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60e1e4c12576611f17c0fca4d07e988ff65a960f8b016719c57c7b874bda820`  
		Last Modified: Sat, 16 Nov 2024 03:07:54 GMT  
		Size: 30.6 KB (30634 bytes)  
		MIME: application/vnd.in-toto+json
