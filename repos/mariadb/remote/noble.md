## `mariadb:noble`

```console
$ docker pull mariadb@sha256:81e893032978c4bf8ad43710b7a979774ed90787fa32d199162148ce28fe3b76
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
$ docker pull mariadb@sha256:196a12a494b83274fb396997a309d78cfd8809b1f78978f1877a7bccd2bc0c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104922091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d79eba61eb2baf4b8e9f31ebe28eca086a4051ed90378e5e4a09d3252c139`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
ARG RELEASE
# Fri, 14 Feb 2025 06:55:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 14 Feb 2025 06:55:09 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Feb 2025 06:55:09 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.7.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Feb 2025 06:55:09 GMT
ARG MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ENV MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Feb 2025 06:55:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2025 06:55:09 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86886c6aaa8394249d97cc0b25327592a3effc85bdac18fb2a9fdfbaec1caa`  
		Last Modified: Wed, 09 Apr 2025 01:19:12 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b221cf763a87bab4a4d9da9eafc02158d4ba0fdeb254ebf9c19a5645d5e850e`  
		Last Modified: Wed, 09 Apr 2025 01:19:12 GMT  
		Size: 5.3 MB (5349241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4180757702b359044e19a536700ff77438baa4330a86dc2a98f96eb7890140`  
		Last Modified: Wed, 09 Apr 2025 01:19:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43028b9f5f8e1b2d5ad2f7733fedcf5f7d8f23f718e71bb13d1cac3d82e86fc0`  
		Last Modified: Wed, 09 Apr 2025 01:19:12 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbef7eafa75b11cd96be469feeb7fa4aadf93a67936f1537c90bc45bdc036cfe`  
		Last Modified: Wed, 09 Apr 2025 01:19:14 GMT  
		Size: 69.8 MB (69840973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab732728101fd20d5e3c8fd2627152a03f384196976ce9246ed8ea64ac53c297`  
		Last Modified: Wed, 09 Apr 2025 01:19:12 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9f57c1bb301a7bff8311cbc4a9f79478c48697e5fdb845ba91b127c6e7b9c3`  
		Last Modified: Wed, 09 Apr 2025 01:19:13 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:3cd0368e06d8b9bf8e2ca0a24b295417cdc497b89294d3e7d53fba3f983b2764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf888ff251c7a036fbde6bc579a4cb3ff26c4c0cc8e136b361aab03a8270b722`

```dockerfile
```

-	Layers:
	-	`sha256:54dddf5585da841e39622c45830efc208fc1eabbeca54239794034b7c2a58c6b`  
		Last Modified: Wed, 09 Apr 2025 01:19:12 GMT  
		Size: 4.1 MB (4081407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e59aa4835f048c30e9d79187fe206ad1c791b13cf85d08721b86f3e252be0e`  
		Last Modified: Wed, 09 Apr 2025 01:19:12 GMT  
		Size: 31.2 KB (31228 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:cdce0831a8ddc4cf7a59f06607a99794a2476a88f4142621d3b22486b8a2e3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102868584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18697a0407bf4ea9a3c452e7a25f63404d1365d9750f0b129ae2405329e3378`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
ARG RELEASE
# Fri, 14 Feb 2025 06:55:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 14 Feb 2025 06:55:09 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Feb 2025 06:55:09 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.7.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Feb 2025 06:55:09 GMT
ARG MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ENV MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Feb 2025 06:55:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2025 06:55:09 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2634dd6770bc4cd8390f879448180a0efb3ce7fbc21d8b8431a35f7aff63f3`  
		Last Modified: Wed, 09 Apr 2025 08:29:06 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52437edb6901b3ea3dd639434f9d8b1c8be0865de0f62f7b20b186b55d9ba8a`  
		Last Modified: Wed, 09 Apr 2025 08:29:06 GMT  
		Size: 5.1 MB (5130232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abcc7eca3038e7e3ba50c5198456f694069368fbdd49f9e77e9579e57028955`  
		Last Modified: Wed, 09 Apr 2025 08:29:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48714b635922d2c48af069fa377780959135483ba7cc46803f74ccab16884264`  
		Last Modified: Wed, 09 Apr 2025 08:29:47 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c1a2d23fef36b9abd284d3100e8930cba14bbb2f885147c55fff939357bd8b`  
		Last Modified: Wed, 09 Apr 2025 08:29:50 GMT  
		Size: 68.9 MB (68877171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fffdbfe6df8c0ea12fd1171a593af266d9a09927c13d2d91121aa7b98851daa`  
		Last Modified: Wed, 09 Apr 2025 08:29:47 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3043bf49e2343a2701816962873de575b321ecc7f087bf63d69878475f00db`  
		Last Modified: Wed, 09 Apr 2025 08:29:47 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:2837cf3e723bc39e92337446cef89be3010bcbef9d2adda256bdafde8a8b0afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb52460631bafd93432d927939dab0344a3a1360fbb6308a782549da12ec7ed`

```dockerfile
```

-	Layers:
	-	`sha256:bb64be980251f4431028a542b62c0a24e1f04f51b0498342c64eacd0efa16bbb`  
		Last Modified: Wed, 09 Apr 2025 08:29:48 GMT  
		Size: 4.1 MB (4088680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5273eaac88de4d5ef9c08289310732075060a135aad0bcb3f2cf2b41fc470487`  
		Last Modified: Wed, 09 Apr 2025 08:29:47 GMT  
		Size: 31.4 KB (31440 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:759317d1cf03ddda25b84ff8967e73174fd94b382bc032f854e7b9ba4bcc9b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115051995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a740e843032f21f6bce75682ea19cfc3fd7eb98ce0f5524268d98f4656d325d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
ARG RELEASE
# Fri, 14 Feb 2025 06:55:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 14 Feb 2025 06:55:09 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Feb 2025 06:55:09 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.7.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Feb 2025 06:55:09 GMT
ARG MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ENV MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Feb 2025 06:55:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2025 06:55:09 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1556bdf84c0cfae1dbb282095b4dbc9b2a65fe74cafb5a373a64d859b6aa1c`  
		Last Modified: Wed, 09 Apr 2025 05:47:11 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f7da6fdbbd184f0815ad5e0a0049ae7327d4aeb9919a0269a2daa70c04d12c`  
		Last Modified: Wed, 09 Apr 2025 05:47:11 GMT  
		Size: 5.9 MB (5913295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e8f5cba09d5d528821591a837ee56c54343ddb67675945ed6f2a4bae059b3d`  
		Last Modified: Wed, 09 Apr 2025 05:47:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3462aa90e4a8e90b02629f65bff7268ed29cee341a8273488970e643be5187ff`  
		Last Modified: Wed, 09 Apr 2025 05:48:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d032f0fbb51aa59c058c719b7099a691fd8610166ebb42764462bbd4be112bca`  
		Last Modified: Wed, 09 Apr 2025 05:48:23 GMT  
		Size: 74.8 MB (74783598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1e2f3ae72c49d41c6bf35528d90d92f392ece8ab171cf2428d061245785edc`  
		Last Modified: Wed, 09 Apr 2025 05:48:20 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55fb2ecfb2a6a19ee80a82c18906033f6f20cfa62fb0e12767074dc0dd46f68`  
		Last Modified: Wed, 09 Apr 2025 05:48:20 GMT  
		Size: 8.4 KB (8403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:c4fb27cc6d9318704f580bbb27a4e73815482870595269da38c447c17d35d681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3634380fd050d2a8eacaf2877748227ac310af22ee816f789aa19de141c79f6`

```dockerfile
```

-	Layers:
	-	`sha256:36c1a200cc82baf3a5e631758c7bfed749ed3dba060253c155d4f61ea02790ca`  
		Last Modified: Wed, 09 Apr 2025 05:48:20 GMT  
		Size: 4.1 MB (4089160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ab986afe528b5c02fb4b03cff523366c72596b6d0f7122d8cfd1021c06f21e`  
		Last Modified: Wed, 09 Apr 2025 05:48:20 GMT  
		Size: 31.3 KB (31303 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; s390x

```console
$ docker pull mariadb@sha256:016699c0509f4c879936af382bd90916e312be1803c2c3c5112fce30094a4a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110282514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302251e27794a64a9533fa0c27ac9dd66db6f0963457f9e3b873c68a9d2b4281`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
ARG RELEASE
# Fri, 14 Feb 2025 06:55:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 14 Feb 2025 06:55:09 GMT
ADD file:8f287f40ca940c9bd87c8706751f5f1c5bbd0a83fd75f7d938832b226fdb936d in / 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Feb 2025 06:55:09 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.7.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Feb 2025 06:55:09 GMT
ARG MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ENV MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Feb 2025 06:55:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2025 06:55:09 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e5722f32c6281fa87f1e5f7ebe307864b50aa95a116496a205ce47478bc9b52c`  
		Last Modified: Tue, 08 Apr 2025 11:54:12 GMT  
		Size: 30.0 MB (29956206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e637c5dbe99438c498e511e600f72ccddb1b35b862410f714c74f64b42e08aaf`  
		Last Modified: Wed, 09 Apr 2025 05:12:30 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5816c0e949a59291930b9e06ab7db5dcab8719bbdd697eec516964a90eccf2e9`  
		Last Modified: Wed, 09 Apr 2025 05:12:30 GMT  
		Size: 5.5 MB (5482952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d0f97194f65d788a62f7113868d278733d0f2aa00aadc5a3b617ba4cf5d657`  
		Last Modified: Wed, 09 Apr 2025 05:12:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3488420a5b1f36c466d1c857bb758ecb82191ef1938a746b800cbc68351569b`  
		Last Modified: Wed, 09 Apr 2025 05:13:23 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3cc44084ae774208dac5a6e9a04a5bf1068eba54cfd1353856e6b40ee45e88`  
		Last Modified: Wed, 09 Apr 2025 05:13:25 GMT  
		Size: 74.8 MB (74829129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496727bf6c6b0f242f6c19f028cc0e4473ec7eff48a59ec2236354124bf6bcb0`  
		Last Modified: Wed, 09 Apr 2025 05:13:23 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd47c85c485aa735885616f1b6b62a981c052b859e3c45eb70cb313161c8510`  
		Last Modified: Wed, 09 Apr 2025 05:13:23 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:95c741d154dfa994f65423b5c604da1445234447aba62bf0c65a1fe0984e0363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915ca0c13bf2df994ddb8b63cc855e733727e0b516601b47bb273356d1d40abf`

```dockerfile
```

-	Layers:
	-	`sha256:3bce350600da9a71ecb58bbf20c13e13efc8ff5d5e2225eb337838e408bba3be`  
		Last Modified: Wed, 09 Apr 2025 05:13:23 GMT  
		Size: 4.1 MB (4083130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4e6aabb7c1c1c5f7a10b9459817bee263fe1f7a66350e97be3bac0bc45fdbd`  
		Last Modified: Wed, 09 Apr 2025 05:13:23 GMT  
		Size: 31.2 KB (31228 bytes)  
		MIME: application/vnd.in-toto+json
