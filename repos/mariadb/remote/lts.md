## `mariadb:lts`

```console
$ docker pull mariadb@sha256:7fcb6109db2ba31b22a5709c1eaf9e84f76c9f1b9b9031ef09f24092f7f207cc
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
$ docker pull mariadb@sha256:526c15fdea2110dc8a7d007f76495d2c5e56721d2550c4e40541b8d14e0200d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108669676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f2146a0b377c9645def8c75f986110dec408c136003674192889d2eef8300a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:55:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 09 Feb 2026 19:55:47 GMT
ENV GOSU_VERSION=1.19
# Mon, 09 Feb 2026 19:55:47 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 09 Feb 2026 19:55:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Feb 2026 19:55:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:55:47 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:55:47 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 09 Feb 2026 19:55:47 GMT
ARG MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Mon, 09 Feb 2026 19:55:47 GMT
ENV MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Mon, 09 Feb 2026 19:55:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
# Mon, 09 Feb 2026 19:55:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 09 Feb 2026 19:56:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 09 Feb 2026 19:56:05 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Feb 2026 19:56:05 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 09 Feb 2026 19:56:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Feb 2026 19:56:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Feb 2026 19:56:05 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 09 Feb 2026 19:56:05 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7ac4a84e7131cf395844e5bcd2f856d9523f9d68ce448e4f85c4b032e26375`  
		Last Modified: Mon, 09 Feb 2026 19:56:17 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e30aeb2bc9609cdbccd9d77bbe5b40cf80f5180e48f11ccfc02c5570f97a56d`  
		Last Modified: Mon, 09 Feb 2026 19:56:20 GMT  
		Size: 7.7 MB (7698812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbfd20b1e946088c9232c3f8cb6f4001e7a9c9b7be833531a05eede9ee84cd8`  
		Last Modified: Mon, 09 Feb 2026 19:56:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3b999c731fc0efb64936f4656fc56ef0e429fd0cbdc7d7463f7967df2d9b92`  
		Last Modified: Mon, 09 Feb 2026 19:56:19 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fb344e911275b8c1a0b9646f9e028da91023437973069a109e929f5df0e2ae`  
		Last Modified: Mon, 09 Feb 2026 19:56:21 GMT  
		Size: 71.2 MB (71230625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724bd80f6f977d4a4ff558f766506cd6e0ab4b524613f481092bc7dab3a5611c`  
		Last Modified: Mon, 09 Feb 2026 19:56:20 GMT  
		Size: 4.0 KB (4037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919c1ef6a44a8b5b85146006212efa7b09cbe04d69a8946be3082dfebe36ad6c`  
		Last Modified: Mon, 09 Feb 2026 19:56:20 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:43731e1b978ea9fa4ec7f212b58ce143081833a50d7ccb139ca28fb837969282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87196abc081598e31ca5764bbba2dee0527bbbd6a6bd314a2fc70599e739e7d4`

```dockerfile
```

-	Layers:
	-	`sha256:335dc7f0b9d526b09c1ddf49c0128cdf2d31de0eb8b21935d24d27c79ddd15ce`  
		Last Modified: Mon, 09 Feb 2026 19:56:19 GMT  
		Size: 4.3 MB (4273709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ba44206648f2d73d5dea1181608d5a3a74238a8c12ae00a9e0fb7bf721f493a`  
		Last Modified: Mon, 09 Feb 2026 19:56:19 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:22a9e75e92eb8f4a0cb1f875ed98922cdab9c7386f4b5530172f43099e11397f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106365067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba0489760b36fd7b3d47a3ba3968da5c089bd8dacc4b84064cd68f992b63a31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:53:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 09 Feb 2026 19:53:55 GMT
ENV GOSU_VERSION=1.19
# Mon, 09 Feb 2026 19:53:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 09 Feb 2026 19:53:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Feb 2026 19:53:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:53:55 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:53:55 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 09 Feb 2026 19:53:55 GMT
ARG MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Mon, 09 Feb 2026 19:53:55 GMT
ENV MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Mon, 09 Feb 2026 19:53:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
# Mon, 09 Feb 2026 19:53:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 09 Feb 2026 19:54:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 09 Feb 2026 19:54:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Feb 2026 19:54:13 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 09 Feb 2026 19:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Feb 2026 19:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Feb 2026 19:54:13 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 09 Feb 2026 19:54:13 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 06:35:45 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1571d0166be34929ce681261f5d9a82fdf7883860407e3b5851a05d6e10c9e6`  
		Last Modified: Mon, 09 Feb 2026 19:54:29 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ece2ef3a5f988aacaa03bc9d83701fad28ca8c0c88c535c4ab4ba42311825e`  
		Last Modified: Mon, 09 Feb 2026 19:54:29 GMT  
		Size: 7.3 MB (7320108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9a15dd61f2b4cc7836cc0dde27324c883df610142bd710a5c4065a8a2e8a06`  
		Last Modified: Mon, 09 Feb 2026 19:54:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a06d856508410335ae2ab85acf8fd8b1caee3c52b52e1cedaab62e13459c272`  
		Last Modified: Mon, 09 Feb 2026 19:54:29 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d0949c1193ba1f9113df86d6df4138f5bbbe23bd437c7230f4488825790f6d`  
		Last Modified: Mon, 09 Feb 2026 19:54:33 GMT  
		Size: 70.2 MB (70166908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1983e119dd284fc118ab6046c90d6f919c34e80519e8aed2b252f1169378751b`  
		Last Modified: Mon, 09 Feb 2026 19:54:30 GMT  
		Size: 4.0 KB (4034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5e5840a4fb68649a00c23f3d754e283dbbdbf5c2bae86d16bed122e87f1f1b`  
		Last Modified: Mon, 09 Feb 2026 19:54:30 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:064b1be29f0221fda4044167ed6946a27798e7f4082c7c4bba71fdab8626cb1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45e3efc927ea8259d25520fca4e9c2b8222300b04cc667b4dc74dff825cceb8`

```dockerfile
```

-	Layers:
	-	`sha256:cdcc531e091ba13958d71c82b3608799f58dd6e66d6f74875156b37714bbacf9`  
		Last Modified: Mon, 09 Feb 2026 19:54:29 GMT  
		Size: 4.3 MB (4280986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bee382a35194587581936c6937424f4e14696bff3f326b5371f9347190441b3e`  
		Last Modified: Mon, 09 Feb 2026 19:54:28 GMT  
		Size: 31.7 KB (31667 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8cb50b98e8393c41dbe8227694ec37f156f3bc9c4488c9f6dfa20ed213390ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.1 MB (119087873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0a86bc370018626f42a2403062505a35394af172d0dacf3e46aba60a657894`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:50:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 09 Feb 2026 19:51:34 GMT
ENV GOSU_VERSION=1.19
# Mon, 09 Feb 2026 19:51:34 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 09 Feb 2026 19:51:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Feb 2026 19:51:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:51:34 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:51:34 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 09 Feb 2026 19:51:34 GMT
ARG MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Mon, 09 Feb 2026 19:51:34 GMT
ENV MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Mon, 09 Feb 2026 19:51:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
# Mon, 09 Feb 2026 19:55:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 09 Feb 2026 19:55:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 09 Feb 2026 19:55:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Feb 2026 19:55:37 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 09 Feb 2026 19:55:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Feb 2026 19:55:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Feb 2026 19:55:38 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 09 Feb 2026 19:55:38 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e465cb9a54e1e7699159cc33f01a03882245807f55f18ef53cb719757bc6f11c`  
		Last Modified: Mon, 09 Feb 2026 19:52:55 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0c19b57c8161c92150c3193ab496e7d0029f9c7550577de5be2066c20156a0`  
		Last Modified: Mon, 09 Feb 2026 19:52:55 GMT  
		Size: 8.6 MB (8557165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12e091f8859edd88af66534d86dad7b363f844be6b775788238df5e3121729f`  
		Last Modified: Mon, 09 Feb 2026 19:52:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96cf2ef31c726c73b9f1c01777747242d2ef93af4012c801eee1053d773e774`  
		Last Modified: Mon, 09 Feb 2026 19:56:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1bef66a8a72f7ae3a6ecad64c3466ed3e4a07f0bd71de0b4bf42ebba700006`  
		Last Modified: Mon, 09 Feb 2026 19:56:18 GMT  
		Size: 76.2 MB (76210325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426bcd194a074c8ceb628ea203887fa01dad21686904a83cf92e2b0dbaf0201f`  
		Last Modified: Mon, 09 Feb 2026 19:56:16 GMT  
		Size: 4.0 KB (4031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab6b9657aa5288a2295bd154a3e949da832aeffe8c9e5ba2730eff9f6c642f5`  
		Last Modified: Mon, 09 Feb 2026 19:56:16 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:a440a786b0d4b6e2bde9dcc21b9fe0cb9fe358867e02d6fb9f471109f817af03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffb9a3362635996af2ac0c3358edbe39d473585fd67888badd8224281e9a10c`

```dockerfile
```

-	Layers:
	-	`sha256:6ada04026d6bdd91e101129d84e5e034362e1949768312f5daa595929ee7659c`  
		Last Modified: Mon, 09 Feb 2026 19:56:16 GMT  
		Size: 4.3 MB (4281644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5358d621223c9c87046a6982f11816324cbe713f30ad7544d847d174f6f888c`  
		Last Modified: Mon, 09 Feb 2026 19:56:15 GMT  
		Size: 31.5 KB (31531 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; s390x

```console
$ docker pull mariadb@sha256:fb933ba6defb5aa01500408dea0e02227977fd99a405084341c56374b57eb2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113778413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdb458e00e382dda0b49e8bb5d6b58625341e000e2bb408d4a23380557c3490`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 13 Jan 2026 06:29:20 GMT
ARG RELEASE
# Tue, 13 Jan 2026 06:29:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 06:29:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 06:29:22 GMT
ADD file:55a7874afa0094b7b4c6edc68b58164a34177fa761bc6e673ddb0c846b91f26f in / 
# Tue, 13 Jan 2026 06:29:22 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:50:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Mon, 09 Feb 2026 19:51:03 GMT
ENV GOSU_VERSION=1.19
# Mon, 09 Feb 2026 19:51:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 09 Feb 2026 19:51:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Feb 2026 19:51:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:51:03 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:51:03 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Mon, 09 Feb 2026 19:51:03 GMT
ARG MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Mon, 09 Feb 2026 19:51:03 GMT
ENV MARIADB_VERSION=1:11.8.6+maria~ubu2404
# Mon, 09 Feb 2026 19:51:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
# Mon, 09 Feb 2026 19:52:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Mon, 09 Feb 2026 19:52:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.6+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.6/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Mon, 09 Feb 2026 19:52:15 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Feb 2026 19:52:15 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Mon, 09 Feb 2026 19:52:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Feb 2026 19:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Feb 2026 19:52:15 GMT
EXPOSE map[3306/tcp:{}]
# Mon, 09 Feb 2026 19:52:15 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:88318e41cf944fd93c8b2fdfaeb1378b17ed0e2440ef9811f9820449bf19a6ad`  
		Last Modified: Tue, 13 Jan 2026 06:36:13 GMT  
		Size: 29.9 MB (29909204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b998bb69c1a7641e4ec25bb345dc1875dc73ddfad6856c0ea3cf9df3de93a17`  
		Last Modified: Mon, 09 Feb 2026 19:51:45 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e882de07c6fc1297000f60bfe57f38c999227649beedca424a6ba0a00b80f80b`  
		Last Modified: Mon, 09 Feb 2026 19:51:46 GMT  
		Size: 7.5 MB (7540797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43afedd33730718eb80827ffc771cf8ba954d9caca622928639464779a4f2d8`  
		Last Modified: Mon, 09 Feb 2026 19:51:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113b153042117a5fc6553e51ba12c43f601003f316de09b49c8d512d964f900d`  
		Last Modified: Mon, 09 Feb 2026 19:52:39 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554f112ee4a643759051358750f5dd7d65cd8921e420a12cbe40d5c2cf559d29`  
		Last Modified: Mon, 09 Feb 2026 19:52:41 GMT  
		Size: 76.3 MB (76314182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9398181ce4af0822522396b8fe027dabb6d3dbc86718c3db88a1d9114ba63a2f`  
		Last Modified: Mon, 09 Feb 2026 19:52:39 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda6319d3e9ffd1fbbbfee4396af5136ee979806cdb4d205ebade51a681b7cae`  
		Last Modified: Mon, 09 Feb 2026 19:52:39 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:e2db265b773a38e87a96c56bcbd04a5c236df2bf48ad737e82e5cb5f320c1cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3959ef5a5706a0d7c4afb16f8ab73afcceafdc1fcbc41cc61a8358d50bc707bc`

```dockerfile
```

-	Layers:
	-	`sha256:3f33da3985c31e1dc37296a7e5727660f4bd3d1e3f7e568946351d685efc1935`  
		Last Modified: Mon, 09 Feb 2026 19:52:39 GMT  
		Size: 4.3 MB (4275428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e85a3913adea3f9b1c5d37c17440fccb650768c82360f3ed3a56661dc10e666`  
		Last Modified: Mon, 09 Feb 2026 19:52:39 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json
