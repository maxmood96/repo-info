## `postgres:18-trixie`

```console
$ docker pull postgres@sha256:84d31be2cfa1d6f07907ca4f397468a351e660cf52f1223302e66e789244c372
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:18-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:99f4a559071bd10d96575f5dc43b15e4bc3cf3ca4686c329564dedf4bbbb6512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162288643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439543311e0c6ae220dfa0572ae04de0e0556ddc4b86eeb28fc878210ddf98b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:03:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:03:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:50 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:03:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:03:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:03:54 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:03:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:03:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:03:58 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:03:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 12 Feb 2026 21:03:58 GMT
ENV PG_VERSION=18.2-1.pgdg13+1
# Thu, 12 Feb 2026 21:04:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:04:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:04:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:14 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:04:14 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:04:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:04:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:04:15 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:04:15 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:04:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659362c5a0b7c289982c72f8a617f284fbaa531184a7ace6ddde01cb18606cff`  
		Last Modified: Thu, 12 Feb 2026 21:04:35 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde5569f086be0615cb1e4e366973040394f930caea72cc33a1e112424c07ef8`  
		Last Modified: Thu, 12 Feb 2026 21:04:36 GMT  
		Size: 6.4 MB (6437937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f633039419970f7febb88e5206b7f4a3535110ef65991be6a24b328e9feb1f`  
		Last Modified: Thu, 12 Feb 2026 21:04:35 GMT  
		Size: 1.3 MB (1256761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777cc89ca451e3286deb4ac5d68df1c494600c403aaf4cca2abed1bbf523fd95`  
		Last Modified: Thu, 12 Feb 2026 21:04:36 GMT  
		Size: 8.2 MB (8203805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3892cfe5fd0dd6f3fae7e110038d16313c7c280494628451e1e1b45a500a1c9`  
		Last Modified: Thu, 12 Feb 2026 21:04:36 GMT  
		Size: 1.3 MB (1311640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a61803f45f9a16a8a08a9c911f97d4805143f6810189e55a85e09d96f6f01`  
		Last Modified: Thu, 12 Feb 2026 21:04:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271cc796df4f493a11077b397fe9cd924c4365ac6067e630d6a9995b2f3b95fa`  
		Last Modified: Thu, 12 Feb 2026 21:04:37 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead3bf55c0035e28fde6061fd41f57a1ab221fee035b8226d678141acce7109f`  
		Last Modified: Thu, 12 Feb 2026 21:04:39 GMT  
		Size: 115.3 MB (115269989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebad2bb4202094f47f62c0dec52d92b420f35a642914025b906f794c36ae632`  
		Last Modified: Thu, 12 Feb 2026 21:04:38 GMT  
		Size: 19.3 KB (19333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698873b94b0d13aef9098473fb77c26eba2eba2e198653a415a2a3013b1d76b8`  
		Last Modified: Thu, 12 Feb 2026 21:04:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d47a78b32570a6d06f804b2066addfbabf58ccece693d2905ecd86f3fd0f3c8`  
		Last Modified: Thu, 12 Feb 2026 21:04:38 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d92c993d8ccc2acca3dffb548cd0f813f5f6d56f270efd14ca3242d95914f1`  
		Last Modified: Thu, 12 Feb 2026 21:04:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:4ac7a35af6b4f220dc1c55cf297d33021bc868fe701ea9a81cb094f5e29fbc4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6009209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cfeae1eef0679b302065179c5fa8496492d42a0821fba1f6eb54c7a61b6f32`

```dockerfile
```

-	Layers:
	-	`sha256:f00d75aa906e1ab1fbed3aa469a9707271eb3a1e079cc14e0a581c3656ebe37b`  
		Last Modified: Thu, 12 Feb 2026 21:04:35 GMT  
		Size: 6.0 MB (5956751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ebeb2eb594aab967f888e806e6492a1479b5f31c9f121900d794df5959515b`  
		Last Modified: Thu, 12 Feb 2026 21:04:35 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:3355270af3fca45467c4f893a6166bc16b07e456f88c922b6f72dc4d5f2b988b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91402075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d56f08b27fef49b927415da18b2311a9893cf42e27a94521f4065ba1065d2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:53:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:53:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:53:28 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:53:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:53:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:53:37 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:53:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:53:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:53:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:53:45 GMT
ENV PG_MAJOR=18
# Tue, 03 Feb 2026 02:53:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 03 Feb 2026 02:53:45 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 03 Feb 2026 03:07:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:07:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:07:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:07:24 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 03 Feb 2026 03:07:24 GMT
VOLUME [/var/lib/postgresql]
# Tue, 03 Feb 2026 03:07:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:07:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:07:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:07:24 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:07:24 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:07:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2112bec51f3682c1134b1548db8a0eb0bbf6b4a7c83987d779fa40ff2619e50`  
		Last Modified: Tue, 03 Feb 2026 03:07:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751428a21553d3edc43b837daf503d6cb262e363d902bccdcce11675dc96c202`  
		Last Modified: Tue, 03 Feb 2026 03:07:37 GMT  
		Size: 5.9 MB (5930384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57e7fb447de5be4902c43f06fa813857ab18c220a66745d9f773c196e91dbb3`  
		Last Modified: Tue, 03 Feb 2026 03:07:37 GMT  
		Size: 1.2 MB (1227521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226d1708a2e350e4cbb879805559aadbc426ce199ad26e1c89d679ddf48028ef`  
		Last Modified: Tue, 03 Feb 2026 03:07:37 GMT  
		Size: 8.2 MB (8204240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1257be07277d44a9a40284b8d43fc91831504de507450347afb07621bff752`  
		Last Modified: Tue, 03 Feb 2026 03:07:38 GMT  
		Size: 1.3 MB (1317308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885216cd59de3ceec980c7eb62da1a3133fa708e6fd8b98941e9bdd20b45efd9`  
		Last Modified: Tue, 03 Feb 2026 03:07:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1d5d3196524f2b023fd10856a8416e32dce3c058b3bfc880835664caa26c1a`  
		Last Modified: Tue, 03 Feb 2026 03:06:03 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf79a492397f145a37eaf9efd57ac829092b3afecaea66e40e71dc312531d1d`  
		Last Modified: Tue, 03 Feb 2026 03:07:40 GMT  
		Size: 46.7 MB (46745305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7859649cf27bb028d21895332ac6bab5695106b79dbd59d5c6ce05c3cb4fb5`  
		Last Modified: Tue, 03 Feb 2026 03:07:38 GMT  
		Size: 19.2 KB (19182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e20cf523b6010b9a256b0344ed37ac4000ceb91bf760f988feabb9d6e526a0`  
		Last Modified: Tue, 03 Feb 2026 03:07:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad3c5b3f48645f9cf0955e5ff45cde9e4e9b8d006ce0d9014d8eff03157b625`  
		Last Modified: Tue, 03 Feb 2026 03:07:39 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5b0e5daa8d39ba59f6f9ee147ea3c8a3f1d4351a6a3fb0d522404dc05803f3`  
		Last Modified: Tue, 03 Feb 2026 03:07:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:c97226a57f400edb49dd9dcc1d77071eae82d8299c2e7a6612ad5f9b81f17597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba985a999db1371d13249353eff01ef93cff92031dcff8711785c11f030541f4`

```dockerfile
```

-	Layers:
	-	`sha256:0541f3e0fde5eb768dbf5be92426524fa1f9945369b3d0ec8cd4dae8a1595fa4`  
		Last Modified: Tue, 03 Feb 2026 03:07:37 GMT  
		Size: 5.1 MB (5119894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6186381a5e076dd4d3dee945a480b3a11ef202bd6403a050d648d59b7a68cd`  
		Last Modified: Tue, 03 Feb 2026 03:07:37 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:eec8ea85c227218ef98f41139f34a41b78417ae837425a7e865b18b2497c76f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87722058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea9adae0aed6b058027b8f295fe190aab5987df1eca6d16575e78fea9886d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:57:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:58:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:58:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:58:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:58:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:58:17 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:58:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:58:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:58:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:58:22 GMT
ENV PG_MAJOR=18
# Tue, 03 Feb 2026 02:58:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 03 Feb 2026 02:58:22 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 03 Feb 2026 03:10:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:10:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:10:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:10:01 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 03 Feb 2026 03:10:01 GMT
VOLUME [/var/lib/postgresql]
# Tue, 03 Feb 2026 03:10:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:10:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:10:01 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:10:01 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:10:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7241322787a86c3779bd7129f7a8807cf92c82b40cae8140a64043e09e429c6f`  
		Last Modified: Tue, 03 Feb 2026 03:10:13 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbda09a90ebd9d8ced712bcef1a4eb8bcf3d80921d71d1442a1bb15332b961e1`  
		Last Modified: Tue, 03 Feb 2026 03:10:14 GMT  
		Size: 5.5 MB (5496547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbac2efac22379697efe078ef0beace421ead15d84acf377761f0b4f6e1554e9`  
		Last Modified: Tue, 03 Feb 2026 03:10:14 GMT  
		Size: 1.2 MB (1222407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658cb1e57c7d379e637ca1f77cd46d781d3544b167e499286c1c06ccb2470167`  
		Last Modified: Tue, 03 Feb 2026 03:10:14 GMT  
		Size: 8.2 MB (8204059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a481291ce9399b00362a580f02b5cbbdc062ee37bb0963d4ef616f42847f7047`  
		Last Modified: Tue, 03 Feb 2026 03:10:16 GMT  
		Size: 1.2 MB (1172633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8206cbe0dee3057333c851c85273901ba6be94b1d214092783a4b3afd9e29d6`  
		Last Modified: Tue, 03 Feb 2026 03:10:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab4d2c534455219ff205e7e38b057cfe334d62126ba6beac2f25e2e816383d0`  
		Last Modified: Tue, 03 Feb 2026 03:10:15 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897120730af41a07c2509c1a5ac10e848392afef6054dd6c140c2f6ce704963b`  
		Last Modified: Tue, 03 Feb 2026 03:10:16 GMT  
		Size: 45.4 MB (45382880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea85d7ef1ef0309ae642cf2f92af3cdeb0a0f538b23a4b5ef17d5e8c68d0dddd`  
		Last Modified: Tue, 03 Feb 2026 03:10:16 GMT  
		Size: 19.2 KB (19204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138a0e60a1396598bfcb6c3ed82ec488c9653f02f16b37b6da15a53eb6d1bfb8`  
		Last Modified: Tue, 03 Feb 2026 03:10:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999d9b78f4e9f7c910d058092a32ffc7810ceda8b51b5ed29ff48601d7e04ef7`  
		Last Modified: Tue, 03 Feb 2026 03:10:17 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450f3b7f684754ccdddd3faad92f91aeec8eb620ef6b56c02ae60abd79a81e75`  
		Last Modified: Tue, 03 Feb 2026 03:10:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:df96a3615a80bcfc1bad6c2cbc3a381b9ae4453a84c56d6aff88d84f0177d6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174356f7a13b7808dbccc0aa101b6a16c767e3f624d21089d14c0c79823736cf`

```dockerfile
```

-	Layers:
	-	`sha256:6f5ad74ec7b1d53e0ef9663af6c2c71dab7dc1fac1167fef6ba227bc148f87df`  
		Last Modified: Tue, 03 Feb 2026 03:10:14 GMT  
		Size: 5.1 MB (5119199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec622c1fb04092f6f3c8dad79d48f65deafbb4e6b67bd32c025f3d8bed4f3154`  
		Last Modified: Tue, 03 Feb 2026 03:10:13 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c850de575f0c5aaeb941c08fa9ac2fea5b71bb86c314739630f76af2da976640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160906507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1abcd3dfd6196090ad24565ab60d9399d89661aeaee15d57a0046e3bd0ca2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:03:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:03:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:03:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:03:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:03:23 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:03:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:03:27 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:03:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 12 Feb 2026 21:03:27 GMT
ENV PG_VERSION=18.2-1.pgdg13+1
# Thu, 12 Feb 2026 21:03:45 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:03:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:03:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:03:45 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:03:45 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:03:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:03:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:03:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:03:45 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:03:45 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:03:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded9a8fc4fa7e8fe731bf925d44fa4fcd679a8e53e5a30d9f121bd2f99f60cd3`  
		Last Modified: Thu, 12 Feb 2026 21:04:05 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff75d590949ddc9432a30bc0fe61a93013d23a6db43f43d6fc4b2d8c8e0008a4`  
		Last Modified: Thu, 12 Feb 2026 21:04:05 GMT  
		Size: 6.2 MB (6231068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8877a0d854abe449e0af0118a8ff38b3b156f96312cba3e058f22821c2ca02f`  
		Last Modified: Thu, 12 Feb 2026 21:04:05 GMT  
		Size: 1.2 MB (1209511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897f6ad82b48746b8fe6608245ad0ca760bdb0e59d5a918868d8c1dd7e4b5869`  
		Last Modified: Thu, 12 Feb 2026 21:04:05 GMT  
		Size: 8.2 MB (8203883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7a6ccc5f55e873cc3a7d968b1913666f50fcc6ce44a71ae5f942a8cb2b3eea`  
		Last Modified: Thu, 12 Feb 2026 21:04:06 GMT  
		Size: 1.2 MB (1220545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecd997d0dc2c5de3df250728bc9b6a884f08ce51774a7c24b66ce2e190e45c5`  
		Last Modified: Thu, 12 Feb 2026 21:04:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b5a489e4108e8c69527b3351187268700c9bf1fcad34563863360d8f601f27`  
		Last Modified: Thu, 12 Feb 2026 21:04:07 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996ccc8b94c2fdd9ddcd875f518585f3eb0e46cb68e6d1a602519e2db0cfba31`  
		Last Modified: Thu, 12 Feb 2026 21:04:09 GMT  
		Size: 113.9 MB (113871526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c5d0f44446e79aac8e6e556a0cffe11fc28589d039186929c7bacbed87938e`  
		Last Modified: Thu, 12 Feb 2026 21:04:07 GMT  
		Size: 19.3 KB (19331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd0fdf3766ba84874278eb4d277a590af8708bf982785e614e9fcc9aa5f1280`  
		Last Modified: Thu, 12 Feb 2026 21:04:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ce9848f5a4758637b589c75dc5b2115b6614ab1a30cc873503060d5f51d7b`  
		Last Modified: Thu, 12 Feb 2026 21:04:09 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0efe371a6b4d7d48d982e27649a43e667b5f5bee70b712b1a7fff1ce4cea5ff`  
		Last Modified: Thu, 12 Feb 2026 21:04:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:5ed1c488713854fdc95c626f217d3c4fa313762f64aceea4d219547cda55902f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754513f89670d385e280f27b3263361f06598d53731eac2d8739094ec192fe64`

```dockerfile
```

-	Layers:
	-	`sha256:b6533a8184d013e9901f8eb611bb0e9357df7ada53363c6681f1ffa299146999`  
		Last Modified: Thu, 12 Feb 2026 21:04:05 GMT  
		Size: 6.0 MB (5963124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9a70b87a2b9328c51df1b9509649a85cf5c5baca65545fc03b7c2ad0430bc3`  
		Last Modified: Thu, 12 Feb 2026 21:04:05 GMT  
		Size: 52.7 KB (52736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; 386

```console
$ docker pull postgres@sha256:e9d55eb89617d76161da674975912372a787d16e1945f750fb451d5b8c61242c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97512849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9fc7be0e817e351fc277196265ee8bdf2695d70f72e9eb5960059dc4020aa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:35:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:35:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:36:02 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:36:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:36:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:36:07 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:36:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:36:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:36:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:36:11 GMT
ENV PG_MAJOR=18
# Tue, 03 Feb 2026 02:36:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 03 Feb 2026 02:36:11 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 03 Feb 2026 02:44:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 02:44:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 02:44:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 02:44:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 03 Feb 2026 02:44:55 GMT
VOLUME [/var/lib/postgresql]
# Tue, 03 Feb 2026 02:44:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:44:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 02:44:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:44:55 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 02:44:55 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 02:44:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07777db809ec82418866176a741889cb16eb9427299a12b7fbd3dda8b2ac0ec0`  
		Last Modified: Tue, 03 Feb 2026 02:45:08 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8736de788606496c6624b36f558a3d6721b3489c67d19185ba0bc916f132c249`  
		Last Modified: Tue, 03 Feb 2026 02:45:08 GMT  
		Size: 6.6 MB (6630590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6549ab5243f9fc74df8b7612fd580597cb50238ca698bbeb1f1eb31842299dc`  
		Last Modified: Tue, 03 Feb 2026 02:45:08 GMT  
		Size: 1.2 MB (1225843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d84b7e87a29a4b39961d35fb071abd9fc3ea9caee21776bbf8b01d25e3c0043`  
		Last Modified: Tue, 03 Feb 2026 02:45:08 GMT  
		Size: 8.2 MB (8204000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4291591fae91021a4309b728ab6420f6446ea560b46d32ab16ce2c04d085579`  
		Last Modified: Tue, 03 Feb 2026 02:45:09 GMT  
		Size: 1.3 MB (1308247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c6825b3c8ec1df5c10fb24fbbe4fa18f662a0ca46cbc67e6fed7c41142dfa`  
		Last Modified: Tue, 03 Feb 2026 02:45:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c97b528e582ea3f951d5fe67d2b212cbaac400765361d409ba6f2d05df7ff0`  
		Last Modified: Tue, 03 Feb 2026 02:45:09 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef54429b8c5a5e6ba36134929cd4dce07405e9cb530267511241fe583f2cbd64`  
		Last Modified: Tue, 03 Feb 2026 02:45:11 GMT  
		Size: 48.8 MB (48820539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4024a131564909e049a2865e73e2bbedf7df298181951f37dcb99008ae53e2`  
		Last Modified: Tue, 03 Feb 2026 02:45:10 GMT  
		Size: 19.2 KB (19189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f403a0743aa389080aaafc563cfafe51f1cd3e47d7379dda17a89ff77ca6709`  
		Last Modified: Tue, 03 Feb 2026 02:45:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31992bcce5722ae6993a5b05e2b8763fa5a1676c0533e5189ad8e63b5a67f42d`  
		Last Modified: Tue, 03 Feb 2026 02:45:10 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b682be8dc0297cda052a7c07a811e406ddd38c307172110e096e9f072c6b1f`  
		Last Modified: Tue, 03 Feb 2026 02:45:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:9c6e89f964fe49ce342400e39d1d9bd60dc8513f86f8ce45f2399a5db4bd420f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29e30a8d4e52ab0f033d55c5cb6298c6e722e6cb9f102e6b6522744527834bb`

```dockerfile
```

-	Layers:
	-	`sha256:a3f0ddc4a0868ab9fc00891786b37073f7c3317919147b938b15c556555a0638`  
		Last Modified: Tue, 03 Feb 2026 02:45:08 GMT  
		Size: 5.1 MB (5115227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c133ac8ad45670a0dce127115cc3a533edae483f18b24796163927a3d507da`  
		Last Modified: Tue, 03 Feb 2026 02:45:08 GMT  
		Size: 52.4 KB (52391 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:e889ca5580e6fcfdfc62fdc734c6a6c9f371937d900afe87a095fc30f68bbb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174708003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c281f94ac20040d229dbe6228c71639fa7ec3cc5667da5ef8cc490ab20c7072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:02:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:03:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:03:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:03:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:03:37 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:03:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:03:47 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:03:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 12 Feb 2026 21:03:47 GMT
ENV PG_VERSION=18.2-1.pgdg13+1
# Thu, 12 Feb 2026 21:04:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:04:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:04:47 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:04:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:04:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:04:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:04:49 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:04:49 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:04:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dd2116d4f00610191cab66c1981409e66c43cfcea0b7afce48664af9ada05a`  
		Last Modified: Thu, 12 Feb 2026 21:05:15 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99cf5a0f5205f034311e8f9c0c3a94a51781cb93e8f59f0ed6560400db6aeed`  
		Last Modified: Thu, 12 Feb 2026 21:05:35 GMT  
		Size: 7.1 MB (7076719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173747098b4670bdf4262d42a1b879833541a3e367f8432e0a2a119e0be551d2`  
		Last Modified: Thu, 12 Feb 2026 21:05:34 GMT  
		Size: 1.2 MB (1214809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92305f81f4a0a40d11db267bcf684c4a77eb2f095c690e267e6da2fea074bb22`  
		Last Modified: Thu, 12 Feb 2026 21:05:35 GMT  
		Size: 8.2 MB (8204037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d6666bbf7d6240fbfe28141bdbed8a99a9cfc32497ac23e1bdad9a2ea2886`  
		Last Modified: Thu, 12 Feb 2026 21:05:35 GMT  
		Size: 1.4 MB (1394967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cda6fb4e1a3fc351a02d477d60c2a575674d6b5113368d1d651e093e4792f5`  
		Last Modified: Thu, 12 Feb 2026 21:05:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09b1640c0f3a3a530ecf3570c85b5a629532c446304c345cf8472675cb2915e`  
		Last Modified: Thu, 12 Feb 2026 21:05:36 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bd409a7ac033c3890430d3b9d039a2e9dfd827964917c99cd6468717f63d88`  
		Last Modified: Thu, 12 Feb 2026 21:05:39 GMT  
		Size: 123.2 MB (123187378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410389c77a513a002994f7a1c435f7f1b9e4014864867091a480f04ca03a09df`  
		Last Modified: Thu, 12 Feb 2026 21:05:36 GMT  
		Size: 19.3 KB (19327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620d1c9677cfe23be2d6b4baf0a826942a38766c71da435222e5fd9a1b2a5a4`  
		Last Modified: Thu, 12 Feb 2026 21:05:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a50598748fd37b76f840826fbbfe179af78e6f33fa3e1ac2d3271cb33d3373c`  
		Last Modified: Thu, 12 Feb 2026 21:05:37 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6e11bec92078843abf0793047dc75766808c5539cabd08f2dd88c6e329763b`  
		Last Modified: Thu, 12 Feb 2026 21:05:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e4c5e51c61e787ba1206bb0db1770973fcf86bc97d1af76b5719dbc41c6197f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a768ae353a48ec52f05fc860ef9ba07dbe9bc1af38848f072e44f9c4b25abed1`

```dockerfile
```

-	Layers:
	-	`sha256:b07052e9fff0cd57c607c75f896f7b5f192b5b8a908f72829914c32d37e232bc`  
		Last Modified: Thu, 12 Feb 2026 21:05:35 GMT  
		Size: 6.0 MB (5963399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb97aef49ea9298e03f96daecad39ef17ea234ed8205f6831c1b05d42dcae05`  
		Last Modified: Thu, 12 Feb 2026 21:05:34 GMT  
		Size: 52.5 KB (52534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:5da8c5d8e5b6f5253e3b80a1852687e202d8a300b8d671887e67b21e0f03ba4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92800093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd00820a31cc36efaae7d98dab5420f552e71cdc26166582a23ea4094c8fae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 04 Feb 2026 16:13:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 04 Feb 2026 16:14:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 16:15:14 GMT
ENV GOSU_VERSION=1.19
# Wed, 04 Feb 2026 16:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 04 Feb 2026 16:16:15 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 04 Feb 2026 16:16:15 GMT
ENV LANG=en_US.utf8
# Wed, 04 Feb 2026 16:16:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 16:16:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 04 Feb 2026 16:16:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 04 Feb 2026 16:16:58 GMT
ENV PG_MAJOR=18
# Wed, 04 Feb 2026 16:16:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 04 Feb 2026 16:16:58 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Wed, 04 Feb 2026 18:21:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 04 Feb 2026 18:21:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 04 Feb 2026 18:21:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 04 Feb 2026 18:21:38 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 04 Feb 2026 18:21:38 GMT
VOLUME [/var/lib/postgresql]
# Wed, 04 Feb 2026 18:21:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 04 Feb 2026 18:21:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 04 Feb 2026 18:21:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Feb 2026 18:21:39 GMT
STOPSIGNAL SIGINT
# Wed, 04 Feb 2026 18:21:39 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 04 Feb 2026 18:21:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80995be55917dc7fd201d347bc9226e2f5ac4bf648270056077ffdd82365b78c`  
		Last Modified: Wed, 04 Feb 2026 18:24:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1f5c6b2d99f755313f7c8a99b0dc4359c317ad0b8bf85fa05a15235111d7c2`  
		Last Modified: Wed, 04 Feb 2026 18:24:11 GMT  
		Size: 6.3 MB (6292229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3419a5cae79de9fcd3de7a8c5585cda9f74e580063c21f2ba132beaaf144525a`  
		Last Modified: Wed, 04 Feb 2026 18:24:09 GMT  
		Size: 1.2 MB (1202087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1011f782d19ba43309db24778d82c70cb389a070476ff5dae98b8b45210498d`  
		Last Modified: Wed, 04 Feb 2026 18:24:12 GMT  
		Size: 8.2 MB (8203651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0485b03c21170701329d20fbb35c7b9ca2b9d9a7d4437c48576a357aed50c301`  
		Last Modified: Wed, 04 Feb 2026 18:24:11 GMT  
		Size: 1.4 MB (1402345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055b637555d4df19ff25f1e2fbb73523accc9fa0389284938730df0384953bb`  
		Last Modified: Wed, 04 Feb 2026 18:24:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d5fd337755cc5ee8443095f73c397172e5f877bb14a60fe985381ee14c8dd5`  
		Last Modified: Wed, 04 Feb 2026 18:24:12 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7891df7d239e7a5204c6d37735ae5f5d057755cc4b8ef279952efc20392ffce2`  
		Last Modified: Wed, 04 Feb 2026 18:24:20 GMT  
		Size: 47.4 MB (47393616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38af23ccc764fe7a4fcf5bb3cb0919ce3b32fa8b040181e6b8ec604c0f3113a3`  
		Last Modified: Wed, 04 Feb 2026 18:24:13 GMT  
		Size: 19.2 KB (19192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75128f66af88b03a3b8ef6c20162df8cd51b48b2aec516267859d8bc149bc342`  
		Last Modified: Wed, 04 Feb 2026 18:24:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ede76c24447942b32aa134d71682cec7b06dd38310225f956be85e4ecfecec2`  
		Last Modified: Wed, 04 Feb 2026 18:24:14 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a79a25d2551fdaae6bd52b148bc35d11c2cd6379b18dad9a5765f1c3cb7afd4`  
		Last Modified: Wed, 04 Feb 2026 18:24:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e20f0d85c337139f941ce330dee8f53315305d17cdaac771df86b02c56d7e736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5162696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c478cea448e61e50fbabb1864aee79d5db1e8eeb718d27ddfb2610534ba0bf`

```dockerfile
```

-	Layers:
	-	`sha256:4c9444effc0a884e13b65eae0a835fb4d4b449404c0d3c064344dbb07cb4945b`  
		Last Modified: Wed, 04 Feb 2026 18:24:11 GMT  
		Size: 5.1 MB (5110167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5345dcd4d377048b1a005c78acc27fec51abde7fcc9a99a9581da627bba206f4`  
		Last Modified: Wed, 04 Feb 2026 18:24:09 GMT  
		Size: 52.5 KB (52529 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:c482533880e281ca33cdb89641892f9cd6ba92ded8f672e42d401c26b5aef8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176858536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa391416c23502f6d4b8d6c11e0d1616c25b145f18c53c36f615517da69c725f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:10:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 03:10:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:10:59 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:10:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:11:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 03:11:04 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 03:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:11:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 03:11:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 03:11:08 GMT
ENV PG_MAJOR=18
# Tue, 03 Feb 2026 03:11:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 03 Feb 2026 03:11:08 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 03 Feb 2026 03:23:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:23:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:23:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:23:26 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 03 Feb 2026 03:23:26 GMT
VOLUME [/var/lib/postgresql]
# Tue, 03 Feb 2026 03:23:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:23:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:23:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:23:26 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:23:26 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:23:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8077f2bbcfce1aaedf1a064a0e8fd51aebe94ad0ef24c0ff2ddca619fbd173fa`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79287514408b6ef0a85b7d3a863a699fc7122c0b12b45844a562c3208221510`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 6.4 MB (6408759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5e8fb73d9a4ab10b09d8fd286ff36deb8d8ae34e6f2013352136f379a40f4`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 1.2 MB (1230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c866b9c8124101d8c7209f17cfd7d182230fddc5fb91850fe69a2dd12caee377`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 8.3 MB (8258952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b55952f5e10fc188cd69ff85002b0f1dbd437076f36a273875c03c1562589f`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 1.4 MB (1398202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a2d60021e150d93707586195a33ecb491529c20516756048816be04ff66b72`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e42b977764bd402a1c842afa683e87e58284f47b463bdba118c8bd7fa04f0cc`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c451ba34ac57c75500f50c8d1fc12c5ea7d6ae63ebfa14e420df020aff079ed`  
		Last Modified: Tue, 03 Feb 2026 03:24:00 GMT  
		Size: 129.7 MB (129694498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bcb027227816da4be1ddccf028ed71e7eb0f718abc8c3bb640d4ad158af98f`  
		Last Modified: Tue, 03 Feb 2026 03:23:58 GMT  
		Size: 19.2 KB (19190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1afcb7af5e39fdfbe1af18909a7f7942f77784245b443042f1fd5dbcf13498`  
		Last Modified: Tue, 03 Feb 2026 03:23:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82186cd635cc43110b1611643790b679087ee2956d555847252cf43de926ea78`  
		Last Modified: Tue, 03 Feb 2026 03:23:58 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f78da5da7ea1596ea1b43771ca177dad927f687aaf7006dff485168ef02612c`  
		Last Modified: Tue, 03 Feb 2026 03:23:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3ed54179b768bb582b403014a8386adf9edbe363620a443a30ce399568d69129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b31259fce01305767b38eecf4ecdafe0086a7e0dfaf712f4cebaf08ec8d7237`

```dockerfile
```

-	Layers:
	-	`sha256:e5347135bab5a2df37a0d44a19a9b7cb082a600d19a3d4cee3c466403c9565a0`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 6.0 MB (5973421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c857605ca4bbcda1e38fc42241a8b33e0d9db199d220ed5eb25196ebf0be40a`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json
