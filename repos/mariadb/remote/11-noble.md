## `mariadb:11-noble`

```console
$ docker pull mariadb@sha256:404ebf26ed7a56fbab05c29f6f1e70188e5eadb51bba8cee8d355775776deb08
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

### `mariadb:11-noble` - linux; amd64

```console
$ docker pull mariadb@sha256:017f70170824e1b9016f6a734f3a2177e570872dbbdde1cb23a36536121bc3cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106216940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f221c81748f5ef793e7bf57d858a0fd606a1e03f39b935ddf832fcb889cad0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 18:49:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 10 Nov 2025 18:49:53 GMT
ENV GOSU_VERSION=1.19
# Mon, 10 Nov 2025 18:49:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 10 Nov 2025 18:49:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Nov 2025 18:49:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 10 Nov 2025 18:49:53 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 18:49:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 10 Nov 2025 18:49:53 GMT
ARG MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Mon, 10 Nov 2025 18:49:53 GMT
ENV MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Mon, 10 Nov 2025 18:49:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
# Mon, 10 Nov 2025 18:49:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 10 Nov 2025 18:50:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 10 Nov 2025 18:50:07 GMT
VOLUME [/var/lib/mysql]
# Mon, 10 Nov 2025 18:50:07 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 10 Nov 2025 18:50:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 18:50:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 18:50:07 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 10 Nov 2025 18:50:07 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a874a624acb15083556a9230c25e8042e5a669f9f8386bf38e8ed724452fc`  
		Last Modified: Mon, 10 Nov 2025 18:50:43 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f7fa352d51bb6854a590d493fbf846aad8b1b8ef691de93610344c84d6f8c4`  
		Last Modified: Mon, 10 Nov 2025 18:50:44 GMT  
		Size: 5.3 MB (5288009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93125b8ee3973ec5373969ea64f69b6c176f5d470bb625f8a1d6f24ecf3a291d`  
		Last Modified: Mon, 10 Nov 2025 18:50:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e858aa4c52776ea3dcedc63eca2e4e1ec53fba0708141a198dd86fcfb76b35`  
		Last Modified: Mon, 10 Nov 2025 18:50:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9245809f4f9a55316a512691f104cd51a6716d39462aa259e5b737a87b7de5`  
		Last Modified: Mon, 10 Nov 2025 18:50:52 GMT  
		Size: 71.2 MB (71191555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb90718e36f749add5b236a9878d9a5f74c9d7d3dffad3108d3984b8e9d53121`  
		Last Modified: Mon, 10 Nov 2025 18:50:43 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7549b325aede314ccf0074095164d95f4d3e1e541094117f46166a4f8571a4`  
		Last Modified: Mon, 10 Nov 2025 18:50:43 GMT  
		Size: 8.4 KB (8396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:85e69ba0dc632b88d78fa386d7ddf9fabc71ecc3e982067e31d7e6e13ffe2019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f18daf41d3aa4782d9754ce4f9db36ac131d43fa2f62f48591b33110c20640`

```dockerfile
```

-	Layers:
	-	`sha256:ff41b31bcb04d773048d332df1e491f11a8eb2d30d82e314ddeed66a06f67559`  
		Last Modified: Mon, 10 Nov 2025 19:37:14 GMT  
		Size: 4.3 MB (4273709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f534a5ffda121fbab0a3c4576bb4dad9009d9101dbe72246a824b35d40a29354`  
		Last Modified: Mon, 10 Nov 2025 19:37:15 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d693dcab644f3f7d337e4edbe069a0e068e0deb36ff5456dbf0e8fd1a05fd572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104125170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc25d65a12d36a41f77fbab204dd4ff1b31abca8e0ffc4920ef1264feb61ca22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 18:41:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 10 Nov 2025 18:42:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 10 Nov 2025 18:42:18 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 10 Nov 2025 18:42:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Nov 2025 18:42:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 10 Nov 2025 18:42:18 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 18:42:18 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 10 Nov 2025 18:42:18 GMT
ARG MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Mon, 10 Nov 2025 18:42:18 GMT
ENV MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Mon, 10 Nov 2025 18:42:18 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
# Mon, 10 Nov 2025 18:42:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 10 Nov 2025 18:42:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 10 Nov 2025 18:42:34 GMT
VOLUME [/var/lib/mysql]
# Mon, 10 Nov 2025 18:42:34 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 10 Nov 2025 18:42:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 18:42:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 18:42:34 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 10 Nov 2025 18:42:34 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fc7934de475a6784023f8241612ec81a954e20bfa9656c3b28fa2c8126da26`  
		Last Modified: Mon, 10 Nov 2025 18:43:02 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9966518c46c8a3df4f8e40af09c9e9d7930de7286cb9ae59b99e40a1a88ef94`  
		Last Modified: Mon, 10 Nov 2025 18:43:03 GMT  
		Size: 5.1 MB (5097619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2b38f03bfd4071931cf99759ae0a4aa4adc5687777a26009a4416c6766c27a`  
		Last Modified: Mon, 10 Nov 2025 18:43:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1cd539bd3b7bd682dbfa3fe67abfebfa66e2dfb53e4e4e080addec18d3898d`  
		Last Modified: Mon, 10 Nov 2025 18:43:04 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7436553eab47336174c2b9f8157db80db8b77da2ef7d33d0c3fd8d308d0a835`  
		Last Modified: Mon, 10 Nov 2025 18:43:09 GMT  
		Size: 70.2 MB (70151604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb8e8614fbfe6c025d160c7636836b5ce477ff7f296691c738dff9d3275d431`  
		Last Modified: Mon, 10 Nov 2025 18:43:05 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0773ddd0af1785e9bc414b8d5ca21556169535e959497869dc7d69391bc3e5a7`  
		Last Modified: Mon, 10 Nov 2025 18:43:05 GMT  
		Size: 8.4 KB (8402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:270b5052f831b05113bd84a2f5c194776686a44bcd3b7968907e68a6a613f80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628f3d65228c4789e70c6767969ab46f63b66762b3732dc7868e01b80ed85674`

```dockerfile
```

-	Layers:
	-	`sha256:ea2884f5f0e50e7c751ace0bbcb2bce67242175baed252ca74059071849dffe9`  
		Last Modified: Mon, 10 Nov 2025 19:37:23 GMT  
		Size: 4.3 MB (4280986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5411237b96224c99d5551e3d1d09c56d579f679d2c27a4dc859853321fd6f79`  
		Last Modified: Mon, 10 Nov 2025 19:37:23 GMT  
		Size: 31.7 KB (31667 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3d551d4eb1185506321f61d1ad8d50dfec6adde87792dd3a160116ff09f218a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116401161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5165dd8b3e7abfd894153f7d48d380fb5e93ba12db132de2ca27272bda4e3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 18:43:05 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 10 Nov 2025 18:43:36 GMT
ENV GOSU_VERSION=1.19
# Mon, 10 Nov 2025 18:43:36 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 10 Nov 2025 18:43:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Nov 2025 18:43:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 10 Nov 2025 18:43:36 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 18:43:36 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 10 Nov 2025 18:43:36 GMT
ARG MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Mon, 10 Nov 2025 18:43:36 GMT
ENV MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Mon, 10 Nov 2025 18:43:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
# Mon, 10 Nov 2025 18:51:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 10 Nov 2025 18:51:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 10 Nov 2025 18:51:59 GMT
VOLUME [/var/lib/mysql]
# Mon, 10 Nov 2025 18:51:59 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 10 Nov 2025 18:51:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 18:51:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 18:51:59 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 10 Nov 2025 18:51:59 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffe9eeb970bc22c11002e14f054b14813fd4fcd9ccf5cb0be0a05661bdd26a7`  
		Last Modified: Mon, 10 Nov 2025 18:45:00 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50c8e61acd9dcfd32202787f32a5b23ad049003774ca2556736264fecb85b0b`  
		Last Modified: Mon, 10 Nov 2025 18:45:00 GMT  
		Size: 5.9 MB (5927264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72a2ca1e4b5d729ff5cdc03ea29f8c8256ceb2982113d3f5e04c38c9c18b28c`  
		Last Modified: Mon, 10 Nov 2025 18:45:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d776bfcc7921ae76918fa5f6f4450538d5d0f15e12fd8777a33fc1e748e1cd0e`  
		Last Modified: Mon, 10 Nov 2025 18:52:44 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1d99c95f37ff467400797eb14da4947a8497ba5f47bb03f93166cf504e8746`  
		Last Modified: Mon, 10 Nov 2025 18:52:50 GMT  
		Size: 76.2 MB (76156133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba4166fbbc59d72b61d706dbb5cb63a99a7360bbdc7655b4d6d2dd3facd16a`  
		Last Modified: Mon, 10 Nov 2025 18:52:45 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9f47329618cf668598857bd91fe88289c2e6b389a9f483d41bb9a144d2b2a1`  
		Last Modified: Mon, 10 Nov 2025 18:52:46 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:3372e168bd982ee48abeac46ed51eedfdb8cbe7741895ecf0b9a0851c40ffbbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb06974a5fb7f3caa30ca90c70cc968e5a99fb85cca3d6368d23e856a07db5a`

```dockerfile
```

-	Layers:
	-	`sha256:b2e364c2fb0f673fdac665f22de56d1059d66e8b5de5df949786990541ef0e6d`  
		Last Modified: Mon, 10 Nov 2025 19:37:29 GMT  
		Size: 4.3 MB (4281644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31efaf4d450716833bde7db994237bb19b9594ae554923f36149727b8c07c34`  
		Last Modified: Mon, 10 Nov 2025 19:37:29 GMT  
		Size: 31.5 KB (31531 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:c35e4a35fae34395818db823d18cf1380815454466248b5a4e2408c22a9bd46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111612331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d04c17f6b636f7b8caa733e18681a4cece12f0904d07271791f5ef942897e2a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:05 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:06 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:07 GMT
ADD file:1c921a1d937949898d3d4ba499ce8d41425fe6dd2c8fdbcddd0070f2699f05b2 in / 
# Wed, 01 Oct 2025 13:02:07 GMT
CMD ["/bin/bash"]
# Mon, 10 Nov 2025 18:44:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 10 Nov 2025 18:44:47 GMT
ENV GOSU_VERSION=1.19
# Mon, 10 Nov 2025 18:44:47 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 10 Nov 2025 18:44:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 10 Nov 2025 18:44:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 10 Nov 2025 18:44:47 GMT
ENV LANG=C.UTF-8
# Mon, 10 Nov 2025 18:44:47 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 10 Nov 2025 18:44:47 GMT
ARG MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Mon, 10 Nov 2025 18:44:47 GMT
ENV MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Mon, 10 Nov 2025 18:44:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
# Mon, 10 Nov 2025 18:53:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 10 Nov 2025 18:53:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 10 Nov 2025 18:53:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 10 Nov 2025 18:53:37 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 10 Nov 2025 18:53:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 10 Nov 2025 18:53:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 10 Nov 2025 18:53:38 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 10 Nov 2025 18:53:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:67735b72a65d308a2c2c9505d0d6e8419b7f2654a16cbd56963d88e01202d507`  
		Last Modified: Wed, 01 Oct 2025 15:43:10 GMT  
		Size: 29.9 MB (29906151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bc87e91dea23f71bb7ca9e1aff2152a49e12f71798a9d5c1c9f85a0da0e99e`  
		Last Modified: Mon, 10 Nov 2025 18:46:14 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54dc45bf33098be604405bd7ff63808ad68b310e0f33a522d568bdbf70f5bf2c`  
		Last Modified: Mon, 10 Nov 2025 18:46:15 GMT  
		Size: 5.4 MB (5443863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a2484fbf49ab14221b124d6e50bbb8cd49a8442aa2639c60e3c986a259bd37`  
		Last Modified: Mon, 10 Nov 2025 18:46:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c63e942364e51e665cdbdeb8527583536ed91dda7c15b34fcb5e36cce349c3f`  
		Last Modified: Mon, 10 Nov 2025 18:54:12 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca20401f8fa264b4df40fc737c8bd7a4235b3cc76d0a4230732d8d153087c7e`  
		Last Modified: Mon, 10 Nov 2025 18:54:18 GMT  
		Size: 76.2 MB (76248082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324643c0790a513cda1b0bfe2400a6e15115266c7c4287a34ca9697c8f50b7a4`  
		Last Modified: Mon, 10 Nov 2025 18:54:12 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395baea87dc445a94f8bd3dc86ac49bd99d33bc837af7f03c39238c8cf162118`  
		Last Modified: Mon, 10 Nov 2025 18:54:12 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:cade48a9481f5cce76dcc4724eec88f354cf8a15a2cf6f630a98257fa2d032e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc036ec6830ba5250b53dbccc011abf4eb869ab9aab913c1fa7e33f60e6b237`

```dockerfile
```

-	Layers:
	-	`sha256:e5a4b774fc74d22c05d4eb9b0aeb80d09dd7f625cf23e15ade8a87208f2de3a9`  
		Last Modified: Mon, 10 Nov 2025 19:37:34 GMT  
		Size: 4.3 MB (4275428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8bbe3ad42c65034defb0d3d2dfb9c248bcf81cf5e449fd241a53943f258915c`  
		Last Modified: Mon, 10 Nov 2025 19:37:35 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json
