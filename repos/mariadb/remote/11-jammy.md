## `mariadb:11-jammy`

```console
$ docker pull mariadb@sha256:416016f57f522c215d2908866e56e13e6474f071cd65112c216ba19e68f219ca
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

### `mariadb:11-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:deabcaabdf348ae8d757ca94e398bab1f42dad64173e7ad6f035f06e4fc18247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122717711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bafc7c9f19768cbf809add76a86ec037ff333f4c480e04161af087571121a5b`
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
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:11.3.2+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:11.3.2+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
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
	-	`sha256:e311a697a4031e52691ab1b5a8c325a448280fef9fc03d89dd97ab40f4245bce`  
		Last Modified: Wed, 17 Apr 2024 18:55:29 GMT  
		Size: 29.5 MB (29534028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1ba319970cfbd41b8e6306235d13983ff2c3fdc76a76e085bcdb11eda8c9ad`  
		Last Modified: Thu, 25 Apr 2024 21:51:15 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8c04c19869d890894f998882b75946eeb198c5a58b0ae4a8dfaff22bd14de2`  
		Last Modified: Thu, 25 Apr 2024 21:51:16 GMT  
		Size: 5.6 MB (5647769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83faec168fdb2d8ebc914ff36117b12aefa1eff46f01c9d89873667a5878083c`  
		Last Modified: Thu, 25 Apr 2024 21:51:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7b4e5babb3ec2efcf38ab37d1445392619d6be99c70d1100d4aee49df0e7f7`  
		Last Modified: Thu, 25 Apr 2024 21:51:16 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f06199db3ebb0b4865bc9148659ebed2bc27bd805412223b03493832123d7b`  
		Last Modified: Thu, 25 Apr 2024 21:51:18 GMT  
		Size: 87.5 MB (87521881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba9e4e742cf815ceded1ffb6f73e55c02f8dc9a6653b176c43194e69b208e22`  
		Last Modified: Thu, 25 Apr 2024 21:51:16 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424da8c2bb4fb9d2f751d48e0637674bc3916f4157412453a7b51f07495f9d5e`  
		Last Modified: Thu, 25 Apr 2024 21:51:17 GMT  
		Size: 8.3 KB (8255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:d948a534eaad55839f52257b6688dd9f1adb02ef6b16ef2aafa92299dec2f456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4610071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb26ffe39da9086a6c7d7ff78926055292405fe3db7388ba56464b842d8d932`

```dockerfile
```

-	Layers:
	-	`sha256:8188ba28f4945bdc5af9d432e0243488cbed23ee37892b69449ecdcbfb494d04`  
		Last Modified: Thu, 25 Apr 2024 21:51:15 GMT  
		Size: 4.6 MB (4578658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb52fbfde39f63fda1913dc83d28d378cff8f31a6d1e572422d93317520bbcf1`  
		Last Modified: Thu, 25 Apr 2024 21:51:15 GMT  
		Size: 31.4 KB (31413 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a5c6932b92d6102c47248efa6f8520b084349666dafa64c22648fe2b396105d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117095079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5842df754018f57542d6ccac60cd106adc2fc7b0a009463081da40b2bf8b19`
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
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:11.3.2+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:11.3.2+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
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
	-	`sha256:70104cd59e2a443b9d9a13a6bce3bbf1ae78261c4198a40bf69d6e0515abe06a`  
		Last Modified: Wed, 10 Apr 2024 19:20:55 GMT  
		Size: 27.4 MB (27359551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f16c6ce80420cf68373704936a7170998e511752d7e88d48037fcaa553e1ecf`  
		Last Modified: Tue, 16 Apr 2024 11:50:32 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49518a22b0bd0e206a5982b6ed2553414c649055e430f63816edb6b24afc6a43`  
		Last Modified: Tue, 16 Apr 2024 11:50:33 GMT  
		Size: 5.5 MB (5461352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4f68736ad1ff6519af9e17cbd7f5272ffa8bca95433b12662742b2e6b39b92`  
		Last Modified: Tue, 16 Apr 2024 11:50:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8caf34c0ab6ab2ca88fd9e134f9848124b2af1346c4895502ac23e92e29571`  
		Last Modified: Tue, 16 Apr 2024 11:51:24 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd4b67b09cf848c01d90058e54aeda1806f60de8f20b3efa0004391e5e33842`  
		Last Modified: Tue, 16 Apr 2024 11:51:26 GMT  
		Size: 84.3 MB (84260137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b4272de36fac6af1c9f0c377c6f6eb95cf4b9d667d85f93c8068d9b04ed0cc`  
		Last Modified: Tue, 16 Apr 2024 11:51:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78caa24f54f47ebaf11f65af40f146f9ac9db3bd79b1a6e910205b18c6f591a`  
		Last Modified: Tue, 16 Apr 2024 11:51:24 GMT  
		Size: 8.3 KB (8254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:f471d5b7dabe64b705c2354d56f29dd13997ca4b2f41871fe70316f81780b0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4616264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834e2b7a977843d887f0867d6a3d264b425c1495af27299ddba633575dac07e1`

```dockerfile
```

-	Layers:
	-	`sha256:55834e459dc0b0ec5ae9fa7e6940041aa950800789ee0de1d5991624e25d6f41`  
		Last Modified: Tue, 16 Apr 2024 11:51:24 GMT  
		Size: 4.6 MB (4584998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e5de8b0ce6ada557c38efad5e7406a2255627bc20d1caf93e33a8155b42c2f4`  
		Last Modified: Tue, 16 Apr 2024 11:51:23 GMT  
		Size: 31.3 KB (31266 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:145db8775a553c0808a22a8e0944def1d2c5730e5bcde8c07f79e01e804f1d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130788449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57020793b2a71a607aba680f061791b36c57d020f62039674cd5e8abbd008299`
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
ADD file:a6dad5ca890a7e93d717612d191eff2d9bbab6f9cef18c588630297bd6a61cc4 in / 
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:11.3.2+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:11.3.2+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
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
	-	`sha256:8735f03877b4ef190c5279652cd5a0a8db5ddb4170fd1fb1710abee9d2f811b1`  
		Last Modified: Wed, 17 Apr 2024 18:55:49 GMT  
		Size: 34.5 MB (34461311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c70ad7d6e03634799f516541da6fba8cd0b3fa69fc8281197bb5507ee5f4704`  
		Last Modified: Thu, 25 Apr 2024 23:10:00 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76147975155474fcc9b3236571c1ff5a666122ca0a7f1ef93002240f0534707`  
		Last Modified: Thu, 25 Apr 2024 23:10:00 GMT  
		Size: 6.1 MB (6079554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf0cbf8ceae33172414902f56988d2b960fe0e71e546a6304ce00938d5c1d55`  
		Last Modified: Thu, 25 Apr 2024 23:09:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b1ee9a80b2ef69dc53e619a8115aabc21152e62344180499d7f5d7ee3b76b2`  
		Last Modified: Fri, 26 Apr 2024 01:08:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b18ac66305288544db0b38523129fde31f67169d5405ed004f12aa1d4ec61`  
		Last Modified: Fri, 26 Apr 2024 01:08:52 GMT  
		Size: 90.2 MB (90233541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79d320957b492acc89a9fad3e923cb4676731f655af290984e01d2d89256329`  
		Last Modified: Fri, 26 Apr 2024 01:08:49 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc166eae4004feab538fa95b832508ad7022b50ec602408a6a1f6ca5da3dec8`  
		Last Modified: Fri, 26 Apr 2024 01:08:49 GMT  
		Size: 8.3 KB (8255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:a40767b268ed29f7a80da06d536e19561bd8d68cbf24c4c89ccfde8cbbd2266d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4617650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e173cdb6d0086c052cd7615bb3fcc1200c458afb353def0acdf1f719255f0a`

```dockerfile
```

-	Layers:
	-	`sha256:370b7d56209ef0a5349436ddc569eae4f8e55f93576cbbc51e9518411e7b8965`  
		Last Modified: Fri, 26 Apr 2024 01:08:49 GMT  
		Size: 4.6 MB (4586329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db8e3cf55bb8259c095e9159ea7634060303b312a6267d7ad58044a56c5267f8`  
		Last Modified: Fri, 26 Apr 2024 01:08:49 GMT  
		Size: 31.3 KB (31321 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:29a79ebd0576db7d49b14547e41a9abf254c6b821bf34b3a6a4450c04c830194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121455579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282bfb94daff1e7efa0b67c198b0877fd0341b49948dd79e5fb377d235edb521`
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
ADD file:f721f8e69988c4a423ddfb143b1001213ba52ffe029e8623c2f62e210d611fbc in / 
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 22 Feb 2024 01:03:14 GMT
ARG MARIADB_VERSION=1:11.3.2+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ENV MARIADB_VERSION=1:11.3.2+maria~ubu2204
# Thu, 22 Feb 2024 01:03:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 22 Feb 2024 01:03:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.2/repo/ubuntu/ jammy main main/debug
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
	-	`sha256:69f495792ca5ae69cb97986c54ee9f3fe805a53ca9f2f710b9ea60e20d0665ce`  
		Last Modified: Wed, 17 Apr 2024 18:55:55 GMT  
		Size: 28.0 MB (28000323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b1c470c9096af6f237ff1ec8a908622f9d7509d4ec50feb46eddafbe8c79a1`  
		Last Modified: Thu, 25 Apr 2024 21:52:37 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4620cfa1b008f5d6c7d60ace57bf5ad0c2c0a3e4f15b2382d89aaa2c74efb86b`  
		Last Modified: Thu, 25 Apr 2024 21:52:38 GMT  
		Size: 5.5 MB (5532057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472c69354b2a2463721f670678eebe21eb716dbeedd34a4f5c7e8d4ab523e9bb`  
		Last Modified: Thu, 25 Apr 2024 21:52:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb2ba5efa9ea29ab5960ac1e00f3f01c2d9cd88c1dc5c040f9bd3dfffd4b4e8`  
		Last Modified: Thu, 25 Apr 2024 23:50:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147b3720c007ec4458c9ff1ecababc8238f58635e97d536175ef7f7efea1da8c`  
		Last Modified: Thu, 25 Apr 2024 23:50:34 GMT  
		Size: 87.9 MB (87909161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b3b37e27ab0fd0ee45fe97ba311cc24b91fa5122c2de27294d5e03a1ab5d3e`  
		Last Modified: Thu, 25 Apr 2024 23:50:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f59973edba670674272be2e35655d62dd953008f082675e192af21acd474be`  
		Last Modified: Thu, 25 Apr 2024 23:50:31 GMT  
		Size: 8.3 KB (8253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:ea411bc1964dafd197a98ea24cba87a1adf9291636be396cdde31474666efe84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4586846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f94f7a14d4cadbe6d253dfb2d8c79d7275630c0ecad4582e280908bfa3679a`

```dockerfile
```

-	Layers:
	-	`sha256:21116b9362513c98eea375a90fd65a8f4272343128d46f4bc9b002da33a01288`  
		Last Modified: Thu, 25 Apr 2024 23:50:30 GMT  
		Size: 4.6 MB (4555594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0140a5ee5f298d8da8a70051d1fa67be33bd0277dea927476a2404ea8ca2dafa`  
		Last Modified: Thu, 25 Apr 2024 23:50:30 GMT  
		Size: 31.3 KB (31252 bytes)  
		MIME: application/vnd.in-toto+json
