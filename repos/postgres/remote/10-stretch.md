## `postgres:10-stretch`

```console
$ docker pull postgres@sha256:db3b8d6457c0216f966630487ed3bdb120eda674929cb09225d1e17105990abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `postgres:10-stretch` - linux; amd64

```console
$ docker pull postgres@sha256:64c74ec8a0792cbd195ea70b3c6c137c9090f3008ad98f7302e30819c3d6673b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73216604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b3684d8af20ad3274cef12538a7dcaf624653f00ae79e1110a6b4d7b9c51ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:17 GMT
ADD file:55a25b93e8f2940a796f3cbf1e78bddf5f49c46b1b89b63b9b5673cbed9483ca in / 
# Thu, 22 Jul 2021 00:47:17 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 14:31:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 14:31:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Jul 2021 14:31:12 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 14:31:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 14:31:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 22 Jul 2021 14:31:30 GMT
ENV LANG=en_US.utf8
# Thu, 22 Jul 2021 14:31:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 14:31:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 14:31:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jul 2021 14:32:59 GMT
ENV PG_MAJOR=10
# Thu, 22 Jul 2021 14:32:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Thu, 12 Aug 2021 21:08:23 GMT
ENV PG_VERSION=10.18-1.pgdg90+1
# Thu, 12 Aug 2021 21:08:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 12 Aug 2021 21:08:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 12 Aug 2021 21:08:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 12 Aug 2021 21:08:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Aug 2021 21:08:41 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 12 Aug 2021 21:08:41 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Aug 2021 21:08:41 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 12 Aug 2021 21:08:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 12 Aug 2021 21:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 21:08:43 GMT
STOPSIGNAL SIGINT
# Thu, 12 Aug 2021 21:08:43 GMT
EXPOSE 5432
# Thu, 12 Aug 2021 21:08:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:778066204fb734c2fb80cb8127cb35d67d742806a4eaf1aba0b5393c4ae6f2a4`  
		Last Modified: Thu, 22 Jul 2021 00:53:22 GMT  
		Size: 22.5 MB (22527428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df352e90091835ab15cb7cd3ae712c4ecbd0daa3864bbc2ca70e4f28bf4f6dd6`  
		Last Modified: Thu, 22 Jul 2021 14:37:15 GMT  
		Size: 4.5 MB (4503278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7242d94fa186f60db358fd064070674670a6acb577a32c93dcc8df0d0860654`  
		Last Modified: Thu, 22 Jul 2021 14:37:13 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7583c6f085605f2363722eb29362108c1cd0e60864fff4e81b3942f2bf851a9e`  
		Last Modified: Thu, 22 Jul 2021 14:37:13 GMT  
		Size: 1.4 MB (1412232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb70ff3ea1b261740c31e0ab8094435550788236944d2434f27aab5120bf52f0`  
		Last Modified: Thu, 22 Jul 2021 14:37:12 GMT  
		Size: 6.2 MB (6185332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1409f9a52f605433ec11cbd356af74a8a9460ae885627aa7a8864a38e833c39`  
		Last Modified: Thu, 22 Jul 2021 14:37:10 GMT  
		Size: 385.0 KB (385044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174aa3d8763d4730994bad279acf14b0e9e828d2e56c05f9bbf973ec84c4bcb2`  
		Last Modified: Thu, 22 Jul 2021 14:37:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee06562012c00927910aafb53ec4573356ff17cba25a82072dfc929cc88aa658`  
		Last Modified: Thu, 22 Jul 2021 14:37:10 GMT  
		Size: 5.3 KB (5340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b614e8e8be45bdf4e16543cd6178f3d501ae7919316ef32a3f92de5f34ef725e`  
		Last Modified: Thu, 12 Aug 2021 21:25:01 GMT  
		Size: 38.2 MB (38183058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c546eec1a39c1d28c4f08f8dc1fce6c11b032c5039728a2f0d2c84b33ebb569`  
		Last Modified: Thu, 12 Aug 2021 21:24:50 GMT  
		Size: 8.1 KB (8076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44634d9e2b3b4cdbccbc51edb19ef44d9948ba2de92252467897afe9802dfc12`  
		Last Modified: Thu, 12 Aug 2021 21:24:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4245fb67e6469b66e98a295774cf912e076a32b5a516f9cf316fab10ec29bb`  
		Last Modified: Thu, 12 Aug 2021 21:24:50 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edf5ebe04b571696054fbfa9a10063d041e0f713a1e1d175bc63e0ea77dcfaa`  
		Last Modified: Thu, 12 Aug 2021 21:24:50 GMT  
		Size: 4.4 KB (4411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9909801b8dcb06072c8a61de9c69caf9307e9632183b633bf62a1fdbfcec39d`  
		Last Modified: Thu, 12 Aug 2021 21:24:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; arm variant v5

```console
$ docker pull postgres@sha256:d2096ebb240e25cb20d204e133d6b034e5f3822abd73b0807ba37a5acf4bb94b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70168668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f2a2f8c3737fcff95f0927919c5165ac020a490d4e3916543971d61d21a100`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Jul 2021 00:53:35 GMT
ADD file:15b3f2121b39bbc6e8b5dae83180128e0dbf1c86ea4d9f81533ed493efcc6dc8 in / 
# Thu, 22 Jul 2021 00:53:36 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:42:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 09:42:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Jul 2021 09:42:19 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:42:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:43:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 22 Jul 2021 09:43:12 GMT
ENV LANG=en_US.utf8
# Thu, 22 Jul 2021 09:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:43:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:43:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jul 2021 10:34:10 GMT
ENV PG_MAJOR=10
# Thu, 22 Jul 2021 10:34:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Thu, 22 Jul 2021 10:34:11 GMT
ENV PG_VERSION=10.17-1.pgdg90+1
# Thu, 22 Jul 2021 11:00:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 22 Jul 2021 11:00:04 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 22 Jul 2021 11:00:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Jul 2021 11:00:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Jul 2021 11:00:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Jul 2021 11:00:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Jul 2021 11:00:09 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 22 Jul 2021 11:00:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Jul 2021 11:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 11:00:11 GMT
STOPSIGNAL SIGINT
# Thu, 22 Jul 2021 11:00:12 GMT
EXPOSE 5432
# Thu, 22 Jul 2021 11:00:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7900ccce3a65cf4889d5e7618644bba320a4667d14e5987da7b26a95ccc8e1f3`  
		Last Modified: Thu, 22 Jul 2021 01:07:10 GMT  
		Size: 21.2 MB (21204360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cda63bf4fa55dbf5e11a5561144d3dc0d6dba3216bb7e2c434651de5b00f3d8`  
		Last Modified: Thu, 22 Jul 2021 12:01:45 GMT  
		Size: 4.2 MB (4238903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c36e2da49bff3f1e53f3421863982bf0ad3fbd476512c08d9cf1f736f5b46ba`  
		Last Modified: Thu, 22 Jul 2021 12:01:42 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771ba66ca9e34e9d9e187c90b608ea215a319af89e305a1b2f4af1e0719d7a07`  
		Last Modified: Thu, 22 Jul 2021 12:01:42 GMT  
		Size: 1.4 MB (1371520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8b78aa31b67432bfab47e666c9f881bee5c1f6ca6231145c7fdf57217cf7af`  
		Last Modified: Thu, 22 Jul 2021 12:01:44 GMT  
		Size: 6.2 MB (6185674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc54d5f76ef9b63aa686908ec777bcd60a6f22ebd059ee25e851fb2f9eaff79c`  
		Last Modified: Thu, 22 Jul 2021 12:01:40 GMT  
		Size: 385.1 KB (385074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2dc3ffa79a558ed51c2e08723127cb58d42dd1f51761c8fc5394cfb451aa63`  
		Last Modified: Thu, 22 Jul 2021 12:01:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049a65478343a3353a505350aabbe4091a0834d3623b7b6ab95839a4e69b1733`  
		Last Modified: Thu, 22 Jul 2021 12:01:40 GMT  
		Size: 5.3 KB (5343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122712505fc5d44f43bdf2007e4238de88b528ccf364a0cc5632da74ebaf25ad`  
		Last Modified: Thu, 22 Jul 2021 12:03:21 GMT  
		Size: 36.8 MB (36762906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d610ae21dd5354e1695fa3d0be49ade3493ee236e0e990c488a568556feac28`  
		Last Modified: Thu, 22 Jul 2021 12:03:04 GMT  
		Size: 8.1 KB (8078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739ebaf22b8dcc1952bad854adb899550533739ced6453149e508ac59cb0d2f7`  
		Last Modified: Thu, 22 Jul 2021 12:03:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb3a0fd674cf345feae1bc49e3ea62a4514e995fd2c01cf74a9026ccbbca020`  
		Last Modified: Thu, 22 Jul 2021 12:03:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ef22a1213a639b4426d31c76438b83971d8689bfdb940b7f7338c0fa513dba`  
		Last Modified: Thu, 22 Jul 2021 12:03:04 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739a98e47c02acb67bb71c50651bc122cf5833c545e877f1a3bf616442963050`  
		Last Modified: Thu, 22 Jul 2021 12:03:04 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; arm variant v7

```console
$ docker pull postgres@sha256:91ecdb00655627588f0ea1fb0e7552541ba6f6d221f591f045f86c43d2cd7462
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66845996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fee72fc361c9c181127f2fb6147a3bb1c8d326c644aaeb456c6a96a67f2ba1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 19:07:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 19:07:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Jul 2021 19:07:38 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 19:08:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 19:08:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 22 Jul 2021 19:08:22 GMT
ENV LANG=en_US.utf8
# Thu, 22 Jul 2021 19:08:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 19:08:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 19:08:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jul 2021 19:54:09 GMT
ENV PG_MAJOR=10
# Thu, 22 Jul 2021 19:54:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Thu, 22 Jul 2021 19:54:10 GMT
ENV PG_VERSION=10.17-1.pgdg90+1
# Thu, 22 Jul 2021 20:17:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 22 Jul 2021 20:17:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 22 Jul 2021 20:17:18 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Jul 2021 20:17:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Jul 2021 20:17:21 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Jul 2021 20:17:21 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Jul 2021 20:17:22 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 22 Jul 2021 20:17:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Jul 2021 20:17:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 20:17:26 GMT
STOPSIGNAL SIGINT
# Thu, 22 Jul 2021 20:17:26 GMT
EXPOSE 5432
# Thu, 22 Jul 2021 20:17:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c6fcff359f3de9514e72ca488952426c54c4ce239cb7b5415418b305f60ad2`  
		Last Modified: Thu, 22 Jul 2021 21:10:40 GMT  
		Size: 3.9 MB (3875061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890c07da5f3efcde00bdf37349e3349072e67eb60607f3d49e2971e1814ee066`  
		Last Modified: Thu, 22 Jul 2021 21:10:38 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770a54c0ef462a12987a55a63e202618039d4c26bc887e03c48b0bdf876d7b6c`  
		Last Modified: Thu, 22 Jul 2021 21:10:38 GMT  
		Size: 1.4 MB (1363908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff5c52e5dacde980dbc67dbfc282e3456601d5d41e2aabffa4d11de9db58feb`  
		Last Modified: Thu, 22 Jul 2021 21:10:40 GMT  
		Size: 6.2 MB (6185649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671d01e209eb2951c73879fa238e59e532f7c565a2ccc29f07f1d507512dac10`  
		Last Modified: Thu, 22 Jul 2021 21:10:36 GMT  
		Size: 379.2 KB (379215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb683b31afbe93430529bf13371ef06c54bf7dd13b0b49d21448eaf65f3caecc`  
		Last Modified: Thu, 22 Jul 2021 21:10:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e3fc255c9d279cae83ec48746a0f7b556aafe728367c73495374131b5278d1`  
		Last Modified: Thu, 22 Jul 2021 21:10:36 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cec0aaa0ca243484823001284dd2707a11ac927ce16caa6299014786f745517`  
		Last Modified: Thu, 22 Jul 2021 21:12:26 GMT  
		Size: 35.7 MB (35706528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a72f6cbef32ef737965447f1be0ffc5efe059d6fad1d0a3e871071c9257093`  
		Last Modified: Thu, 22 Jul 2021 21:12:00 GMT  
		Size: 8.1 KB (8073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017e8eeeb74450edb8f0abfbea3eabd2255870b09efabf450f840906d015aa00`  
		Last Modified: Thu, 22 Jul 2021 21:12:00 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a46909ff4ca66b91052dd56f9b3578503082482dc05e1bb14df621116f25114`  
		Last Modified: Thu, 22 Jul 2021 21:12:00 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d86aacda376d78ad97493e0c993031188f5a894b2fdc9248f7afdce2634459`  
		Last Modified: Thu, 22 Jul 2021 21:12:00 GMT  
		Size: 4.4 KB (4413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e59b8aa248de1c29f460338aade4b99dcddb4be084dceca9e54955aff8053e`  
		Last Modified: Thu, 22 Jul 2021 21:12:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c1af400e101dc6d0a832ff297343b431785e87a1a8e20e0c84df0db17ae0ac97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69454223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c660f84089715bd60b5b55e91c64d236e0c67394fe15cafeed5f2871fb951b66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:40 GMT
ADD file:b39a01b3af7a531df3592571b7f6eaa7efd20919858f7f0cd2ddf1c1eceb078d in / 
# Thu, 22 Jul 2021 00:41:40 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:40:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 09:40:39 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Jul 2021 09:40:39 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:40:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:40:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 22 Jul 2021 09:40:57 GMT
ENV LANG=en_US.utf8
# Thu, 22 Jul 2021 09:41:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:41:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:41:04 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jul 2021 09:51:01 GMT
ENV PG_MAJOR=10
# Thu, 22 Jul 2021 09:51:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Thu, 22 Jul 2021 09:51:01 GMT
ENV PG_VERSION=10.17-1.pgdg90+1
# Thu, 22 Jul 2021 10:00:15 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 22 Jul 2021 10:00:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 22 Jul 2021 10:00:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Jul 2021 10:00:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Jul 2021 10:00:18 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Jul 2021 10:00:18 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Jul 2021 10:00:18 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 22 Jul 2021 10:00:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Jul 2021 10:00:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 10:00:19 GMT
STOPSIGNAL SIGINT
# Thu, 22 Jul 2021 10:00:19 GMT
EXPOSE 5432
# Thu, 22 Jul 2021 10:00:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9e7a560784c85cb9624bff5b6e479fbb95d5e265873987014f8aec75d509a530`  
		Last Modified: Thu, 22 Jul 2021 00:48:50 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2ea70ae1349e65ef7f4c202983fdac20725963e6553d90d47314763af2bad7`  
		Last Modified: Thu, 22 Jul 2021 10:15:58 GMT  
		Size: 4.1 MB (4078612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990f21505e76c417e57578cbd45788834b4a6564c31d083382d3ae3021683eab`  
		Last Modified: Thu, 22 Jul 2021 10:15:55 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6eb4c48cee0dc2c97838784c8a8931b13ad046b1c7cabdb8ba0f3e403cfe1a`  
		Last Modified: Thu, 22 Jul 2021 10:15:56 GMT  
		Size: 1.3 MB (1347053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921e205dc33a1123a9efe26b403b66eaa8b20c85afed7b0006a71ce43518b7cb`  
		Last Modified: Thu, 22 Jul 2021 10:15:54 GMT  
		Size: 6.2 MB (6185360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3d9d49dce3da3f02acb710ead740036d82c536de532eb174f783d60035b8a4`  
		Last Modified: Thu, 22 Jul 2021 10:15:53 GMT  
		Size: 377.9 KB (377896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cdb549cee5bb00e285164800948b3042a4800f853a8681061cd39da10e88d1`  
		Last Modified: Thu, 22 Jul 2021 10:15:52 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ff2b4166363f21639ac816840d22426af54adb1b88a835ba921fdecc0ee309`  
		Last Modified: Thu, 22 Jul 2021 10:15:52 GMT  
		Size: 5.3 KB (5338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bdf23ee54c5bacabb1c41b0c85cd723411b13ba2cbf981e5b44a9a7e62535d`  
		Last Modified: Thu, 22 Jul 2021 10:17:13 GMT  
		Size: 37.1 MB (37055646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b314285f8f4b8feebb801fd9f55b9ffb0fc2e273ccbcfea50262a1185b3afeba`  
		Last Modified: Thu, 22 Jul 2021 10:17:02 GMT  
		Size: 8.1 KB (8073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0389efe033cde7f2152110cec53ba6602f15a3114f070d0a983dcef8f45f1ad`  
		Last Modified: Thu, 22 Jul 2021 10:17:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ddc1b11324a94a329a9bbaca8c39ed7a5953e5c154897cc26e1875a56ab237`  
		Last Modified: Thu, 22 Jul 2021 10:17:05 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d713d98f9c7187856c35ad44182d7f7d3b8904657e9c122be7934d6d78c01b8`  
		Last Modified: Thu, 22 Jul 2021 10:17:04 GMT  
		Size: 4.4 KB (4409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409912a4ed3c4a09c175f6158b648a0cf9086bd778481f9bc252f03441b3b0ba`  
		Last Modified: Thu, 22 Jul 2021 10:17:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; 386

```console
$ docker pull postgres@sha256:5cabe5c67ea1e6018d7d10b7af072f941c9a993b9dbf3be12bf9416f8c2b3f8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74383157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea56ed1d64ae33f3bc23256287fe9315b97a0cadfe5ba97e3d0dc30a822bb9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:45 GMT
ADD file:031e0099f6d9f77a3c2cc04e510e38072e1deb4394692b02cee9689e30a4286a in / 
# Thu, 22 Jul 2021 00:41:45 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 12:20:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 12:20:42 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Jul 2021 12:20:42 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 12:21:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 12:21:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 22 Jul 2021 12:21:15 GMT
ENV LANG=en_US.utf8
# Thu, 22 Jul 2021 12:21:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 12:21:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 12:21:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jul 2021 12:23:03 GMT
ENV PG_MAJOR=10
# Thu, 22 Jul 2021 12:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Thu, 12 Aug 2021 21:17:53 GMT
ENV PG_VERSION=10.18-1.pgdg90+1
# Thu, 12 Aug 2021 21:18:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 12 Aug 2021 21:18:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 12 Aug 2021 21:18:19 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 12 Aug 2021 21:18:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Aug 2021 21:18:21 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 12 Aug 2021 21:18:21 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Aug 2021 21:18:22 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 12 Aug 2021 21:18:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 12 Aug 2021 21:18:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 21:18:24 GMT
STOPSIGNAL SIGINT
# Thu, 12 Aug 2021 21:18:25 GMT
EXPOSE 5432
# Thu, 12 Aug 2021 21:18:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:92ef0ad3e2e4c31244fba7bdf4771ee5d90b4a815d9ac530ac555e1b83dc93d8`  
		Last Modified: Thu, 22 Jul 2021 00:49:52 GMT  
		Size: 23.2 MB (23156226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95132cbc6863102e5fd85a33bbd5e3be66f26a160e052840d82ef9fe46605863`  
		Last Modified: Thu, 22 Jul 2021 12:31:13 GMT  
		Size: 4.8 MB (4811214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284aecc663b6543f0fa8a030550fa808b76607ff2c5b92b56c73d026db0862d5`  
		Last Modified: Thu, 22 Jul 2021 12:31:10 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdfa7ac24e51401cd24b16962318da57696d3afdcb83f89e8b7c931a309da18`  
		Last Modified: Thu, 22 Jul 2021 12:31:10 GMT  
		Size: 1.4 MB (1382580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b616fbc560270aedffeb6f38c552f60248af321144e5fcb9a45490313915c5`  
		Last Modified: Thu, 22 Jul 2021 12:31:13 GMT  
		Size: 6.2 MB (6185559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4530f3ac3001e753c71d9dc9a0a566becb339c1c6a743757728455ba0ecf13c4`  
		Last Modified: Thu, 22 Jul 2021 12:31:07 GMT  
		Size: 393.3 KB (393334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7093b2162ad33c4a5d004fea1a4526b9995848c2217ca37e12325f69ca17605`  
		Last Modified: Thu, 22 Jul 2021 12:31:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b8dfe581b58a39f2b12e58ba104683342fe8cbcbe608c93268c8bb7b2bf2e`  
		Last Modified: Thu, 22 Jul 2021 12:31:07 GMT  
		Size: 5.3 KB (5343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6d798e6505a57275397f3a3806ac235c28c94c05a4647d5d55ea51780e87c0`  
		Last Modified: Thu, 12 Aug 2021 21:35:25 GMT  
		Size: 38.4 MB (38434017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e6fc5c385fe49f98f1838159ae1dff4e85090de9ffa1dedfe6055a29d92b1e`  
		Last Modified: Thu, 12 Aug 2021 21:35:14 GMT  
		Size: 8.1 KB (8073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea0115ac2550ef28fce30a82965e78b3398998cccf8eb34bb23c562bf6a941a`  
		Last Modified: Thu, 12 Aug 2021 21:35:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8fe16d95284ae658d2022b92d32f4ba89073c691e1a3105cbc102cd9187d4`  
		Last Modified: Thu, 12 Aug 2021 21:35:14 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59a3e4df5dba224160ed1da70498317970c176f5d91d1a99a207ecc1a7657f4`  
		Last Modified: Thu, 12 Aug 2021 21:35:13 GMT  
		Size: 4.4 KB (4411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2374150c200aea144fe82856b9723889648609f6e28aa3528e9e68c0257e2e0`  
		Last Modified: Thu, 12 Aug 2021 21:35:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
