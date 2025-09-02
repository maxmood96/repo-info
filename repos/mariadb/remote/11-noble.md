## `mariadb:11-noble`

```console
$ docker pull mariadb@sha256:ec5d50f32359ff020b93cce6834f9bf89147c34aea0e90c952ccf556c94a4fb8
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
$ docker pull mariadb@sha256:f29244e9757d7773c043dbacf95e515ba5b6c7aa26fc78af55a5d79b6399b03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105290189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b9e7bfd1d0aae3cd23df7f61d8a357a8ad5e79a5df5dc4802fd4a2f1a70cf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 07:40:04 GMT
ARG RELEASE
# Fri, 08 Aug 2025 07:40:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 07:40:04 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:11.8.3+maria~ubu2404
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:11.8.3+maria~ubu2404
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af53108b48762c40cbbc48754aa5232fb050eee40a8cf8fdc19940e891ae7b6`  
		Last Modified: Tue, 02 Sep 2025 00:25:05 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62e588404190760b2679fcc3bb5958f8d8cd0fad4d7dc14a399b0c7ab4b98e1`  
		Last Modified: Tue, 02 Sep 2025 00:25:10 GMT  
		Size: 5.3 MB (5349704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b2e80811b0fb2125ad93b340d310ea2246268fb114684531ecc878632c0d1c`  
		Last Modified: Tue, 02 Sep 2025 00:25:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1b9d7bf084db0d91b44d929afa29753611c65b5faaea5bb7ac35874d876aa1`  
		Last Modified: Tue, 02 Sep 2025 00:25:05 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4ad17fe8b28a1591542ca42341bb69243275836546d9d4c2ee66311aba5de5`  
		Last Modified: Tue, 02 Sep 2025 00:25:14 GMT  
		Size: 70.2 MB (70203192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49490fb213ce4f780e55f394e59c109744855b396c4574780557fd583a67bdae`  
		Last Modified: Tue, 02 Sep 2025 00:25:05 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d36f1aabe2cb313dbfae70196d660eacdfd4f4d19a73149e3a4ad9fad6e001`  
		Last Modified: Tue, 02 Sep 2025 00:25:06 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:7031443354d39f0dd5effcbc2116a8c2370f207f0a64a0b7f152f6f2b6983515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fdf35d0ae184e6158b49505df8741401d24a5d92e42e5f536eb0ead50fbf31`

```dockerfile
```

-	Layers:
	-	`sha256:7f3d5386421b19d0cd5475bce38fc5ceb29a27e9ec343281d7ac840097be886f`  
		Last Modified: Tue, 02 Sep 2025 00:36:00 GMT  
		Size: 4.3 MB (4263645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c194ad5337d8d20583fe5f8ae59de9f96346e8fdecb927523e7739281add152`  
		Last Modified: Tue, 02 Sep 2025 00:36:01 GMT  
		Size: 31.2 KB (31230 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:14aa81ddf2311d8a63e2dd36b664224bb47f0000f51e5769a06df44fb467bdcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103226826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad14918eb0f40960629894fa24b2991969f70a22670e9bcf6fc939d44530d5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 07:40:04 GMT
ARG RELEASE
# Fri, 08 Aug 2025 07:40:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 07:40:04 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:11.8.3+maria~ubu2404
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:11.8.3+maria~ubu2404
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc2eddb6a6b2ee6f31d327a7b24ebc53d91b4a5da735d30388e1e6b19e6dcd5`  
		Last Modified: Tue, 02 Sep 2025 02:22:41 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fa34e3a4b1118ee9a724506c3e2b13476b292d51b170273bbcecdfa2f5f4a6`  
		Last Modified: Tue, 02 Sep 2025 02:22:42 GMT  
		Size: 5.1 MB (5130799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c685877590ed908fd0b60a12b7ccab73fe6ca696447a8622b37f46dda15e0da1`  
		Last Modified: Tue, 02 Sep 2025 02:22:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e40ada8cd44eb1f3b47e7e880c3355f0470efd1203950638ddc0b06253c4b8a`  
		Last Modified: Tue, 02 Sep 2025 02:23:49 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca6de211d35d5da436bf8ae22889664c57c39fa0682825129976f305fccc911`  
		Last Modified: Tue, 02 Sep 2025 02:23:55 GMT  
		Size: 69.2 MB (69221553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c2c13bab8684339623ceeda32745adaecbf54364b266310fb6449c852fa735`  
		Last Modified: Tue, 02 Sep 2025 02:23:50 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbdf96c23d5985c5ea9d4519502ebc5250f6d1d6c1ae44d2203eb30f7f5f42b`  
		Last Modified: Tue, 02 Sep 2025 02:23:50 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:0befeab6a1d70e51e4f47b9c00ed3eefdf1eab011a101aa07c5ed93fd4f82424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e5526deb66d25d8ff914bc7920d3f86c3e06dcdf1919e6e3567a0c56a97b1e`

```dockerfile
```

-	Layers:
	-	`sha256:7176d92134ec7b22522a5341af65bfdd0c5a3b649e6aaab1c1a949b0fb9425f5`  
		Last Modified: Tue, 02 Sep 2025 03:36:06 GMT  
		Size: 4.3 MB (4270920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c771376706afe0671c7404fcd1951d05cd6c141732f644f8d141df0148965280`  
		Last Modified: Tue, 02 Sep 2025 03:36:07 GMT  
		Size: 31.4 KB (31442 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2010bf9a1f5780b7b26cad97eb505453f83f4f4e4463b13f81d51a0352de880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115428604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f22433b286e5cd96b06db52641c5f513391b15cccfc17875bdb5f94fa919f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 07:40:04 GMT
ARG RELEASE
# Fri, 08 Aug 2025 07:40:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 07:40:04 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:11.8.3+maria~ubu2404
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:11.8.3+maria~ubu2404
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298d2feab47ffce3d72163667c5f53a68043d5d0fa58c736ce4116499eba7ad3`  
		Last Modified: Tue, 02 Sep 2025 01:09:04 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866227cbb6fef9a46a4f11a4b73540c211c9996e777fe6120b21999f6edad42d`  
		Last Modified: Tue, 02 Sep 2025 01:09:05 GMT  
		Size: 5.9 MB (5914247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2644f57b02a3cec77b8771269b3cc2fe48d7d108d528d1c106db2716d128c`  
		Last Modified: Tue, 02 Sep 2025 01:09:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422291c112020386c7f8274c1e13c055eed9cde27ef30d00245f8c14eecd8a9a`  
		Last Modified: Tue, 02 Sep 2025 01:11:55 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d75e51a2cedf37957b63c165c5b01370371f7f2524423ef7a48828dace4474`  
		Last Modified: Tue, 02 Sep 2025 01:12:04 GMT  
		Size: 75.2 MB (75170578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cb274b5973a3de1dfe771b7048243a73be39fe8a17c8050aeefbd1c0a1d25f`  
		Last Modified: Tue, 02 Sep 2025 01:11:56 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1e0c2fce45df56c43d933133892d2c060dd8dffdc5eed4eb59be125c35d9b2`  
		Last Modified: Tue, 02 Sep 2025 01:11:56 GMT  
		Size: 8.4 KB (8404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:377b506ceb4b0818f6c00d57d38f18fb340828731026a18bcf010c4f52bd84f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d7b28195cc045f34cd98a5186077bd65d6f16f1ee8f86f61ebcb84d4168dce`

```dockerfile
```

-	Layers:
	-	`sha256:ea09b83fe0c345caf35e4767ddacb2a7ef9b513b0a4ca6c8eae443d3ba8ed236`  
		Last Modified: Tue, 02 Sep 2025 03:36:12 GMT  
		Size: 4.3 MB (4271566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:982c9d1cab2cdf3659730aa48debd44af0478c70b5ce0dd4114d3b06f06d5c71`  
		Last Modified: Tue, 02 Sep 2025 03:36:13 GMT  
		Size: 31.3 KB (31306 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:a83a71b2870ad5eef03300cf4522a546230729c1603567e6a5d305e7a97aff6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110689396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920fd647bc36d41c494ab7f221a0fc19e83271b8b2516631ae738431cbd314c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 08 Aug 2025 07:40:04 GMT
ARG RELEASE
# Fri, 08 Aug 2025 07:40:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 08 Aug 2025 07:40:04 GMT
ADD file:9c3c50a7bf89c14623163f11927acdf7c8624c7519f83f2d95bf5a99ea4d21f9 in / 
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:11.8.3+maria~ubu2404
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:11.8.3+maria~ubu2404
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:80a64b6a7d961af355cc1a24ce954958de51e8bc2fb336684c1fbec689663c29`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 29.9 MB (29933009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf93632914626a13b53d8b83b1ce61591921683e85f33c9fb3326e0f42cdb59`  
		Last Modified: Mon, 01 Sep 2025 23:56:55 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fb334e6f3edff4e40e75c72b4fe57843061dda6115d4dbcafa3d04e01c9a5f`  
		Last Modified: Mon, 01 Sep 2025 23:57:01 GMT  
		Size: 5.5 MB (5483292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3398717d7912bfec9fce0dca2e762f88b47138f4d12746a5978f5c8ecc753943`  
		Last Modified: Mon, 01 Sep 2025 23:56:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a308994843f39c5b7017b9e70198aa5d03fd0289e811d474a514cdfd8cc1f0d`  
		Last Modified: Mon, 01 Sep 2025 23:58:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a1532ce3ec2dda0229b51484f326e998a9420bd150af7146bcb275d6d6e924`  
		Last Modified: Mon, 01 Sep 2025 23:59:05 GMT  
		Size: 75.3 MB (75258860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1e7860ebe03e85bd890ac771bc3bc8d293ac6d0259db74f34ab0b6f0bf63d`  
		Last Modified: Mon, 01 Sep 2025 23:59:00 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00f199400a780921464d82ae85f720d1101aac0741ccff4e128a20419ffd24b`  
		Last Modified: Mon, 01 Sep 2025 23:59:01 GMT  
		Size: 8.4 KB (8402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:a315b1c6d147f7a8a5d2da0f34fbe5b2b553ea6b2487e79c91b616302325b2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fbe4e00ffe100b25a682f14dd50d02d8e2eb7e8324f4d5dd21a91aed18cdd0`

```dockerfile
```

-	Layers:
	-	`sha256:3c9bc3bff8157e158688783446617b82223361fce136b2b86e8aebd74dac849e`  
		Last Modified: Tue, 02 Sep 2025 00:36:14 GMT  
		Size: 4.3 MB (4265366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eca18e0a0a8197e67cd0d282bc41f8807eea0e58529cd665370f888c137a5f23`  
		Last Modified: Tue, 02 Sep 2025 00:36:14 GMT  
		Size: 31.2 KB (31229 bytes)  
		MIME: application/vnd.in-toto+json
