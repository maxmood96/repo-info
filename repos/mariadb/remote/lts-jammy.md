## `mariadb:lts-jammy`

```console
$ docker pull mariadb@sha256:51d830f73fa70ee5ceb420b765a49e19615d395d655c7f16871c9cc6d93a9cb5
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

### `mariadb:lts-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:2ce8ff67514929c15d8b591753c48183e1e4ed7f70d0bbbacba88c0518597d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122463392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5118c1924b403db4e777470a72de14efc670145e27214fbd209b3db6101ae005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 22 Feb 2024 01:03:14 GMT
ARG RELEASE
# Thu, 22 Feb 2024 01:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 01:03:14 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 01:03:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 Feb 2024 01:03:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV LANG=C.UTF-8
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	sed -i -e '/character-set-collations/d' /etc/mysql/mariadb.conf.d/50-server.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Feb 2024 01:03:14 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 01:03:14 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3c645031de2917ade93ec54b118d5d3e45de72ef580b8f419a8cdc41e01d042c`  
		Last Modified: Wed, 10 Apr 2024 19:20:48 GMT  
		Size: 29.5 MB (29533419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd468dfa2e47775b72a59b551a81fd3a5a1f715cf5382c0a546535d95bf53b8f`  
		Last Modified: Tue, 16 Apr 2024 04:26:10 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9f7d11a85ca36ae79b2250155c543af2f592f5d174abb751b51e5b7c966094`  
		Last Modified: Tue, 16 Apr 2024 04:26:11 GMT  
		Size: 5.6 MB (5647642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c862782187f57f2df31c085aed50451ce73ec4874f2f5a909998c9cb2a02814`  
		Last Modified: Tue, 16 Apr 2024 04:26:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19eebbaded8a02acbb2fe23897ce542d6de35336a6d6ab4a8c0831cf0462a137`  
		Last Modified: Tue, 16 Apr 2024 04:26:10 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a44e70f5e66a7b5e47e6ba1753cd9c63144f17981a576409a33d2466330bd`  
		Last Modified: Tue, 16 Apr 2024 04:26:13 GMT  
		Size: 87.3 MB (87268307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c211c70a1b7e04f5844633c64e0752ccf10b189a2bade4933dd6222fa9f3c94`  
		Last Modified: Tue, 16 Apr 2024 04:26:11 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab88bf2e03b1e25a4d1c8dd35e658abcf563f34f13f469a7cfdf3121387dca86`  
		Last Modified: Tue, 16 Apr 2024 04:26:11 GMT  
		Size: 8.2 KB (8246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:bcc1a6c8b9fde44cab0c82ec97e62cd8f0b9091cda520688a5812c5cbaf0b34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4609133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee5a2fe4cc53e20e8302e89be70d4cf0daeee060b26528e01006de7ca9efe74`

```dockerfile
```

-	Layers:
	-	`sha256:cad8f060d4f449cdf94e7f8ad3573a3fb11fa268bc85ef1bfac69e3a2efd6f9c`  
		Last Modified: Tue, 16 Apr 2024 04:26:10 GMT  
		Size: 4.6 MB (4577703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e28331f63b622f25f2ed4ee3dd3b6a247304ccf2138d44a2ddb3c2527e46ac9a`  
		Last Modified: Tue, 16 Apr 2024 04:26:10 GMT  
		Size: 31.4 KB (31430 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:90fedb039998a1e9c70c170482784625406c6486fa8cedf3a34c121ad7026812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116865283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfe392ece2f31961c8b2684f860e46c01848dabfe85397bde46828e85920693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 22 Feb 2024 01:03:14 GMT
ARG RELEASE
# Thu, 22 Feb 2024 01:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 01:03:14 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 01:03:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 Feb 2024 01:03:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV LANG=C.UTF-8
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	sed -i -e '/character-set-collations/d' /etc/mysql/mariadb.conf.d/50-server.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Feb 2024 01:03:14 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 01:03:14 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f4bb4e8dca02be491b4f72d2ef2127a64ce49c48d0d9c0a0fcaffa625067679d`  
		Last Modified: Tue, 27 Feb 2024 19:00:12 GMT  
		Size: 27.4 MB (27358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a936dfd11bcebe7e6c8d9b5cdba70dee61cdc7c7359b48d8b3f37b562dbc3bbb`  
		Last Modified: Fri, 15 Mar 2024 19:57:25 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b160c94476c618dc71dbde8a876ae246cd24e147e5583265bb6a13dcfeeae3`  
		Last Modified: Fri, 15 Mar 2024 19:57:25 GMT  
		Size: 5.5 MB (5460560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2852b259badd8e4ba47df868855ac821538c3040ba99aa44019faf427074cce5`  
		Last Modified: Fri, 15 Mar 2024 19:57:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b6ddbb08c39c4fd12e6a74ce47cceb34f324d40bf5ffb67264f40e52437130`  
		Last Modified: Fri, 15 Mar 2024 19:59:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f02d97f2d8962afeb547587ed75be83ed87e74a88f0f09a53146a21a8edb34e`  
		Last Modified: Fri, 15 Mar 2024 19:59:42 GMT  
		Size: 84.0 MB (84031967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994fef625868ab58c614abffe3296ef768b447ab1d0600e71a1c124ea2dab00d`  
		Last Modified: Fri, 15 Mar 2024 19:59:40 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce07317f70b495637f2ad1925c4e9d8b5f8540e6748d9be77ec656bcb85723f`  
		Last Modified: Fri, 15 Mar 2024 19:59:40 GMT  
		Size: 8.2 KB (8246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:1b583a20759c852512eeb942b930840cf3f843682c71c5f0df8c07ca2fc1cdab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4615341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2038bec2935900a3ac4f285cb8fc4b247a7896a30ed600ef995499dbe9ef0772`

```dockerfile
```

-	Layers:
	-	`sha256:c2f6a7a4c9f981bed08412fe86035349dd79a54651aa93419c9f9fe39f615ae6`  
		Last Modified: Fri, 15 Mar 2024 19:59:40 GMT  
		Size: 4.6 MB (4584055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e05b9950bf4da1eb6463fae4f1f1a8f05e9a391bd1de4f80331c814414989c8`  
		Last Modified: Fri, 15 Mar 2024 19:59:40 GMT  
		Size: 31.3 KB (31286 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f119b22c9822cac4cce559746d3e989e15ee71b548f7aa58f5f1ef42f934c9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130547460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d79bb2bb26db5c953e17b5454bf3f2dc2820cae5aebf505643737f0aeb5e827`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 22 Feb 2024 01:03:14 GMT
ARG RELEASE
# Thu, 22 Feb 2024 01:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 01:03:14 GMT
ADD file:0dbed3c6dc73c3c23ae9cfc0a37fa355c57611fbae41da7ff9e2ecfe43404587 in / 
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 01:03:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 Feb 2024 01:03:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV LANG=C.UTF-8
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	sed -i -e '/character-set-collations/d' /etc/mysql/mariadb.conf.d/50-server.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Feb 2024 01:03:14 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 01:03:14 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:ec9849f84ea05dcddad3aae1dad17f2f49b3b950c39945bf0207824781a4dc58`  
		Last Modified: Tue, 27 Feb 2024 19:00:28 GMT  
		Size: 34.5 MB (34493757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f46bfdfc37d0885d87421a8a52e25e4341406e62d51f8b82e8c748c069f9fe2`  
		Last Modified: Wed, 06 Mar 2024 03:51:51 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6baf76f4d6981c4ba88d28998ee3236e2977b79105aa0daf176b7a8db0e414ff`  
		Last Modified: Wed, 06 Mar 2024 03:51:52 GMT  
		Size: 6.1 MB (6079165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485ea9dfe5c6876a6ba5f71d93d1f0d5163282774e6b2515adec8516486a93e8`  
		Last Modified: Wed, 06 Mar 2024 03:51:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f2375103336189961fb0577b4ad6d8df037889723bdd0931c0f6b2afefb2a7`  
		Last Modified: Wed, 06 Mar 2024 08:59:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6d500bb7f4311f66db96f7e93af9b0d49f84aca7b189e4ee6355a6c16613a2`  
		Last Modified: Wed, 06 Mar 2024 08:59:45 GMT  
		Size: 90.0 MB (89960505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9656e19536d5558f0e3af1278df43ed88a5f76acd35e5511c539a8d810b9bc8c`  
		Last Modified: Wed, 06 Mar 2024 08:59:42 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b901ff85f7e41c532eaf210763d4f2ce29d7d3214adbf2d11ecda2fbf1ee5bd`  
		Last Modified: Wed, 06 Mar 2024 08:59:42 GMT  
		Size: 8.2 KB (8250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:165846614bf1140987aea837360d4519a3a1d28600e4bee0c647a896cf655911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4616681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15283c1d127aa03e48d6b2f6a60c7f024d04a5356633979b1e8545d93d058208`

```dockerfile
```

-	Layers:
	-	`sha256:496276516c4e207f8df459bb37b899d9b9e1902f3a785587a960d9c46374789e`  
		Last Modified: Wed, 06 Mar 2024 08:59:42 GMT  
		Size: 4.6 MB (4585342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e99667114042eab3560343960f7bfcdb22deef3fb0a98545be46995bf513058f`  
		Last Modified: Wed, 06 Mar 2024 08:59:42 GMT  
		Size: 31.3 KB (31339 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:247544c8111e4f125a2fb69dc378d769a6da95ddccd2ffa0cef7fec9bc532f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121283655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ace1233ef5b9131583a4d14605dcef71825f65ab9497760d3662a6e0bbf462`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 22 Feb 2024 01:03:14 GMT
ARG RELEASE
# Thu, 22 Feb 2024 01:03:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 22 Feb 2024 01:03:14 GMT
ADD file:fc6c0c3ab39493d732bf2a969cf1478735923705ad656cbc6398d4dbe45626fe in / 
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["/bin/bash"]
# Thu, 22 Feb 2024 01:03:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV GOSU_VERSION=1.17
# Thu, 22 Feb 2024 01:03:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENV LANG=C.UTF-8
# Thu, 22 Feb 2024 01:03:14 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	sed -i -e '/character-set-collations/d' /etc/mysql/mariadb.conf.d/50-server.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Feb 2024 01:03:14 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Feb 2024 01:03:14 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 22 Feb 2024 01:03:14 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:137c4868f69560c0e626198e084a56f05d140f3ac9de35f029d58db50ee2bdd3`  
		Last Modified: Tue, 27 Feb 2024 19:00:35 GMT  
		Size: 28.0 MB (28011097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bcf6c3699a53965a5014afe8abfd9f42b27dd065f77156f60fc14aff01bfaa`  
		Last Modified: Mon, 11 Mar 2024 21:20:33 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a83d0eee369810c2238da7145f11da29f6ccb51c23a9d386306510328ae2bd3`  
		Last Modified: Mon, 11 Mar 2024 21:20:33 GMT  
		Size: 5.5 MB (5531802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4647a005159f2ca71a6ec186035a5a10de87700af800a32846943f6e372ada6c`  
		Last Modified: Mon, 11 Mar 2024 21:20:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd80676075ebd013d31abb8a8a5edb7c9ba47128cc3a6955d33bb8c0eb97932`  
		Last Modified: Tue, 12 Mar 2024 00:47:49 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94382a3407d65e77eb4df7026f7e8c94013aee83caadd3b054e29b6fa1a07109`  
		Last Modified: Tue, 12 Mar 2024 00:47:51 GMT  
		Size: 87.7 MB (87726720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05e376fe0c32d97e6b6365823423e10825fc70bb48c6f8d72a0bc0c803dc2f`  
		Last Modified: Tue, 12 Mar 2024 00:47:49 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7685c9751debc0528f686ac6d722832592ff745ea804cec4e4d3814b9f3243`  
		Last Modified: Tue, 12 Mar 2024 00:47:49 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:a1896f962ec297311fab74b626a5947dd44857c98b5cdbbd0bb67f9160d64414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4585876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:697a02921d27f5cf4d50bccec92bdea56b29d1a08c06a2de7754eafd886cdbd9`

```dockerfile
```

-	Layers:
	-	`sha256:7497a1912c1fe3835d0f5e3f57663b3706f62952b55d846956cb21a4679815d1`  
		Last Modified: Tue, 12 Mar 2024 00:47:49 GMT  
		Size: 4.6 MB (4554607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f14d63156ae105b69e91c5e6d2426ad05e2081bfee755b30bf07975e33c622b7`  
		Last Modified: Tue, 12 Mar 2024 00:47:49 GMT  
		Size: 31.3 KB (31269 bytes)  
		MIME: application/vnd.in-toto+json
