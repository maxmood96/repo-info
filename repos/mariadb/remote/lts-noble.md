## `mariadb:lts-noble`

```console
$ docker pull mariadb@sha256:7cb913de658b7cd6c34e90f2688dd7f3193379dc9b6abadcbc521a661b7a1dee
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
$ docker pull mariadb@sha256:d1787c4e3f4f5c418b89a7a95aca77546cdc9aa4ae4321b641abe0b7a8efd536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106264529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99bc1d68744e95a503a67b3cb7b1ae7ed399e3a57a9ca6b4f696f15e388cd1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:33 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 17 Mar 2026 01:40:50 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:40:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 17 Mar 2026 01:40:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:40:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:40:50 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:40:50 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 17 Mar 2026 01:40:50 GMT
ARG MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Tue, 17 Mar 2026 01:40:50 GMT
ENV MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Tue, 17 Mar 2026 01:40:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
# Tue, 17 Mar 2026 01:40:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 17 Mar 2026 01:41:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 17 Mar 2026 01:41:05 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Mar 2026 01:41:05 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 17 Mar 2026 01:41:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:41:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:05 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 17 Mar 2026 01:41:05 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5843c951070e7c817aef864d93455c61cdfaecf5da8e7c7bd91b519348ac1bd9`  
		Last Modified: Tue, 17 Mar 2026 01:41:20 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a0e6ba478b3d58edbb53d04fcf9ad920443e5d4e6bfcac74302164db0779e3`  
		Last Modified: Tue, 17 Mar 2026 01:41:20 GMT  
		Size: 5.3 MB (5287958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c688148c30c15c24ec9d4c090247967fa410d730d350b0037d52733ab118710e`  
		Last Modified: Tue, 17 Mar 2026 01:41:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86447b1c7e20cd2c58c3dddd627f53f25f98d26d9ea94dd28a41b05726efed8a`  
		Last Modified: Tue, 17 Mar 2026 01:41:20 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943dc8eb543e7eec76735d4275a8f8e83bffedbf33c920c2dfc1d66ee7ec8e55`  
		Last Modified: Tue, 17 Mar 2026 01:41:23 GMT  
		Size: 71.2 MB (71230357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af136b8199a634efb0411cde7283939bf5ea30319f427fa0e7a89ff8c51fca9b`  
		Last Modified: Tue, 17 Mar 2026 01:41:21 GMT  
		Size: 4.0 KB (4032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7761d3ebebab336f052b318e11ef6187d23c30692d453521413317810ad8c7ee`  
		Last Modified: Tue, 17 Mar 2026 01:41:21 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:42fb9c01b25549c8dc99de0a98a1691b4fab4501f3ced58f1a5ae4c65398d409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7e18a9d4f556e8494b8ba5f09b63fe5ed8ba198e00e18ebf7950b9f45b56ce`

```dockerfile
```

-	Layers:
	-	`sha256:fbca07dac99c05ab37a5d97c8da9f33047d879de78f91611648a86cb8c2aff80`  
		Last Modified: Tue, 17 Mar 2026 01:41:20 GMT  
		Size: 4.3 MB (4273725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:163fc8c2f075dd0089323b8ae14dd968997d7f827281f5c39df6b88fc589bc87`  
		Last Modified: Tue, 17 Mar 2026 01:41:20 GMT  
		Size: 31.5 KB (31454 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:dc5c836aca504875bf6866d8e482673bba7f1e77be6a5c53bffeb8282a796a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104149681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08c32d8509fb29912b0b45ab2d2a4df0fb00cbad023a8a75d89fbd8507040e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:41:59 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 17 Mar 2026 01:42:20 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:42:20 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 17 Mar 2026 01:42:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:42:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:42:20 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:42:20 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 17 Mar 2026 01:42:20 GMT
ARG MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Tue, 17 Mar 2026 01:42:20 GMT
ENV MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Tue, 17 Mar 2026 01:42:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
# Tue, 17 Mar 2026 01:42:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 17 Mar 2026 01:42:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 17 Mar 2026 01:42:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Mar 2026 01:42:38 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 17 Mar 2026 01:42:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:42:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:42:38 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 17 Mar 2026 01:42:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d59fe63766cb641370cf5791c24825299c25ab9d9b8e57cc765740037c3928`  
		Last Modified: Tue, 17 Mar 2026 01:42:53 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541e6850181f6aaa862c6ad75a2b63ff0f6fdd90855081e57035456ddc7cf1dd`  
		Last Modified: Tue, 17 Mar 2026 01:42:53 GMT  
		Size: 5.1 MB (5098458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8bf11d74623fec6f9be8c3db35c2ca4f5f8cc68b415a5a565944ef20aa5ddd`  
		Last Modified: Tue, 17 Mar 2026 01:42:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1745acd769922b7d60736e2d1d9c194092d0678abb3c28c4dff74e7e8b4a5f`  
		Last Modified: Tue, 17 Mar 2026 01:42:53 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f401ea555ab5a53c87bf311e5d70df08fd76f264705f462c43382f0c817c0c`  
		Last Modified: Tue, 17 Mar 2026 01:42:56 GMT  
		Size: 70.2 MB (70167287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b370aa29c3f2046dbbe1374dac665b8ee6ccb0cef334ab1138895ca9a76e34f2`  
		Last Modified: Tue, 17 Mar 2026 01:42:54 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310f4d2e3a4278ebe88e280c38e4062cb4de25f68ea9d5038d73159851ec1032`  
		Last Modified: Tue, 17 Mar 2026 01:42:54 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:92b3e0a29fe892de21c9b887119584f0545ed7fd98f67e5bcae8cd960a0fe571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17595f924b4a2c230a78e41ca8f92dd61ec396b9cba2f21b7bdaeee85835e03`

```dockerfile
```

-	Layers:
	-	`sha256:b1606de439a31c576cb4a220b11f2650443d8e3ba653e05918446a4d5f507d08`  
		Last Modified: Tue, 17 Mar 2026 01:42:53 GMT  
		Size: 4.3 MB (4281002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53906f5caafa01f4745f056700bef5d2198fd9e216f83c02a9b3010152213c05`  
		Last Modified: Tue, 17 Mar 2026 01:42:53 GMT  
		Size: 31.7 KB (31667 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8cb56254b4736e77c8f003f6b226507f7fb61aee05fd1ede6132b868d327d48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116458872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d92360661833d3a1f5a2beb0ca400653a30981d928386675d215f2192c09cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:45:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 17 Feb 2026 20:46:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Feb 2026 20:46:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 17 Feb 2026 20:46:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Feb 2026 20:46:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:46:37 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 20:46:37 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 17 Feb 2026 20:46:37 GMT
ARG MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Tue, 17 Feb 2026 20:46:37 GMT
ENV MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Tue, 17 Feb 2026 20:46:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
# Tue, 17 Feb 2026 20:48:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 17 Feb 2026 20:48:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 17 Feb 2026 20:48:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Feb 2026 20:48:32 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 17 Feb 2026 20:48:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Feb 2026 20:48:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:48:33 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 17 Feb 2026 20:48:33 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d94b7553c599b2116dbd5fb33f10bf86a1399b450f560eb340b26e4b7a2afe0`  
		Last Modified: Tue, 17 Feb 2026 20:47:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040e110d00c6329b8fa98abb93d36796fb5b5a91dee24c68c4a0c454e35b499e`  
		Last Modified: Tue, 17 Feb 2026 20:47:51 GMT  
		Size: 5.9 MB (5927589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588405c93c05228b1576f3f03c252bc25f0bc698138fa5853d69c1d36b03dadc`  
		Last Modified: Tue, 17 Feb 2026 20:47:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8d415c729fee5c6fe017824be3b6f306d80efc28b0486f4d9f5e1a4064376a`  
		Last Modified: Tue, 17 Feb 2026 20:49:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37967dea4645dda2774b0e872b11a3afa5ef116822546e623adbfa7c31a33fd1`  
		Last Modified: Tue, 17 Feb 2026 20:49:13 GMT  
		Size: 76.2 MB (76210156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da546debb9942d487d8ab8591cbf2920485df10ae652e5267e51e4eb620abf5`  
		Last Modified: Tue, 17 Feb 2026 20:49:10 GMT  
		Size: 4.0 KB (4033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac680115f32b52db916c4c616b8951187abfd32e8a25a3b7fafddc48ff0ddeb1`  
		Last Modified: Tue, 17 Feb 2026 20:49:11 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:604125a5d5aee4cee0d617913f86aeaf993dd21e2f16e840fe9fdddfb451228c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b68029cb855f892a772c29928eb7b0eb387069a01912bfc3474dce1b4a99a6`

```dockerfile
```

-	Layers:
	-	`sha256:dc6fa1765cd6317be45a33a4883fe68b3e4dd43b212e771ef07b4bf3474ea499`  
		Last Modified: Tue, 17 Feb 2026 20:49:11 GMT  
		Size: 4.3 MB (4281644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2baca86b42b4305f8be2a418dea573b5e64a52631d99b2701b18c8b5ac9e8cc5`  
		Last Modified: Tue, 17 Feb 2026 20:49:10 GMT  
		Size: 31.5 KB (31530 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:8dcf9b59bd30929fc233ef2bbbf218ce347ab26b19624b557eb6b75191be1002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.7 MB (111681396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c5ba46f45328636049efc05f3f348614b781afc115f94ccca2727694f26a62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:45 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:46 GMT
ADD file:36da4c002083f47f3a54f9afaf09c1e01e856a8f55618e96eb26304b47eb72b6 in / 
# Mon, 23 Feb 2026 17:19:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 17 Mar 2026 02:34:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:34:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 17 Mar 2026 02:34:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:34:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 02:34:52 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:34:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 17 Mar 2026 02:34:52 GMT
ARG MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Tue, 17 Mar 2026 02:34:52 GMT
ENV MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Tue, 17 Mar 2026 02:34:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
# Tue, 17 Mar 2026 02:35:50 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 17 Mar 2026 02:36:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 17 Mar 2026 02:36:07 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Mar 2026 02:36:07 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 17 Mar 2026 02:36:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:36:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:36:07 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 17 Mar 2026 02:36:07 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:07785e1e3448bfcdd4a7c917fe2208c68391368db6b314a3bd60d0c083944c3b`  
		Last Modified: Mon, 23 Feb 2026 17:51:53 GMT  
		Size: 29.9 MB (29910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ac4daf3326a50b6ac078ce4f761470d5ea0b4c0e7eeb0cf2d383be614dce1`  
		Last Modified: Tue, 17 Mar 2026 02:35:30 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87634c8077a4cef954bd991ca6d3305283f09240004ab288d0c1ce2658fbaf5`  
		Last Modified: Tue, 17 Mar 2026 02:35:30 GMT  
		Size: 5.4 MB (5443692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92914b34f52e84f0bc55ca2bae4c0ddff62e3556476dbe01d3eb26142395c78c`  
		Last Modified: Tue, 17 Mar 2026 02:35:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7daf6eaf04d2857598e50eaa777855f4f51f088af1d5f1ae18deda4c06eb229`  
		Last Modified: Tue, 17 Mar 2026 02:36:34 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201c0f8a58df88e2239d9995c7eaedb1217f1f9ed56c8f1a19eaa143997ab5af`  
		Last Modified: Tue, 17 Mar 2026 02:36:36 GMT  
		Size: 76.3 MB (76313098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2644b8844b0c2ba57819616db13ff3830c91cc22bdf60179b8736c58574eef00`  
		Last Modified: Tue, 17 Mar 2026 02:36:34 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7271ee0c5f3621267ea35839c5ac12031580d3736172c73cf640e3ca2a39bb`  
		Last Modified: Tue, 17 Mar 2026 02:36:34 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:27d7d0143673ec2356880ceea85c1986d97499443a384858e7aedf8a87f3aa92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a934cf96e77d547975fd60f03922c1fb73e61340002db6818aa7a1d4c9d0dbca`

```dockerfile
```

-	Layers:
	-	`sha256:d3235c2916162a678c00a0ba7d35c0e1f23150cab290d4f721620ca0d5ec6a1f`  
		Last Modified: Tue, 17 Mar 2026 02:36:34 GMT  
		Size: 4.3 MB (4275444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0d4bf473d4014134925590510e2ec73a2819b6b791d02b1712f00138045950`  
		Last Modified: Tue, 17 Mar 2026 02:36:34 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json
