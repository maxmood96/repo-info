## `postgres:13-bookworm`

```console
$ docker pull postgres@sha256:ba6ef1f07410f29e9ccf0946c3fe17eb7a1466f826c46a30e7629c4f2e29b1d3
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:13-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:b79fd62dd7adb077e4ecf6e2ec7366caa6abc3fd7f0b1bd15bbf15dbad697126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148955110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e42e68e624592a8cd6fd02ce0a6e796e1f77ca953714260985f1596cebe6cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg120+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0073ad29fa0d0baadf9a4278397049d3be502742d9d5c6e212172e52c658b54c`  
		Last Modified: Tue, 14 May 2024 02:58:00 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de26d616f1f0bca54f1eac42003abee11436157b4deb4cb3fa69b831f58fe8c`  
		Last Modified: Tue, 14 May 2024 02:58:02 GMT  
		Size: 4.5 MB (4533685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9ac1916a4fe697c5bd1149056c378a36528b50e3c0afce762e710d6b5e9c2f`  
		Last Modified: Tue, 14 May 2024 02:58:02 GMT  
		Size: 1.4 MB (1449885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86761c4a52a00b52451a14ea5237f9d583ecddf48d7c66cec802743233a8b7b1`  
		Last Modified: Tue, 14 May 2024 02:58:02 GMT  
		Size: 8.1 MB (8068839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b2865caf71e146f3f2bdacbd8ade1a4a103045b1668bfa00240d05a77ec0df`  
		Last Modified: Tue, 14 May 2024 02:58:02 GMT  
		Size: 1.2 MB (1196013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34d7669106dbd55813f019528b3505ace02fe70e6ac99a5b568aef12b1a218b`  
		Last Modified: Tue, 14 May 2024 02:58:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24b834dff71df8bfa7f37136b18b96d2ab516477b4db90526ea29a5c7115ef6`  
		Last Modified: Tue, 14 May 2024 02:58:03 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a221fe6652fc2187bf118c7f85e44f476f82826a711540a2f9305765e657f7`  
		Last Modified: Tue, 14 May 2024 02:58:05 GMT  
		Size: 104.5 MB (104536617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3373f066ae4eef9627f80f1577ca45f310a123ddeac6c3b73157a045e4927052`  
		Last Modified: Tue, 14 May 2024 02:58:03 GMT  
		Size: 9.3 KB (9344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f474a1424ccb1d5f4963a8457cc6d11ce67239b40b7c3de31ce38ba979cac7`  
		Last Modified: Tue, 14 May 2024 02:58:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161dc7c149b41857135826b4be10765040024fcfb1c8d442015d266cff68b47`  
		Last Modified: Tue, 14 May 2024 02:58:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946b6e741b0e9a02b1ca74f0a53494a4b3e29d2b7bb477f8bff34c0707c1d738`  
		Last Modified: Tue, 14 May 2024 02:58:02 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb99a6e3550a95ba682b927c69904c01737ba04efbb568115c301ef6e072f7d`  
		Last Modified: Tue, 14 May 2024 02:58:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a5b8a7fe9f37fab7d879e2610f7b03b19c9d9fb0b4b6f228d93e658c7796d6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee3f41fe155b4b95d44bcd9ed785d8f4770ca9bdcf23a3d009a8ef86105d763`

```dockerfile
```

-	Layers:
	-	`sha256:15256bacdc0915d8959f90566062bce548f8f6618c9b5c3e748b1ec9592f02a3`  
		Last Modified: Tue, 14 May 2024 02:58:02 GMT  
		Size: 5.6 MB (5564677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ac17f443da929474a9a8aa10ce9e797ada4b48d2c2bc349d50f0166d153150c`  
		Last Modified: Tue, 14 May 2024 02:58:01 GMT  
		Size: 55.0 KB (55027 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:a8dca32220a7c8cc07474a4b6ec21cd8435bfdaa44efaf68e80f83d2c85548a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146258188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426c6376f535a62d7e57b8f3a6c19766701562928fb8f8c5e6add1a80864a59b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:11 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Wed, 24 Apr 2024 03:53:12 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg120+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81edbd276bfb152d9b8dbd1058e05f108121be5541877d97389f7b657b52416c`  
		Last Modified: Thu, 09 May 2024 22:14:17 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a481ac39beac5c40d7b1205e889e5acc6fbd3add4b09d769c64a60bcf3cc017e`  
		Last Modified: Thu, 09 May 2024 22:14:17 GMT  
		Size: 4.2 MB (4150927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9e070ad10aff56d59e9a1a93bd2e27b50a975bd3a72c420114dab32cd8b6b6`  
		Last Modified: Thu, 09 May 2024 22:14:17 GMT  
		Size: 1.4 MB (1427070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a036cb2e0c807cf11336b85fcfdbb378a57475cc786d76665ce69dd376ca4e`  
		Last Modified: Thu, 09 May 2024 22:14:18 GMT  
		Size: 12.7 MB (12714939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1e496d5d33db24aafbd4009a0cedd112942001d6dfce49235eafc08a504dc2`  
		Last Modified: Thu, 09 May 2024 22:14:18 GMT  
		Size: 1.2 MB (1195008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e76e69c688ab7466aac8cf7a47771f13182f9df0319ab43f51d21d6c90bf38`  
		Last Modified: Thu, 09 May 2024 22:14:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c82fb353ae1fe2943ecb6b9ea3a11b162eaa2b185fd6f5d549359100de640`  
		Last Modified: Thu, 09 May 2024 22:14:19 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac906b23798381f8e6f7af2cff137b3ec846a7e67896974a4054f61d9da3e9a5`  
		Last Modified: Thu, 09 May 2024 23:52:38 GMT  
		Size: 99.8 MB (99840522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8338777751a58fafe88a5151c6611f799b35324bbc381a5b814873325117939`  
		Last Modified: Thu, 09 May 2024 23:52:35 GMT  
		Size: 9.4 KB (9361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cca792d6d012a4c8fd361643fdce2fbe802157e7db1c27b1f74477e538e11b4`  
		Last Modified: Thu, 09 May 2024 23:52:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456a74c3d391e3c1e62fda9c894922e09c1391fb48ba2aed0bbbc86657c72011`  
		Last Modified: Thu, 09 May 2024 23:52:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c44bbc896a59bc68ab929db51c672bca300f4db66ee6c5b7f8e985f1b95a57`  
		Last Modified: Thu, 09 May 2024 23:52:36 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81f0370586025447a76ba65a2579a1c1c6badac78be8ed72ab495adfe153802`  
		Last Modified: Thu, 09 May 2024 23:52:36 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:26c2a9cd7a303a6f09bd35f90fc707955e20671366630c6f7bd145c2f0818590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5632855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7798fab8785be5935259aefb9efc96bf8c662b293fcdddeb8a857585681b2d`

```dockerfile
```

-	Layers:
	-	`sha256:c03c3a2dd65ea9e0c117c0c3a6fa3f747f4d770396258f89fe4f6a72607b4d6f`  
		Last Modified: Thu, 09 May 2024 23:52:35 GMT  
		Size: 5.6 MB (5577779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d73e152166c70d91fcad9111254b0afc9c0ea08d7587d73fe81bb6ad7985a80`  
		Last Modified: Thu, 09 May 2024 23:52:34 GMT  
		Size: 55.1 KB (55076 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:aad31aba28287f6229924e2b63b326bbeccd9196eff604b6a2588ba9ef2880c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136416739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050cc84488e8b8c11383c15c40df57540395443e54d941bc6df753cb5a9153dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg120+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82f99b716fc98f154df0f76b1c3b2f3f9c86d3b4dec80d80e99b0062d457de6`  
		Last Modified: Tue, 14 May 2024 17:02:34 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591a3170f7b289068e879154c6d307a2a9c0d07a5cbbec2953f0f85a06fb404`  
		Last Modified: Tue, 14 May 2024 17:02:35 GMT  
		Size: 3.7 MB (3742541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87817ead93fe912f0cddc59f566c6ea64be19d5e68fa0bdeabdb4094a101cf1`  
		Last Modified: Tue, 14 May 2024 17:02:35 GMT  
		Size: 1.4 MB (1417056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27645fe8f047f291e39b8c277e7937539dfe124483dcd26639664df12fb7ba2`  
		Last Modified: Tue, 14 May 2024 17:02:35 GMT  
		Size: 8.1 MB (8068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5a1c3ebdf06845e5b573a058174b19029f322c36681d90ba253fc486ed74c7`  
		Last Modified: Tue, 14 May 2024 17:02:36 GMT  
		Size: 1.1 MB (1066931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3d498843c867e0c59ea2d6a286dbdfb2636347d7eeddbbfcbe10583778363e`  
		Last Modified: Tue, 14 May 2024 17:02:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f366fb3f7488e0556db8f9cb01571357a4ce3cb3944337b17bff5d2ec98ae8`  
		Last Modified: Tue, 14 May 2024 17:02:36 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b62b5743eee459bca517eb950356eb382294f27faee42e029947c83f2cfd9a1`  
		Last Modified: Tue, 14 May 2024 18:54:38 GMT  
		Size: 97.4 MB (97361487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de99d7bc8bf8fbe79f414f9dd730804c1a1696605bf24d611faa4459bb6cefa`  
		Last Modified: Tue, 14 May 2024 18:54:34 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7519f7142acb3e6fa07627c19554da53e8e10d5d51647cb657c263f458572aa`  
		Last Modified: Tue, 14 May 2024 18:54:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb4d79583534e4ac110441520cfb1a7034446f368c1c2109bc6a03bfc24b1a3`  
		Last Modified: Tue, 14 May 2024 18:54:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d55dc5409a45ee7ff5e094dfeee0c75e1a308999e44c0dc8dfb4e297acb889f`  
		Last Modified: Tue, 14 May 2024 18:54:35 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76c622991db038ecd21b0240e4e9392876ad2f0642ad76efcba6ea957d3c58b`  
		Last Modified: Tue, 14 May 2024 18:54:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4ed25556c2da2f1bde15b5b7e8ae2ae9476b3a6b9cf919cd2a00e8b7d1f95b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5632658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f72af2c4800c960736095e50bf0d9900bd80fd3d9f45ac2488dc5e872621e5`

```dockerfile
```

-	Layers:
	-	`sha256:e3ab9c319a7b4baab5c99f43f8aa485364300fe7790ec6ac5cb698b8ff851b37`  
		Last Modified: Tue, 14 May 2024 18:54:34 GMT  
		Size: 5.6 MB (5577591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6355ab038d9dda94dfc0933c5fec6be103f50e7adb114e080086ba7240d9d796`  
		Last Modified: Tue, 14 May 2024 18:54:34 GMT  
		Size: 55.1 KB (55067 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0797c4d4b07bd43c9737b187e0848094ef4dd1c829177c81c122e9b097e99511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.9 MB (152913793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e52abe6124602943e9d5641beed90d89d15cf6f77360c526aaa7a0592dda0ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg120+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdb2c40dbefc2778641a89b23098bfee01897ba7843d5198654c75f5b575731`  
		Last Modified: Thu, 09 May 2024 22:05:44 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1503404287478d49c3593e6e71d12e9861f8327ad9bbb440968bfa1b202b278f`  
		Last Modified: Thu, 09 May 2024 22:05:45 GMT  
		Size: 4.5 MB (4499174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767286a183cd656fb2293bc02cf6f3ce4f4390ff952e6fc7c0fc26d66ff700c9`  
		Last Modified: Thu, 09 May 2024 22:05:45 GMT  
		Size: 1.4 MB (1382238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250bc06e5c190701772a44c1e547d70f123537f86d1f6310498f087ce2e0093e`  
		Last Modified: Thu, 09 May 2024 22:05:45 GMT  
		Size: 13.8 MB (13827856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09ec754be5f30568d43469e5abe8d4a97416f93dfab6e8389825701a479a63e`  
		Last Modified: Thu, 09 May 2024 22:05:46 GMT  
		Size: 1.1 MB (1108919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98da581ff67ec7a9b71c6eeeae15c6de7785f65413e3024bcfc321ace6874c05`  
		Last Modified: Thu, 09 May 2024 22:05:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749ef310135bb0e04cf4faab77e010740d8269fd7d7736f522ec78ab494138a7`  
		Last Modified: Thu, 09 May 2024 22:05:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8f48e39dcefe73e1e808866616f089bb7b3764c38ffe23471b8f85e51eee8c`  
		Last Modified: Thu, 09 May 2024 22:42:27 GMT  
		Size: 102.9 MB (102895989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26555ef77f648c436d1cb962ade45e198eda0c64a5112afb956cf8a935774dd6`  
		Last Modified: Thu, 09 May 2024 22:42:24 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a940daf283488e7168d11e8d2865eacbf2f07ed6a71a9c0f60ba5471565468`  
		Last Modified: Thu, 09 May 2024 22:42:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7616d103b013c386fc6b6a3c2346cab2165efde3c37c1b0d7d3853c05f47b847`  
		Last Modified: Thu, 09 May 2024 22:42:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1792bddf2074cbf5c45221c4d4849a5bc05ef795a9e5a801b791ce42d2227918`  
		Last Modified: Thu, 09 May 2024 22:42:25 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0849c77666786a95fbca12da2e210f8ce0264bc7d5171556c78665301247d9a8`  
		Last Modified: Thu, 09 May 2024 22:42:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:899f28c856d12799dc45abdb6d49c80ee2f635571620d9db735eeacc3c90a85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5625852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc911b4346fab87e19110ec5292166e2b7841c7df599f7836f6eb4f709a0900`

```dockerfile
```

-	Layers:
	-	`sha256:d54ff8dbb6820320094e63bd75f16ad6ac66a78d11c740c8d1514c210484fabf`  
		Last Modified: Thu, 09 May 2024 22:42:25 GMT  
		Size: 5.6 MB (5570973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad693c6b558e6692fc8241ac6ee47a1a533a7e0faa8041c4886a8582beeacc69`  
		Last Modified: Thu, 09 May 2024 22:42:24 GMT  
		Size: 54.9 KB (54879 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:113f6ab5bc5f8b735797389c6a7cb800fe66a056242dc7608ca2ec669660a67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156905946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae78bc0e3e07e9a1212307037812017740dd123ca05db8b5e331a4c1f9b36898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg120+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed2620ab9e4401fbbd443041fc128930959051eec5e07e7b7fc1d09665fea87`  
		Last Modified: Tue, 14 May 2024 02:06:22 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16481dae15e6cf50b575269d34f22e486bc76f4683c4a2ac088195b19dc4d7b`  
		Last Modified: Tue, 14 May 2024 02:06:22 GMT  
		Size: 5.0 MB (4965048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d73edd350debe8f8edb75f10b1ecb82bf995ed75deedd98ff52cab074b4edd5`  
		Last Modified: Tue, 14 May 2024 02:06:22 GMT  
		Size: 1.4 MB (1425614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9909ca61bee5a4c155d669d05754f87d59d1b5a737bd2c838c60ef43b61e0dce`  
		Last Modified: Tue, 14 May 2024 02:06:23 GMT  
		Size: 8.1 MB (8068880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbf446f6e56c2260d1547f28deb5f54084710125710f5b8c44c25ca02df2f97`  
		Last Modified: Tue, 14 May 2024 02:06:23 GMT  
		Size: 1.1 MB (1137144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d5a28e101968b70d2ccf33f71cd317a44b89db584023dac50a76053ee740ff`  
		Last Modified: Tue, 14 May 2024 02:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a0122cfc07e0e68b8b234c0a0d3fdce30f13dfc9d8407eb74df79516483451`  
		Last Modified: Tue, 14 May 2024 02:06:09 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588471d53ce419288372caa4e0a364eba79982e861197cd6410cab7d1eed9c94`  
		Last Modified: Tue, 14 May 2024 02:06:27 GMT  
		Size: 111.1 MB (111126947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8906c1a5995c4837ebd3c883017972fcbfc26f0b42cdb5491d4ced9202ccf6b`  
		Last Modified: Tue, 14 May 2024 02:06:24 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15eb9a4c64d984f9dda24a371fa2ce6487a126683e5710b9b5e1f152ae827e4`  
		Last Modified: Tue, 14 May 2024 02:06:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b743a755017a830f92d1c23705687d065886d4f975a499bba0ca39055d1aaf6e`  
		Last Modified: Tue, 14 May 2024 02:06:23 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aa078e300e246584a281eafef87dee702ffa0a1f0a273f0e89dda1e10920bb`  
		Last Modified: Tue, 14 May 2024 02:06:25 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e28415fe2a3f168d680f6aa68c5732bc7f7bf097b1fb2fbfe2ca1e963fd440`  
		Last Modified: Tue, 14 May 2024 02:06:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:be095c6cd3fe95d03a2a2d2998933d4926ffcf39c6b1afad8c891b6ac2388831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5630808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bffa64d8430658a977b576e0f4f9aa8d7a82975c9d3364a5848734a78ba348`

```dockerfile
```

-	Layers:
	-	`sha256:480346a6a90919895f1d603adbc12b3b447dde2c13ffaca3be78d9e9cae24b8c`  
		Last Modified: Tue, 14 May 2024 02:06:22 GMT  
		Size: 5.6 MB (5575832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1ea1a305d8f8ff598345142619235354bb53e0a08dc077a077eeb2bb701d21`  
		Last Modified: Tue, 14 May 2024 02:06:22 GMT  
		Size: 55.0 KB (54976 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:6cc6b41f9d00085d83996073ba9c756611de87a9bdd8760398cc271fdb5a24eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150199753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e7aea6d2a463d1d5488625c9615b9d27bedc6f67faba498164d72c38082946`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:18 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Wed, 24 Apr 2024 03:14:22 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg120+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444580f13fc2904f694a6d349b2c67522a17038dc67e92c827568052f2e0b2ac`  
		Last Modified: Thu, 09 May 2024 23:07:52 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9f3e74bf4aa576c2a76513adb11f6df72dfd541ee2a50bf860c2ca61926c08`  
		Last Modified: Thu, 09 May 2024 23:07:53 GMT  
		Size: 4.5 MB (4475113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d139aa4150efef6039cc0e1177f6b86dd83cafbd3a05cde5f4479a1ecac1d96a`  
		Last Modified: Thu, 09 May 2024 23:07:53 GMT  
		Size: 1.3 MB (1337093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9d4cba642795a52fde29406517d061d02fa91af197f1ce15087b3ceeca99c3`  
		Last Modified: Thu, 09 May 2024 23:07:54 GMT  
		Size: 13.9 MB (13910003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c864642aa63843ab307d2ff5f9877997902be475cc5fa88279294135cd2b310f`  
		Last Modified: Thu, 09 May 2024 23:07:54 GMT  
		Size: 1.2 MB (1182924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c02f9b55a7f0ae492cd5fe5179551cfedffff6421d59b72ad7961ce80c58dac`  
		Last Modified: Thu, 09 May 2024 23:07:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6294b3dbbecac21ce86add5c22e19a23cb294be50e74d8bd103966c23fb9a15`  
		Last Modified: Thu, 09 May 2024 23:07:54 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8f180b2c66212996f5213518180b215fc7473fb1143ab0301197854795ac25`  
		Last Modified: Fri, 10 May 2024 06:10:42 GMT  
		Size: 100.1 MB (100130744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8487e50bffcae6d5a5f95db8b3d14f11da28afae03d5094f7ef4fc966c083728`  
		Last Modified: Fri, 10 May 2024 06:10:33 GMT  
		Size: 9.4 KB (9360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96e35975484a2c52ee7ee8610e1b55936d3dbb2f2eacf27314427bc8d823d52`  
		Last Modified: Fri, 10 May 2024 06:10:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db535e57ed53bea302e19fb92e7fdf3c6ff56e81dbe7afe4cd600de2d7dcf132`  
		Last Modified: Fri, 10 May 2024 06:10:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460f0ee0190870e5faaf7f64c472db94b5ab9a9b4e1ffcde22ef5abca359cf9a`  
		Last Modified: Fri, 10 May 2024 06:10:34 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e75616b699803b21d2b1e1d4091425a29ffb45e66c345a06ef2c8ec5836aadf`  
		Last Modified: Fri, 10 May 2024 06:10:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2db7ac52697c01779a0e4c8b7e677032166d36583ded4bebd10a68a5cc6a1a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 KB (54741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbff7121835490d3335f648bf66fef112f83794d48d86927cf39bab65b12a55c`

```dockerfile
```

-	Layers:
	-	`sha256:9c04c8a3610a0c20a26e544dcaa80287cd33df9827b700ba3b5003c93213509c`  
		Last Modified: Fri, 10 May 2024 06:10:32 GMT  
		Size: 54.7 KB (54741 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:272759f5eeafc361096c86b82a83aa2c1884b349d9c430250db6e313ced758ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160957202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0cab21ea926edbb9e78b7260441a957b221968ddfdb10e727436697395c6d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:16:46 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Thu, 09 May 2024 18:16:46 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg120+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679533ebd7a290ad3f9e86a947131de8ce2263568b3b2f9dce2426af3c1d9d71`  
		Last Modified: Tue, 14 May 2024 15:38:31 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc75436997df176c438cc3c32f068ef7ef32a430fe088f60f3b14b8799d027`  
		Last Modified: Tue, 14 May 2024 15:38:32 GMT  
		Size: 5.4 MB (5368171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec7a9c9e28d59d671b303a8ed215dec5c617d085941712041975a6de179576e`  
		Last Modified: Tue, 14 May 2024 15:38:32 GMT  
		Size: 1.4 MB (1371225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baf0005c66072b15b907340892649f395b58750a2727a4138c8d62fc30b9ef2`  
		Last Modified: Tue, 14 May 2024 15:38:32 GMT  
		Size: 8.1 MB (8068963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21384c66fa8ad2af30496f67140f8e068f2ceb2a2d789837e2384593cfca9fd9`  
		Last Modified: Tue, 14 May 2024 15:38:33 GMT  
		Size: 1.3 MB (1283486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c0befeb421a5453649797a027f09baad45dc7c996e3486da49f4e9879286e`  
		Last Modified: Tue, 14 May 2024 15:38:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46725b9093668cd05b0dc9eb9f0aba3b982b3a9434680e5c3303df5b96960ec1`  
		Last Modified: Tue, 14 May 2024 15:38:33 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c8630f9522373d93c71cb316be94171e368c43bea023162ee3097ae6e49a84`  
		Last Modified: Tue, 14 May 2024 15:48:22 GMT  
		Size: 111.7 MB (111704532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0e1b853270ff3913c65d7569d13710727fe9e654a427b7b15f22b4e8d7637b`  
		Last Modified: Tue, 14 May 2024 15:48:18 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2be1099ef4ef85dd5ede704b124c9775dc7432726dca4e45a48b11faa3f1c2`  
		Last Modified: Tue, 14 May 2024 15:48:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a9c74c167e0070ecd94dac3067f1543e30ec2632eb15a5ba1d38b76119a292`  
		Last Modified: Tue, 14 May 2024 15:48:18 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f104948aee0b8980fce32e09ab6775764b7f98c6282b54355e36bc68aad0573`  
		Last Modified: Tue, 14 May 2024 15:48:19 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b56b2d7100009e5c12e788988f7cd1e7e7f57def32828d00d8cc61216983f1`  
		Last Modified: Tue, 14 May 2024 15:48:19 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4dd1a81fe7ff6817a6f66bc3e76c3d09f93c1a74a66e2d09f9f35f8008162af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5626825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adc37904b1599ca35cca41cba0b60f61ce875e4d482afed76d022187775597c`

```dockerfile
```

-	Layers:
	-	`sha256:9fd3c619465d64de6eb010b730412d8e39462594d7a4c48ff2cd351e4776ec20`  
		Last Modified: Tue, 14 May 2024 15:48:18 GMT  
		Size: 5.6 MB (5571906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7208d4b2090c159119e0e953fcdf38df18bc5dea88e1e232185899e4ac587e1c`  
		Last Modified: Tue, 14 May 2024 15:48:17 GMT  
		Size: 54.9 KB (54919 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:ecaca786e06cfde856f8bce73e8c614ef2e9fed382c73f37c040be5798419b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159279293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b7a87b0b99068f64e1506584ebe4ba79cc15dac338d0a0920913a78b622152`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15-1.pgdg120+1
# Thu, 09 May 2024 18:16:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f003856984611f6a84292d175743135cb79ba992a8cc4f64ea85fe8892f388`  
		Last Modified: Thu, 09 May 2024 22:06:51 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0e476833bd3431413e2bf73bab6be3561312929e550ce73d43181cd5d5b096`  
		Last Modified: Thu, 09 May 2024 22:06:51 GMT  
		Size: 4.4 MB (4391031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a63140178ef304ac303edaa3418238557a0d968f18dbc35e79e707430794bb1`  
		Last Modified: Thu, 09 May 2024 22:06:51 GMT  
		Size: 1.4 MB (1415958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5662ec559f18147fbe7ee13f979be9c62b4a8200b3a3e21f04ad8e91cfccf0`  
		Last Modified: Thu, 09 May 2024 22:06:51 GMT  
		Size: 13.0 MB (12986145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2159dec2389cfd5f73b7309ce006c32bc458a333e6720629df904d8d6ba43aea`  
		Last Modified: Thu, 09 May 2024 22:06:52 GMT  
		Size: 1.1 MB (1096971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b2e22b6e43aaa4e3ff1b0acb18d1e11d468e9556778f7880701fea25ecd24c`  
		Last Modified: Thu, 09 May 2024 22:06:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0730e23097d72de7fb6ec61da966f414e01b80cb01ba8a9d71855f43e6549b9b`  
		Last Modified: Thu, 09 May 2024 22:06:52 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b510db5146058f7a203e44b9c956b0be02c85db88f54da5779e48702ffc4537c`  
		Last Modified: Thu, 09 May 2024 22:40:53 GMT  
		Size: 111.9 MB (111857150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ecf96cfdb072c363cc56f6b1cbcb310502488c4e38123c5993afc73a43c77e`  
		Last Modified: Thu, 09 May 2024 22:40:49 GMT  
		Size: 9.4 KB (9356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a17c4c5b8fa29fec454e3d1c757ba32fbcb7a9ddceed0c824e4ac933b78c7e`  
		Last Modified: Thu, 09 May 2024 22:40:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17055770b20bf7c5527f22922554d129918ca3eed4cc35581e00803d7ec5fed8`  
		Last Modified: Thu, 09 May 2024 22:40:49 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f233e5487a5831bff5edb0b2d38417ba1fc3db20199fd1ff89d9c73f7010542`  
		Last Modified: Thu, 09 May 2024 22:40:51 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe13990509d10b3a2f64253bc77487edb4517b29b329d48950d9051dcf8162c`  
		Last Modified: Thu, 09 May 2024 22:40:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4a163382339655da992f52de3562bf70f4749ef5a84c04ee3de3f7ed3f2ffde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5618941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681c7f7f8bab18a8045156f25b5c327b82309bf980fcf4502ff6231a26521373`

```dockerfile
```

-	Layers:
	-	`sha256:09701ac38d9e709ed33547e6e84b7f5db990d1a5d2c166f9fc9e0085e4982883`  
		Last Modified: Thu, 09 May 2024 22:40:49 GMT  
		Size: 5.6 MB (5564071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3ccf800a3ab86636498ec972036c956ac2c23a1acb7ef3760aac25ff549cc9`  
		Last Modified: Thu, 09 May 2024 22:40:49 GMT  
		Size: 54.9 KB (54870 bytes)  
		MIME: application/vnd.in-toto+json
