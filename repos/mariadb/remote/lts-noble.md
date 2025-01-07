## `mariadb:lts-noble`

```console
$ docker pull mariadb@sha256:a3c3ecdba222d33017b1128ae2a5930a3d6b8b21cd6d5e534886e75a523612ee
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

### `mariadb:lts-noble` - linux; amd64

```console
$ docker pull mariadb@sha256:301f8065fc5f7e72288f146d0098d0f27c9c84fcbd5cb9f4f2fb5de46c9cc1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122014371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d75817a027b18f974b742b7846fcaa591eabd37db911557ffccd1fb680aec25`
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
LABEL org.opencontainers.image.version=24.04
# Mon, 04 Nov 2024 20:52:12 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Mon, 04 Nov 2024 20:52:12 GMT
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
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a258d39fecc49209dcf798002f0a692ce0207c1080881a7f7660720d3a7bc`  
		Last Modified: Tue, 03 Dec 2024 02:31:31 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151f16fbb8612414ce3a2d18480ef7a9c793244f92fa8bce394558627c1826d`  
		Last Modified: Tue, 03 Dec 2024 02:31:31 GMT  
		Size: 5.4 MB (5350517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d6d77accdb7a4af6b9d23338ad52021291eeb969b807d912abbc44074ae04d`  
		Last Modified: Tue, 03 Dec 2024 02:31:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2de3fe3ae718dddf7f749d175d6af4e1533113ab238843c1694ad563388fa0`  
		Last Modified: Tue, 03 Dec 2024 02:31:31 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693978e33b66572817da73c4cfea801622d09f2c065a512b8a0dfd4830e0dc5d`  
		Last Modified: Tue, 03 Dec 2024 02:31:33 GMT  
		Size: 86.9 MB (86897661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891a6db0a117759d007bb03aca5c06845903142d75316f9535a865e2f53683f9`  
		Last Modified: Tue, 03 Dec 2024 02:31:32 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6494b26fa42dd80513a1d25d9f78f0d2136b79a2e48557f39294ba5951945e2`  
		Last Modified: Tue, 03 Dec 2024 02:31:32 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:9b4d8656693b156c11d059d4f7c32cdd217bf2634625bf26d8a0abbbf395e5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0fd0dab55487ec277dd6d48f329d67ece1179ce42c8e102665b6d6398ad717b`

```dockerfile
```

-	Layers:
	-	`sha256:7b3075dcd1b2350434453cbda6923535e56fa842176c354c59dce992664a9a5f`  
		Last Modified: Tue, 03 Dec 2024 02:31:31 GMT  
		Size: 4.1 MB (4081420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf45137deec15845b80fd6dc13d44f4388649c41cfb59cdf52c2da1c3e6d7805`  
		Last Modified: Tue, 03 Dec 2024 02:31:31 GMT  
		Size: 30.6 KB (30634 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c06e8915e1a0b315a67878dd083c8a142410c0cdb9c3777c1de703d0346257d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120110243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf030113af3c738be9c5f2cc140da3b301d65448c164bfa2e600c5e1a1c42378`
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
LABEL org.opencontainers.image.version=24.04
# Mon, 04 Nov 2024 20:52:12 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Mon, 04 Nov 2024 20:52:12 GMT
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8410d55eb77c23c37f6fdd5db9bda499708e77470f675d188095eaa222cbca70`  
		Last Modified: Tue, 03 Dec 2024 06:11:08 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c84580ff96a3409d356d4f96126f7cb3bd92f1a919c33e49b5949810cb941f`  
		Last Modified: Tue, 03 Dec 2024 06:11:08 GMT  
		Size: 5.1 MB (5131176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1171ed6095eca2323de7c240f17ee7276b6de114716a8e06db8d48472abd3d`  
		Last Modified: Tue, 03 Dec 2024 06:11:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9608086e97196b771d31cc4520b16e700e39eaa2a49b31adef26d8c53de792`  
		Last Modified: Tue, 03 Dec 2024 06:12:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac99f801551e28c6f97ad4829d231acac96f277dcf37666a146491e7e55f831`  
		Last Modified: Tue, 03 Dec 2024 06:12:44 GMT  
		Size: 86.1 MB (86072170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b27cf94d7e81b5a70a4f2b4ae2c225dec8a9ecda454c09530192370d138d6e`  
		Last Modified: Tue, 03 Dec 2024 06:12:41 GMT  
		Size: 4.0 KB (4039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82e90c5ef2c98a3baa3fdd6b1f2d510c9655abe5951d94dc3d573647bbba5ac`  
		Last Modified: Tue, 03 Dec 2024 06:12:41 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:247f887d9e54c9477d59f77d806516eb252c2ffee6f0b144737ac58099b294d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370f12dbb44214c77464b24c18a876e2ad49e6dcf18368514931fc9cf6dda852`

```dockerfile
```

-	Layers:
	-	`sha256:8cce93432c55bd801863d1b13771bba1dbb511de669e07c5deb233b0a31b7873`  
		Last Modified: Tue, 03 Dec 2024 06:12:42 GMT  
		Size: 4.1 MB (4088675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f28b717be9fff953f52f2c110b004222f69b28b86435fb791bc40521d8e7d5a6`  
		Last Modified: Tue, 03 Dec 2024 06:12:41 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:69f4dc54199833af0a7454af11ae22c01eaa213dd32523efc611220c8db32837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132537600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830c36db2c1bbbdf745fba43af19bd795a22cdf8ca0db096b0d82abb1c57a72d`
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
LABEL org.opencontainers.image.version=24.04
# Mon, 04 Nov 2024 20:52:12 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Mon, 04 Nov 2024 20:52:12 GMT
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
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c4ad61cde3e4f70d92e0c10784a8c538e2b172f5fc35a605ea4b5a67db55a6`  
		Last Modified: Tue, 03 Dec 2024 05:11:11 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34df743fdcbbbdf1d07a2cbbc2b645f038240e098ea232e5b1577dc8f88df5fc`  
		Last Modified: Tue, 03 Dec 2024 05:11:11 GMT  
		Size: 5.9 MB (5937691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a41fce64b994fea112397ebbc6149891964dc35f7bdd0b60d54549351a6cf5`  
		Last Modified: Tue, 03 Dec 2024 05:11:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23946df8147d5dd97af4ccfadbfde765a885315ef8fff859caa65f138133d886`  
		Last Modified: Tue, 03 Dec 2024 05:12:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b5140ea5b653377edfdb7714d95d60706c9f5d98d8e8a8ea668a068d0b67d`  
		Last Modified: Tue, 03 Dec 2024 05:12:53 GMT  
		Size: 92.2 MB (92196862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4734bfc0a6d53c48c5eb5fcedf1d57a3d32f06b7bd26c410e1207c3ba72ffa8`  
		Last Modified: Tue, 03 Dec 2024 05:12:50 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2765a5aa1a0ac9dc2a741f9d8e623240b246b05a0bed72cdcdababcdd4e7ad6`  
		Last Modified: Tue, 03 Dec 2024 05:12:50 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:75aa8e15700c1704cff2a8469aedc5d9ec274584115fa714331b0b3bd3249589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b3b4a6161ab043f67cfb8ec33021bcd659d536689c381975f9a3cb3a455fe4`

```dockerfile
```

-	Layers:
	-	`sha256:9faa8df9e51916e70c896642f58ddf91d6dc070d4169ab8c1540a951debb4fa8`  
		Last Modified: Tue, 03 Dec 2024 05:12:50 GMT  
		Size: 4.1 MB (4089156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:439e90d26e535ee476438f9f571314eae00661068f46fbcb52998956006f91c4`  
		Last Modified: Tue, 03 Dec 2024 05:12:49 GMT  
		Size: 30.7 KB (30698 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:160cc2397d69a8384c589f8ac4c90febcf170b5722028fbc4c388d2c642c1956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128664366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1889b9ca5e1e6434e5e7e0dece59c37f8e4e90f1fdba013b2d5ab893d3fcc92a`
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
LABEL org.opencontainers.image.version=24.04
# Mon, 04 Nov 2024 20:52:12 GMT
ADD file:1c391e128b3c5e552a1401f9520290446bf94ba089c2d74a5d661001d3d8b60c in / 
# Mon, 04 Nov 2024 20:52:12 GMT
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
	-	`sha256:755503a8fb36d6a0d08275c3792ab81b69fdff95054dff0aa932d6dc30107609`  
		Last Modified: Tue, 19 Nov 2024 17:38:58 GMT  
		Size: 30.0 MB (30020826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e5159b15981c6fb531ba987f6463df8bd7c76d925639524e0b51578bf2c349`  
		Last Modified: Tue, 03 Dec 2024 04:34:25 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b231979c7b92f26f06ee8e75a2d82f217fd5651e4157a6924a168d9d294cfae0`  
		Last Modified: Tue, 03 Dec 2024 04:34:25 GMT  
		Size: 5.5 MB (5507498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394375824803f974a376567cfb78cf281f3836b838e24dbd8e38676f1477ce92`  
		Last Modified: Tue, 03 Dec 2024 04:34:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9b6883ddd279d8e2d842da9e137f41b7e0e98c857fd52e376c78f4a2e5842`  
		Last Modified: Tue, 03 Dec 2024 04:36:27 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4656e84ac8a27e1decbf7b7c5059ddc674ffecbcac3c07bd2db4b1be34f32f`  
		Last Modified: Tue, 03 Dec 2024 04:36:28 GMT  
		Size: 93.1 MB (93121812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6235febd299dd39f820f9de8faefaf9ab257bcd90da70bb6b2308790b45baca8`  
		Last Modified: Tue, 03 Dec 2024 04:36:27 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72134aaf2d2be060f95d8405ad97bdacd3616bf35cb4d02531e89b1c4da349bd`  
		Last Modified: Tue, 03 Dec 2024 04:36:27 GMT  
		Size: 8.4 KB (8402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:f21081cb71587e8cad0e192e4a4f1d02ae8f3b7f8b7a472695bdcfbfeef642ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ccb60345ea30b0c68ce592a751331849af614694060f97d4d7e984c0a8dacb`

```dockerfile
```

-	Layers:
	-	`sha256:6487133e3ce9e15d1df8bcc66773355cf5400cfb8236973a4642ae36d4c98331`  
		Last Modified: Tue, 03 Dec 2024 04:36:26 GMT  
		Size: 4.1 MB (4083148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ca1719954faeea743b75638f9e2ca6837e41ed5547388d93200b3850b81d45`  
		Last Modified: Tue, 03 Dec 2024 04:36:26 GMT  
		Size: 30.6 KB (30634 bytes)  
		MIME: application/vnd.in-toto+json
