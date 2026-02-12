## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:93be01580de628fb24e84c51ada30e83c7ce8090e0395e580fe93be24c802cb3
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

### `postgres:16-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:2b669f6506fa2cd0c1ff0d1bbd019a819ba3aa2876463b93763e143726b4e099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155029450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910b3cc679142f027d1ed3968d46a1aa7c5898e79ec761b5a4a60a183b9cc47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 12 Feb 2026 21:04:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:50 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:04:54 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:57 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:04:57 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:04:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 12 Feb 2026 21:04:57 GMT
ENV PG_VERSION=16.12-1.pgdg12+1
# Thu, 12 Feb 2026 21:05:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:05:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:05:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:05:10 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:05:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:05:10 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:05:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:05:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:05:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:05:10 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:05:10 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:05:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c21a024160b40b90a3e0f42d308981646b7d4d7ea8406d35cc65932148a38f9`  
		Last Modified: Thu, 12 Feb 2026 21:05:29 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd25ab128841d04741da1d6153f84b89144441cbb2e6e26face170d5dae4b322`  
		Last Modified: Thu, 12 Feb 2026 21:05:29 GMT  
		Size: 4.5 MB (4534220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f27bd80d8c02d40a2f1efadf25f3d4833db6de776774632c94ed386a7a96`  
		Last Modified: Thu, 12 Feb 2026 21:05:30 GMT  
		Size: 1.2 MB (1249555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f1484e5e97a6523edcc8946ff8054dcd7bc651ea4685c7856e01d7bd9d5a01`  
		Last Modified: Thu, 12 Feb 2026 21:05:29 GMT  
		Size: 8.1 MB (8066474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e44d95e4f7a4e2aaab46b3758c4bfd37b349f5e3620a8f6e6101ac2a73c1e3`  
		Last Modified: Thu, 12 Feb 2026 21:05:30 GMT  
		Size: 1.2 MB (1196410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c10bd419c0afb780bf313cf222199d3cfa3fea95c3f4458a81b5a6d7b1a818`  
		Last Modified: Thu, 12 Feb 2026 21:05:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a641b21f3a57b974cef589a858b15394c99d5e6548c47a6df0aeb07d403013`  
		Last Modified: Thu, 12 Feb 2026 21:05:31 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f80ea6f7c79366336509540246d7f48f977a4c2eebc83f83dc202ed2ff025a`  
		Last Modified: Thu, 12 Feb 2026 21:05:34 GMT  
		Size: 111.7 MB (111733585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be22009e15c5142272a61cdb6d83347f29955b81a06d74dbff99018e23b2644`  
		Last Modified: Thu, 12 Feb 2026 21:05:31 GMT  
		Size: 10.0 KB (9972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8312caab38196ea6e00ca07c33f32ac5a4836924f3be3eb76fcc5a6121378e`  
		Last Modified: Thu, 12 Feb 2026 21:05:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2f5d743f593fbc57565ce206460d8516e82df8117add8e6773e36327e03ac2`  
		Last Modified: Thu, 12 Feb 2026 21:05:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e33c2b9c4858d9acd2f0c2cd9dd66f64482974b19f9af460ee9c3142c1ca9d`  
		Last Modified: Thu, 12 Feb 2026 21:05:32 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8255f3feb63d8e4054f5c26587e3eeb49dae2dceb9b73ea2da13c450830f1436`  
		Last Modified: Thu, 12 Feb 2026 21:05:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8a3959b0c2263f8df5fa80ff9ed7f101cdce5fd6e4f8b1985ffeb31b61ac883f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7117e96b6cc42822fe174274db673750588eb99ccb0df82c568625816476055`

```dockerfile
```

-	Layers:
	-	`sha256:110d9b1fb4047f394e7054d5e9fdacabc359003befc63946293cbeca79f32412`  
		Last Modified: Thu, 12 Feb 2026 21:05:29 GMT  
		Size: 5.9 MB (5909556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c2b2f195714d771c2978c6a79f52a5d353aeee127305093c524b7f09e4a872`  
		Last Modified: Thu, 12 Feb 2026 21:05:29 GMT  
		Size: 53.3 KB (53294 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:7355bad1ac920f7478dc49ea6b9deff439b4b05781a9f5a87c5b6611006ba21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148014524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d3d134b41ae2f796280ccf97d004c6e2dd1f7687731f299a0999d9c6a0e8c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:56:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:56:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:56:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:56:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:56:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:56:39 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:56:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:56:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:56:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:56:45 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 02:56:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 02:56:45 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 03 Feb 2026 03:11:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:11:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:11:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:11:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:11:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:11:59 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:11:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:11:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:11:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:11:59 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:11:59 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:11:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6036aff531a372e1e9da48952322760c8c052f6735e66afd3251a32e5baace8d`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 25.8 MB (25757618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdbe68fe410f277f274114c85ef2b7f7d1feaf9eef6b66ce637a579f48f463e`  
		Last Modified: Tue, 03 Feb 2026 03:12:18 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f728163862540860a79d8529605f7bc8be06ca0e927e0b7a881a2de96568e3d6`  
		Last Modified: Tue, 03 Feb 2026 03:12:18 GMT  
		Size: 4.2 MB (4151342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8aebb7b1666736f3b2e9232d327d759905262dfbb0c6018a720af81f06e5e3`  
		Last Modified: Tue, 03 Feb 2026 03:12:18 GMT  
		Size: 1.2 MB (1220293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ded14bf135e2c61b5c8ae5c958c2e9af341f86272881c71933dbc14e5f802b`  
		Last Modified: Tue, 03 Feb 2026 03:12:18 GMT  
		Size: 8.1 MB (8066604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a5f9f42d84eafc256c2b86df7102162fad22473efda6b84e2367bc3f5e41be`  
		Last Modified: Tue, 03 Feb 2026 03:12:19 GMT  
		Size: 1.2 MB (1195073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb4529c7eee83451a934ec5debe3a423de249cd6f0d56aac3734ccada1ff435`  
		Last Modified: Tue, 03 Feb 2026 03:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b061a677d8f153f00274f440c26d32dac20ee7be65c46cf88b335ac1d7c16e`  
		Last Modified: Tue, 03 Feb 2026 03:12:19 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3cb6fe923d7af6c0777bfad14f3c16bd0c59303fd69cf9e5a4e3ea8ef6b583`  
		Last Modified: Tue, 03 Feb 2026 03:12:25 GMT  
		Size: 107.6 MB (107602918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad1e2abc4de2b4b54604697ead451e0f7746061c869815e9bcd60902f437d01`  
		Last Modified: Tue, 03 Feb 2026 03:12:21 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c91a56b7d3755811c7199ae5a9e55e93e1046a466a688068904f71a05a7e42`  
		Last Modified: Tue, 03 Feb 2026 03:12:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1305896b128dfd13c80337f02e5d728f5d86b0937fd64d148e50fbb8e50e9f76`  
		Last Modified: Tue, 03 Feb 2026 03:12:21 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f2cbe111c7a8323c610d2d0512a681ea801064df9ff39b47f924a2257906ad`  
		Last Modified: Tue, 03 Feb 2026 03:12:22 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84df6008e44541a3ec7704400bb1cba3600708175622a7d3d5ce435b239e3af0`  
		Last Modified: Tue, 03 Feb 2026 03:12:23 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7b5804b96fbe008b053f6c6b71e0eb7fc33c8b0e00285aeefbeb45a759f66bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db222b999b878c1f158c2103e0dae94fcea8562af9237420da9a2a0d6782fa38`

```dockerfile
```

-	Layers:
	-	`sha256:c3dc44a7cfc8f144f62aa18f323cb50b8f4aa8af13aea2de0811db4a27593527`  
		Last Modified: Tue, 03 Feb 2026 03:12:18 GMT  
		Size: 5.9 MB (5927653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204155e1fd3062a464529db0ad4286f86196533c2551b94fdaedf8dec327d9bf`  
		Last Modified: Tue, 03 Feb 2026 03:12:18 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:79fd51fb7fd77ea998fe3892379a9290bb50f93d679d75446e915cbf846c3f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143058712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc562bdcefd1aa099eaa706cb7adaa04e5388a9c2c2d5413ddd080fb7c68640f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:12:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 03:12:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:12:48 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:12:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:12:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 03:12:54 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 03:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:12:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 03:12:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 03:12:58 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 03:12:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 03:12:58 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 03 Feb 2026 03:27:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:27:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:27:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:27:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:27:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:27:29 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:27:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:27:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:27:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:27:29 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:27:29 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:27:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac7fb96c04f03478bcf4f0642193545832935ad61227e510c697207e70551af`  
		Last Modified: Tue, 03 Feb 2026 03:27:46 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa84b6794c582de4568407709eb8a83870ff6381030a8f967b3878539196132`  
		Last Modified: Tue, 03 Feb 2026 03:27:46 GMT  
		Size: 3.7 MB (3742679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e60487b2a73988ce900dd0171826161a8f5aae1efc15b525c68af09b2c883b`  
		Last Modified: Tue, 03 Feb 2026 03:27:47 GMT  
		Size: 1.2 MB (1216127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafc0597cff342a47478c23b302bed4b55a2012d46142080e4762dce97a0aaa9`  
		Last Modified: Tue, 03 Feb 2026 03:27:47 GMT  
		Size: 8.1 MB (8066417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1e6d1c3661fefb0e126d526f4596bcb2b5815ab62bba719763cd3dcb2cdfd3`  
		Last Modified: Tue, 03 Feb 2026 03:27:48 GMT  
		Size: 1.1 MB (1067279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ae4306740854b04e8a7fe7d25fbf29dc3f17d98ba0c9bea3e5d42c7236b1a1`  
		Last Modified: Tue, 03 Feb 2026 03:27:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe5abb364f8520bcddada0f86d7161e29d48b84536699e43db31c7126533c4c`  
		Last Modified: Tue, 03 Feb 2026 03:27:48 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd796c357a245def85cde5821a064b2e7938f4d7bcc302de6543e3a87ffce264`  
		Last Modified: Tue, 03 Feb 2026 03:27:50 GMT  
		Size: 105.0 MB (105011444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c072bbd7132105097a8b3674e365bc2c405227cedd90a466cf2100222ccca11`  
		Last Modified: Tue, 03 Feb 2026 03:27:49 GMT  
		Size: 9.9 KB (9926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c01e1ba4f71e4868afab6d910024e6b9c77d8d9b5b889c5be8d1bc4da3886a7`  
		Last Modified: Tue, 03 Feb 2026 03:27:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa670ad9a813de824424cb5101aab663c93969acdd1161167925179c242d17c`  
		Last Modified: Tue, 03 Feb 2026 03:27:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e67b06979e5e1a88a301d47813226ec61bd5df913850085836f11596baa07c`  
		Last Modified: Tue, 03 Feb 2026 03:27:50 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5f3ae8205f6e8ac3f949e6fe72bb597616de633f5c43dc433c2311f2ff0dc0`  
		Last Modified: Tue, 03 Feb 2026 03:27:50 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:83a26d7255d24d404375d595862773b5752c3eb8afb900732857667398362009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff64e6e807f1e26433dd16c8d3743bb23a68bb129e4f8e8b4f85b681f60051a`

```dockerfile
```

-	Layers:
	-	`sha256:a219c2c4ad57f5f5cc1d7d9df02f773dde3903b2cd16b24bc188b8080591b977`  
		Last Modified: Tue, 03 Feb 2026 03:27:47 GMT  
		Size: 5.9 MB (5926908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285625a68de24943de58b3e99eb042fc3a29f9fc9b8833297169ad6c0d11f444`  
		Last Modified: Tue, 03 Feb 2026 03:27:46 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:5f2eebad70059500e64b16c7a31d38d19d50a70165774dc99950f8f905f7f1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153016382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c834a134d3388963519f4eb7304a8071d4b87dbead038b21cafaa3e787229b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 12 Feb 2026 21:04:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:38 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:04:42 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:04:46 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:04:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 12 Feb 2026 21:04:46 GMT
ENV PG_VERSION=16.12-1.pgdg12+1
# Thu, 12 Feb 2026 21:04:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:04:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:04:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:04:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:04:58 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:04:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:04:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:04:58 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:04:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:04:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f247e27971122035411512f32fe971015b30eb62b5a7f6faaa8964222b043fce`  
		Last Modified: Thu, 12 Feb 2026 21:05:18 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc3aa0c2e3f9c50361a362cda97854b0d3d4d37a03c905b0517b81a1f563496`  
		Last Modified: Thu, 12 Feb 2026 21:05:18 GMT  
		Size: 4.5 MB (4519450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f4cb437a52be2ef97f7f31b80d20a017cb5148a91e4c765ae4588b8e91eb4d`  
		Last Modified: Thu, 12 Feb 2026 21:05:18 GMT  
		Size: 1.2 MB (1203283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725a797bb153a1f3bd53555158b1c47f4b4095dd390ee89cae586d365ba528b3`  
		Last Modified: Thu, 12 Feb 2026 21:05:18 GMT  
		Size: 8.1 MB (8066464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f908491f97add07c8973b4a634fbd77e9b1f98740cc9e737a86031d2ed206a0e`  
		Last Modified: Thu, 12 Feb 2026 21:05:19 GMT  
		Size: 1.1 MB (1108994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb73b468792a54f6ca65bec9d6b30969365e8d0752fab728032e2e9d6724c89`  
		Last Modified: Thu, 12 Feb 2026 21:05:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b726b69119a580b7c2665d89ac7f52b8ffa992aeb7e2f9c0bdeafa34811ef73`  
		Last Modified: Thu, 12 Feb 2026 21:05:19 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d39518c45818517af971c8c34fe65d66df81a6f59e2a117d276aa8bb598317c`  
		Last Modified: Thu, 12 Feb 2026 21:05:22 GMT  
		Size: 110.0 MB (109989653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f929961dbfe6304e4b3bad48f004d5a41cad3bac13f21189aa3dd76b6032ef`  
		Last Modified: Thu, 12 Feb 2026 21:05:20 GMT  
		Size: 10.0 KB (9968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eeb772868d5b91b229f39f3e17a130d014b036ba0fe86d69b8b3060dfebcec`  
		Last Modified: Thu, 12 Feb 2026 21:05:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb1bced29a3f58eb9189c08474e5a88ac8b8b89ae61a92fb8d55485750fdb22`  
		Last Modified: Thu, 12 Feb 2026 21:05:21 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f27bf23c5218be8f2ff37283ed7f83be295b5fb75830c747585501f755a6de`  
		Last Modified: Thu, 12 Feb 2026 21:05:21 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b1f395b8dcb91a40bb9a14aa8901e725e1bf80512df9171c613aa310b14af`  
		Last Modified: Thu, 12 Feb 2026 21:05:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0beb3ada6fa1f545671383610241d2829379266c711f9f1b8c105d923cc34ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5969408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf357132885b5e4ebb6ba19fa6a9a317e63534d55b38b870beb2e6a6fa2d1ae`

```dockerfile
```

-	Layers:
	-	`sha256:e00abe693562992f08b9512322a83dc73a90e343741d18969762d23d4c3c100e`  
		Last Modified: Thu, 12 Feb 2026 21:05:18 GMT  
		Size: 5.9 MB (5915867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6301f1e13887ddb23170678b01741683ff4c6166257b43945009bd95a8269f`  
		Last Modified: Thu, 12 Feb 2026 21:05:18 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:71fe8ef19f1e187debac099b4d3f3b9ed9d618cfd6f69f4ad1998e648aaa8090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163797991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee195daafa3c49ba4003671a8358a8f9880fed6c899d5750c95fed1c585e4546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:37:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:37:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:37:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:37:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:37:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:37:43 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:37:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:37:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:37:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:37:47 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 02:37:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 02:37:47 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 03 Feb 2026 02:48:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 02:48:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 02:48:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 02:48:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 02:48:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 02:48:52 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 02:48:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:48:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 02:48:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:48:52 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 02:48:52 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 02:48:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f93d228262ac8f12d9af5f87a89d9722b3f4d559df30edfa91327db9f457723`  
		Last Modified: Tue, 03 Feb 2026 01:13:52 GMT  
		Size: 29.2 MB (29210015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a9305b63766602f209d4f79f7875e8be62051cc9133db7cfa73e8f78adf190`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6d762538c006c9e47d86afac7d8c534a0813aa8bc4c962f2ff856ff2e55c8b`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 5.0 MB (4966111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dab1a65ef2a1ba51ecbbf9a65ef36568cc49c0ab18282446d262faa9ee79fc`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 1.2 MB (1218656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28487032489ca397dca96759d418d1538393e331cef01b12c9814fb336700172`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 8.1 MB (8066401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd1f4a36819e75499d5327b86017c4e2abe9d6f1a28cdf0a2738213065e86`  
		Last Modified: Tue, 03 Feb 2026 02:49:14 GMT  
		Size: 1.1 MB (1137506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f041fe79c272cc2a21a8cfb7c3a49f6ec6b14463e736218999498ba71611dbaa`  
		Last Modified: Tue, 03 Feb 2026 02:49:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05deabe4e4d281b5a2ddbcaf271f6e036c703726421e0b75c140ecfcceb279cf`  
		Last Modified: Tue, 03 Feb 2026 02:49:14 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088cd52967a1b6af5d4c7254abf6a6bef0fb0c58384ff8be013269208c2046d1`  
		Last Modified: Tue, 03 Feb 2026 02:49:18 GMT  
		Size: 119.2 MB (119178624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672e2606b7805a7ff37f8581df59ef2817a2a0b5cfa820c52275c886bf920113`  
		Last Modified: Tue, 03 Feb 2026 02:49:15 GMT  
		Size: 9.9 KB (9927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a54a8ae5e264d2a636c9c861be30397177e289376f500b5c61f916e2aba46`  
		Last Modified: Tue, 03 Feb 2026 02:49:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a4a01c16bd1635c21867c39dcc98929b717d5266abcd1ee101d8cf0bd72b07`  
		Last Modified: Tue, 03 Feb 2026 02:49:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e6f3d7397d670e2ef025b6af7801035c28bffba0bc22d4127ab355994bb1fe`  
		Last Modified: Tue, 03 Feb 2026 02:49:16 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfaa34186f523b77dafdfd9027619d60c4144eab0c5eab689c0629289e97620`  
		Last Modified: Tue, 03 Feb 2026 02:49:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:20553840083c4ebf54a5b7293b8ef3b14248ed5f10a08184288783f889948798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5979048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577c15b1696f795a3631d9c480269ccdd0f70a3a3d0537b895b9ccb867b5efdb`

```dockerfile
```

-	Layers:
	-	`sha256:e070e16f666009a8d21ae1bf1422e01165f6dbd84b565adc9940017f53f31c4e`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 5.9 MB (5925796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898aa54ef2087ed5dee1ba230b0afba5ae86445e18fd197234e713ce4859310c`  
		Last Modified: Tue, 03 Feb 2026 02:49:13 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:d482156c8463d2669c2b638e55b79340f03f11a57d8871505b2a2460a7de5b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153856318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ba2c9d4fe17ce8d8796e18204b86c332117d19a95b632c5c4be52b1fefbac9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 09:35:01 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 09:35:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 09:36:10 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 09:36:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 09:36:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 09:36:37 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 09:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 09:36:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 09:36:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 09:36:59 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 09:36:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 09:36:59 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 03 Feb 2026 13:09:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 13:09:33 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 13:09:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 13:09:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 13:09:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 13:09:37 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 13:09:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 13:09:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 13:09:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 13:09:40 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 13:09:40 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 13:09:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1fed8ed52dc6e52b96afc1da0ccf85c92c81820372fc78b006f957e9c58ff600`  
		Last Modified: Tue, 03 Feb 2026 01:13:02 GMT  
		Size: 28.5 MB (28513693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be57c3ba81b4ac90997ae4ca2bfa72870d73cda681c63e05d4836b8f395adf1f`  
		Last Modified: Tue, 03 Feb 2026 10:49:37 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013d2d5628df691f06f45f710bcb1b44aed9769c77bc7f50b52f50fca279fa8f`  
		Last Modified: Tue, 03 Feb 2026 10:49:38 GMT  
		Size: 4.5 MB (4475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af63bb6f60b01fed4a25d6a3722cbae5824c5b0a2302a19cc28c4f2ab7d51310`  
		Last Modified: Tue, 03 Feb 2026 10:49:38 GMT  
		Size: 1.2 MB (1159234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0e9b472f25b51bdc95ecde3e4ecd15aeee9d7975fcdb830253e64184ad02d9`  
		Last Modified: Tue, 03 Feb 2026 10:49:39 GMT  
		Size: 8.1 MB (8066713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1dbb13126f432f030c3381fb1cb9226cfe24a7d47f5d814262ae5455af8dfe`  
		Last Modified: Tue, 03 Feb 2026 10:49:39 GMT  
		Size: 1.2 MB (1182915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081d071f591f199e1e6fb50793088ee6881e12eee0be6576fee5446c312182d3`  
		Last Modified: Tue, 03 Feb 2026 10:49:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a65651ab9bc8110d6a34778e2e8fca4b3a9cd37df796e505cbc35831d060bed`  
		Last Modified: Tue, 03 Feb 2026 10:49:40 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6459b757fc29d6bf1597d2e93645032a06305f88d150dc763377d87fe5e132`  
		Last Modified: Tue, 03 Feb 2026 13:11:48 GMT  
		Size: 110.4 MB (110437884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc1054ebc17a2c1c8904b94a00d4e5e8de5b8f4eb8c8d94ea3590368b7f8d45`  
		Last Modified: Tue, 03 Feb 2026 13:11:37 GMT  
		Size: 9.9 KB (9927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a78e321495400fe363d05a1b80d85c00828e157a32da47750a3380a6d6728c`  
		Last Modified: Tue, 03 Feb 2026 13:11:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b184a5b44d7498cf88496bd5c91ec095df9e72fdd816770f7b69392f4ded3fb`  
		Last Modified: Tue, 03 Feb 2026 13:11:37 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3e52f3937218f748ad2b01582bfe6ba54226bc63fd8008f6bb7cec917d0fca`  
		Last Modified: Tue, 03 Feb 2026 13:11:38 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc90853a5b07c39a595cb2593c8dfab02b2e3e71853fa0a4d302ed63d26eaad`  
		Last Modified: Tue, 03 Feb 2026 13:11:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1dddec028c77f59e47cfb5442d4f8cabd851c65b7981fd63b359f7997cb54666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008816131de8997b0b51a474189a732772bd05e99ea522de636ae0b3c5f70bf1`

```dockerfile
```

-	Layers:
	-	`sha256:a744d684a9dc4e82ff4e8fb1b89c5bd7b17babe3d3c15af17b76d2148d043124`  
		Last Modified: Tue, 03 Feb 2026 13:11:37 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:cffe2c0607bfd1682ffa1fe4dec58992f1d2bcb53dc1501ad88a7eb044198a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167754344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d189e2993be1a553b88f08e11da4f23d9cd29b8a0b20672be6871a7027f6e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:02:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 05:02:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:02:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:02:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:03:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 05:03:04 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 05:03:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:03:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 05:03:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 05:03:14 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 05:03:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 05:03:14 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 03 Feb 2026 05:07:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 05:07:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 05:07:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 05:07:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 05:07:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 05:07:14 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 05:07:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:07:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 05:07:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:07:15 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 05:07:15 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 05:07:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0941aae1f81fd36142e5841137e9916c17539131ecdda93dc3db9d3e88de00e`  
		Last Modified: Tue, 03 Feb 2026 05:04:46 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd6aa237b3c419cd31c5727eb0389fe8a307747b005fe706c311f113945736c`  
		Last Modified: Tue, 03 Feb 2026 05:04:46 GMT  
		Size: 5.4 MB (5368542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729665cfa88f38bb396d31c4778e3344c9779ea7d73b405294cde03f1d65b7b6`  
		Last Modified: Tue, 03 Feb 2026 05:04:46 GMT  
		Size: 1.2 MB (1208143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6043a1fb9779944ee5dc248909133ff85cbb3df5f327906ea15a7499bf36264d`  
		Last Modified: Tue, 03 Feb 2026 05:04:46 GMT  
		Size: 8.1 MB (8066547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c6c7394d0ea200eecd5ee1408119b54acd48d71f357b2c370b98c57fcea42b`  
		Last Modified: Tue, 03 Feb 2026 05:04:47 GMT  
		Size: 1.3 MB (1283638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a0d5c1543081948505ebf8778d4eb99f97fb1397c7e25c6ad05e1bf98d80fb`  
		Last Modified: Tue, 03 Feb 2026 05:04:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db36b12176106420d5dc0c0e963f17a31a801d6bbd2d412606abe17d214f7676`  
		Last Modified: Tue, 03 Feb 2026 05:04:47 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84730c28d0539ee60bd3382bbd68910eefbe80dca551212e6392e505a8963d32`  
		Last Modified: Tue, 03 Feb 2026 05:08:03 GMT  
		Size: 119.7 MB (119738096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f6bf2930c3823be12753c8b61f53b7b4b69bb4c1f6c1aee372a34dc9bc4dd1`  
		Last Modified: Tue, 03 Feb 2026 05:07:59 GMT  
		Size: 9.9 KB (9917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9984b1c362c36801002aae90a04c78e4eec447d6c3c1657d7a2751032e38ca10`  
		Last Modified: Tue, 03 Feb 2026 05:07:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef837327d14b309df0763ee54c070df8ca099c7399d1e5a65a0af024000fa63`  
		Last Modified: Tue, 03 Feb 2026 05:07:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51217704794ecd4150d213b81616c7d700aed75fe41e0d7840aa8f8cbe49d15`  
		Last Modified: Tue, 03 Feb 2026 05:08:01 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320b71cc1853102b29cbeac1bf12f11f4fa8b0b4d091ba1455b920461c003f15`  
		Last Modified: Tue, 03 Feb 2026 05:08:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f04dd1dab1fe2c4d8c27762fd41b4ab3e3170a65997ae2ce99df06cd1395ffaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12eb3d59ab67e021ba5f05e849a5cbb0472523afa73b0c8f382023a5a91458a`

```dockerfile
```

-	Layers:
	-	`sha256:63f81ce32bf7a78d51f67364d557808ca36c584f34b5dfe9a921b7daa7b17d72`  
		Last Modified: Tue, 03 Feb 2026 05:08:00 GMT  
		Size: 5.9 MB (5916917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4737ec07f62d906267db1d46834fcd38e10af8cec5f7a6ab2ca163a60bde507d`  
		Last Modified: Tue, 03 Feb 2026 05:07:59 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:b7ed871b432ee651a758970b8157fcb8a5dbc5f6bf32bfa5b46b2acbfe1f1b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164227216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea936adae61be2a67e84c178a4944b8372b8a406d87601e133ee8dbc703c5d3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:24:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 03:24:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:24:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:25:02 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 03:25:02 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 03:25:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:25:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 03:25:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 03:25:06 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 03:25:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 03:25:06 GMT
ENV PG_VERSION=16.11-1.pgdg12+1
# Tue, 03 Feb 2026 03:36:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:36:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:36:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:36:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:36:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:36:25 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:36:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:36:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:36:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:36:25 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:36:25 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:36:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b83d74613abbc7387175d2ab2448da8869fa392688d523923b92a23fc25e1`  
		Last Modified: Tue, 03 Feb 2026 03:36:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d8bae1607270024722f2500dd5813fc3fbd09a03fbf71f53ef9238d5940f0`  
		Last Modified: Tue, 03 Feb 2026 03:36:54 GMT  
		Size: 4.4 MB (4391202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3645adcd79056eb0925d98cbaf78a6dd1831ed60b76224abd60b03d9d1df85f`  
		Last Modified: Tue, 03 Feb 2026 03:36:54 GMT  
		Size: 1.2 MB (1222786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd14e9939fefdf67a41fb4681e731e7b190d382638f15519a241709a696bb463`  
		Last Modified: Tue, 03 Feb 2026 03:36:54 GMT  
		Size: 8.1 MB (8120731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be14ab6f4e5607371ef579a3b0ab09a9cd983dd748af7e65fb53b8579d638179`  
		Last Modified: Tue, 03 Feb 2026 03:36:54 GMT  
		Size: 1.1 MB (1097076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b75fe51aed34849431039cc74046e5ca1e06f223c76bc934d026d6cabfe0c2`  
		Last Modified: Tue, 03 Feb 2026 03:36:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1b50be1196e268256060c2b5ee9ab85547ff9351fff13cb4d6897c83988855`  
		Last Modified: Tue, 03 Feb 2026 03:36:55 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed3727b207b2581de9f721c3b7ddf5557ff5a38c6897e124e971246ba22cdb4`  
		Last Modified: Tue, 03 Feb 2026 03:36:57 GMT  
		Size: 122.5 MB (122490355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b265304a6d6fe161e411bff535c9a1fc0a62a828efe5eb1971fadfe2519b560`  
		Last Modified: Tue, 03 Feb 2026 03:36:56 GMT  
		Size: 9.9 KB (9927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c48c64bd36e9d953b139bc772597175ab51f482055587fdad96f505fba51ec`  
		Last Modified: Tue, 03 Feb 2026 03:36:56 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed44deb9063e32364b52ec875b7741c770339e5de2b686cb1a25f5820238da7`  
		Last Modified: Tue, 03 Feb 2026 03:36:56 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ba75fa5451ef5957359a6d872e0c64ee43ca498fe60aecc0c279f4d6d8cdf9`  
		Last Modified: Tue, 03 Feb 2026 03:36:56 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965ee5c42a80b0421f7c6360527767bbfcf83bf564554de28dcb2e6a505c241d`  
		Last Modified: Tue, 03 Feb 2026 03:36:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d259f7e2829aef764ce191f5a60d1d8934eab8aa39ce5096a0d688ea12a615ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de52a7ca091cb91596031f183b4c2655af51ae05b148d9d4ba566e0876551f3f`

```dockerfile
```

-	Layers:
	-	`sha256:2ea82662330a5e0dce02896f370f43beb16d539f086045870c61c99fb9283029`  
		Last Modified: Tue, 03 Feb 2026 03:36:54 GMT  
		Size: 5.9 MB (5922272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816ac7a4415d715157b9578f174760a353fb5b7b96e480727d965b66ec9dedb9`  
		Last Modified: Tue, 03 Feb 2026 03:36:53 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
