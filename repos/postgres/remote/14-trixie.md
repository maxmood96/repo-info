## `postgres:14-trixie`

```console
$ docker pull postgres@sha256:8186cfac504299f28d9cae925b703bba6c758f5648793a1b5fcd8d89f9569826
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

### `postgres:14-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:77a643f92519aa98aee0c3849b8897d65d760863cc2d8e919dc82f4558896dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156928784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3591ffbfae811e19068d018a090962aa28ad6027ccbf4100975233831881f8fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:38:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:38:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:38:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:38:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:38:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:38:27 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:38:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:38:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:38:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:38:31 GMT
ENV PG_MAJOR=14
# Mon, 29 Dec 2025 23:38:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 29 Dec 2025 23:38:31 GMT
ENV PG_VERSION=14.20-1.pgdg13+1
# Mon, 29 Dec 2025 23:38:45 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:38:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:38:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:38:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:38:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:38:45 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:38:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:38:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:38:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:38:45 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:38:45 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:38:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f2a074a11f0dcde7abebf48157e1fc6d6096371b13f26b32b0d68b3a57c23f`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363b9d55c6f4067f3c6863c645045834d5f4a8f4191eec8e0dfeb8c1200ba602`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 6.4 MB (6436605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d7f96802b132317a84637fd90e720c82baaf7002d20b814086c6aaa3b6fc34`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 1.3 MB (1256601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d1fadcabe0103f356f147ee8318dcd1dc4a25662d45ef310e8ff5b19b3eb3c`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 8.2 MB (8203736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfdfd13ebc479a75c93d98e6828985d9f27665e363ec6ff8a21f4a7f9422c42`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 1.3 MB (1311498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03667b8e3361c1c6538216a98237f901c6d6db4dbc4d39a158dcd210f6f5ae`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4becb2274bb526a5d22f0df967ed500ebbb633f91f56d3d2c5cd366341f46e32`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e806e0483431380d338496da7cfa0f39060fc164a653d6d0bede3faf7908bc`  
		Last Modified: Mon, 29 Dec 2025 23:39:19 GMT  
		Size: 109.9 MB (109923444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5209bc1a57754281d9861326ce4cf27773cf2bcf0cece82c2a926d65a136fb6`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8255285ed8478d580ff6da8f650877fbf15c06a5e79d2bb65e72b9d2aa881a`  
		Last Modified: Mon, 29 Dec 2025 23:39:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53edcb07ce71323aa948da29845d41ac5147038f563b755fed1dc79a4b23a69`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9759b2407941e7056f31367c627a7887543b44e4f91b6008f56619002fd202be`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b06d3f407d0ab288e8465926beedd8c6030f7ce23e6374d23306ea2724cba1d`  
		Last Modified: Mon, 29 Dec 2025 23:39:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:79f0ca1f167400b4ba3610f8a58d0168a1b7626390cdb0c69b23eabd3d7118a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5645599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a06483d62eccdb52065bc5eb6a412f90f814bd95a11f0171818bab71ae3612`

```dockerfile
```

-	Layers:
	-	`sha256:e3b12f7568bcb25e311687fb78b8ffbaf092bc40acffe8f9b4a712116d1d24e7`  
		Last Modified: Tue, 30 Dec 2025 03:08:18 GMT  
		Size: 5.6 MB (5591735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f794f69d06e9cf2056cd66f6ac801b5f02ce31d5ca0329075366b0d5067ec70`  
		Last Modified: Tue, 30 Dec 2025 03:08:19 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:1c7e4da352dcb0c8eb3ea739b084a475cf6a0206ecc13b92bb159087e8912bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150973615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b403e8f449f5376ce03db42d826ff1b26dcf164b85e59d30f29190a270a7363`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:11:41 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 00:11:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:12:02 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 00:12:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 00:12:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 00:12:11 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 00:12:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:12:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 00:12:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:12:18 GMT
ENV PG_MAJOR=14
# Tue, 30 Dec 2025 00:12:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 30 Dec 2025 00:12:18 GMT
ENV PG_VERSION=14.20-1.pgdg13+1
# Tue, 30 Dec 2025 00:28:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:28:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:28:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:28:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:28:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:28:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:28:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:28:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:28:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:28:02 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:28:02 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:28:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebca39f8bd75ad40180e31c93e4fb5e1358d20505e32462fc6a3f0b765d5bc2`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dd8a411fc6ec0c68ebb09bd1f836335596fb329b0915ebd3da135aa1002343`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 5.9 MB (5928996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44b9152a9e07e83a74aebf375d63feb4f4030f6ea65005b398a4b6f3d8e91f3`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 1.2 MB (1227394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840236e9d3cff6ee32d76434aa96d3470ec005821867fc1e5f31fc0ef36fb601`  
		Last Modified: Tue, 30 Dec 2025 00:28:33 GMT  
		Size: 8.2 MB (8204181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b046043d3ce66cf53aeb8e603d50308cdee723dfb4e75ea39b56cabc2e6d51f`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 1.3 MB (1317201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe6e92ed588d9b4dde079b9821ba1a0ae0133d22e52ef534268dbe541b21fe0`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf74381007d47794fe6a3ec17e0fc5023bcf9e0245ef98d9d898b3eea82401df`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6878ae9d1c56c4f52926e5175910a66bb2e201b59bba5a8e7900c22866a971d7`  
		Last Modified: Tue, 30 Dec 2025 00:28:40 GMT  
		Size: 106.3 MB (106331335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d2656926796c08d41802294e3e0e1e1e837a972162ccdd9a0f146b642b4ab6`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd62d7a15f39c2f11f0853ddd90cf2d3c43412de5a65a458244a70e02e30c14`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746fe4ec871ffc47c4f5ba8cceb86f976769c545b53d7b1e43459e4181a26db3`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4926f47bea551589623eb560a9b4b842b3857ca51fc4d951f957943d9218464a`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5e31655245399a3aeb13af675b1f0e6455d8ed3102ea870f10d0bb2d48bbb4`  
		Last Modified: Tue, 30 Dec 2025 00:28:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:74f095df31102bc31069d180cd50fa1f049d48951fa729c1e15b050372f3d7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5662460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b832a93b6d943313e6fb0cf21e711d613f325f2f80703567bc4ab859d9dc1ec6`

```dockerfile
```

-	Layers:
	-	`sha256:f268790129c411814040022d3985491310cb078a3ac491dd63e346677870a16d`  
		Last Modified: Tue, 30 Dec 2025 03:08:24 GMT  
		Size: 5.6 MB (5608373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ae788d6243562eec9dd866a4205a8c62023e6bda7bd27ed3f2e632346106e76`  
		Last Modified: Tue, 30 Dec 2025 03:08:24 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:2118c348805669aeebd676ce0f835b34efe85e1ba21a46067cff3cf63c76fe65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146086774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd7019e4bcfa1dfb09ec1382c4afd9946870648450508374c4d66cf5055a0fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:14:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 00:14:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:14:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 00:14:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 00:14:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 00:14:46 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 00:14:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:14:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 00:14:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:14:52 GMT
ENV PG_MAJOR=14
# Tue, 30 Dec 2025 00:14:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 30 Dec 2025 00:14:52 GMT
ENV PG_VERSION=14.20-1.pgdg13+1
# Tue, 30 Dec 2025 00:28:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:28:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:28:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:28:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:28:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:28:55 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:28:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:28:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:28:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:28:56 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:28:56 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:28:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a177a90c8fe7fb754639a37ba68b0d63040ad4f33d22e0cd9da4be17b70d98`  
		Last Modified: Tue, 30 Dec 2025 00:29:24 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26463cdb30eb17eb384ab4fd92290fd0025b6a77914bccf4dd79c3535e31f5`  
		Last Modified: Tue, 30 Dec 2025 00:29:24 GMT  
		Size: 5.5 MB (5496807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1f4a4916eb17d4c458b85d14963d1268b2b165387c9be1b6c3d3083ef03dbf`  
		Last Modified: Tue, 30 Dec 2025 00:29:24 GMT  
		Size: 1.2 MB (1222183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697e908be1bfea214687c2a54511c406b127a60ccb5a3b24d6138e5677f36ff8`  
		Last Modified: Tue, 30 Dec 2025 00:29:25 GMT  
		Size: 8.2 MB (8203941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f569ffccc0f0878506d5b9c4f6deef3c3ed315b747ae784c5eb6dacb6d2fd`  
		Last Modified: Tue, 30 Dec 2025 00:29:24 GMT  
		Size: 1.2 MB (1172437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ca65d38f0298a8f469cdca8ee871b6fe11b9fca2a0426e47b5dcdacba23642`  
		Last Modified: Tue, 30 Dec 2025 00:29:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fde318d6bfdbd84162135ba6d8ce1526c3fb15c90b285eb8c74a5b16ce0170`  
		Last Modified: Tue, 30 Dec 2025 00:29:24 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2d8906fb531c4060e46bf8ddc236522b77af048d2d164804f4ff7c4a2e801a`  
		Last Modified: Tue, 30 Dec 2025 00:29:35 GMT  
		Size: 103.8 MB (103761026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e063ca59197050768a2ac002fc42b94687426d4c0975d7ef9c90265ae7301dc`  
		Last Modified: Tue, 30 Dec 2025 00:29:24 GMT  
		Size: 9.6 KB (9634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3e51e3e4cd1ef1b03df699abb250208034ec3dd2f6a887097f97d3a853442e`  
		Last Modified: Tue, 30 Dec 2025 00:29:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f004b3593a2f4c7341e1439eee9c937a64ba5311adfa13631c6360fe88ec8fd0`  
		Last Modified: Tue, 30 Dec 2025 00:29:24 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef33dec7b49f71b1fd22ac3e420481f25b2979b7e9c76491e823d8c7f62e54ca`  
		Last Modified: Tue, 30 Dec 2025 00:29:24 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc385ed4a4a103ceb1fa9bcba99c4879e05c9118be2cf763fb64a985a3616ba`  
		Last Modified: Tue, 30 Dec 2025 00:29:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:935f52270554c2c54e09c0367efe2e0a4b1d2c7b642e1fbd9b378f5c58e64650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5661765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb29f5cf6d79a92b08edd1a62513f9a0fe7333cac1884d9872fea8cf33798df9`

```dockerfile
```

-	Layers:
	-	`sha256:19d199cf1f4fef8e802c5d14617207e85b356bcaee8fd4cd7e111bbc2b6c117c`  
		Last Modified: Tue, 30 Dec 2025 03:08:29 GMT  
		Size: 5.6 MB (5607678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bae3c4e14d85ad677fc3344b02a438136a2b7f46ce5513960e16185ef06e8a05`  
		Last Modified: Tue, 30 Dec 2025 03:08:30 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:00388ce2f37595c9ed80934d91d594d70be41e7fc5c6ede5091002fe036cb712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155561587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81be62857dc52a48d08d4052cd64c7e39fbc210f464584821d25bf2272bdbd3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:41:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:41:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:42:01 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:42:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:42:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:42:06 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:42:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:42:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:42:11 GMT
ENV PG_MAJOR=14
# Mon, 29 Dec 2025 23:42:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 29 Dec 2025 23:42:11 GMT
ENV PG_VERSION=14.20-1.pgdg13+1
# Mon, 29 Dec 2025 23:42:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:42:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:42:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:42:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:42:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:42:29 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:42:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:42:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:42:29 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:42:29 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:42:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fdff07dbc58f7d825f0497d343e4e921a616ce7960576c355a375ca93ddfbe`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a630b65d62f7e3f6c9cac3a55bb08049df892fddaa1918475a95b55be0fb5d66`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 6.2 MB (6232058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a5c54d98a063f4aa6d0cd4b0a6f1ded5a307f3f57a7a211e1f67c113963bf0`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 1.2 MB (1209492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a8c76303c7ce3c708ae10ea4799810a2205151eb276e82a7075eeede3b1699`  
		Last Modified: Mon, 29 Dec 2025 23:42:59 GMT  
		Size: 8.2 MB (8203933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c830fd41b81bfa8f76a1e0d7d945d15b5d55df79caf287f5c36444fc819dff`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 1.2 MB (1220447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78bad8beab6347ff78b2ea773984af6329ddf6943915f2918aa2e04079bbac4`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9276647c9b3d9188676c621831304c544a6a249b967313cd3be07284745f51ce`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea60dfd27f7ef7abe2173c046b820d1135abcbebc492c2a5703daddff4f6b33`  
		Last Modified: Mon, 29 Dec 2025 23:43:04 GMT  
		Size: 108.5 MB (108536655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f168f0945efedff00088aac4287d0a6f3fdb860f3ebc980e434e5ecbde1128b3`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebb23953aa9bc1d43568b7c4fe7e1b66805bb8c2a9ee30142d3fb59994fd347`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8f991b75401ec03797b632dcacc058c3aa05ffc282fd51cb87eeb438175938`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b327b0e423674e5a2898e4813e189318c8ba10d32bc1f186fbdf9b1e9572e8`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709367a4c2366a8ea4afe8f90952e0b4db506d88c44f62dc598c7e065834ae95`  
		Last Modified: Mon, 29 Dec 2025 23:42:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3c0fbb9678269a94c075e39bb7c749711cfbd5ba54bb93fbe8ea12bc1f1045e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5652214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:439069187dca0f973a825f674a04526b85b96a732a9a15b80da7a9aaa72f8b17`

```dockerfile
```

-	Layers:
	-	`sha256:f4babab31539947602c2ea80671cfd136b5f1e62a42540538ab6e9172090d86d`  
		Last Modified: Tue, 30 Dec 2025 03:09:16 GMT  
		Size: 5.6 MB (5598081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd2d69b33f500da25d298daaa11ef953a1e79802df0e7e4e0391b8976a276db2`  
		Last Modified: Tue, 30 Dec 2025 03:09:16 GMT  
		Size: 54.1 KB (54133 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; 386

```console
$ docker pull postgres@sha256:b59138735f14835cfdbf89106cf1aa369001c4b52326191959cc5c8dcfb1f87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166004163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5af174e428b8cbec023ec112d9d9e118f79705116fab2ef93b7194656518c63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:35:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 29 Dec 2025 23:35:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:36:06 GMT
ENV GOSU_VERSION=1.19
# Mon, 29 Dec 2025 23:36:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 29 Dec 2025 23:36:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 29 Dec 2025 23:36:11 GMT
ENV LANG=en_US.utf8
# Mon, 29 Dec 2025 23:36:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:36:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 29 Dec 2025 23:36:15 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:36:15 GMT
ENV PG_MAJOR=14
# Mon, 29 Dec 2025 23:36:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 29 Dec 2025 23:36:15 GMT
ENV PG_VERSION=14.20-1.pgdg13+1
# Mon, 29 Dec 2025 23:46:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 29 Dec 2025 23:46:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 29 Dec 2025 23:46:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 29 Dec 2025 23:46:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 29 Dec 2025 23:46:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 29 Dec 2025 23:46:05 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 29 Dec 2025 23:46:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:46:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 29 Dec 2025 23:46:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 29 Dec 2025 23:46:05 GMT
STOPSIGNAL SIGINT
# Mon, 29 Dec 2025 23:46:05 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 29 Dec 2025 23:46:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ceb683fde9e2d7e9e13a7e4502185e0a46906394ad8d7afcccfa2683ab399c5`  
		Last Modified: Mon, 29 Dec 2025 23:46:16 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ae7eb44bd96d2ac7e1cddbe12b030859a367e7e624a646e45e633138efb244`  
		Last Modified: Mon, 29 Dec 2025 23:46:36 GMT  
		Size: 6.6 MB (6629586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554f37afff07a56f5045e0f93269cbecb6adcd0a8e891e26843f80269d4f3a39`  
		Last Modified: Mon, 29 Dec 2025 23:46:34 GMT  
		Size: 1.2 MB (1225706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210d2da591453bf590a3611c63962e87e018aa3747ad60a5ca4f55eae51519ab`  
		Last Modified: Mon, 29 Dec 2025 23:46:34 GMT  
		Size: 8.2 MB (8203911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8617f0dc8cbca3563f35af046e8361b92e1bde0be6507868bebab95b7bc4eb`  
		Last Modified: Mon, 29 Dec 2025 23:46:34 GMT  
		Size: 1.3 MB (1308170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd9890d5e7e496095acf50027b5fa74cdc59d9bacc0fd3e66f16c5d106f6335`  
		Last Modified: Mon, 29 Dec 2025 23:46:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822b100ae14db54a0cd59ba6b3cc9e25a05e03a08ee389f8d1231fff394f0928`  
		Last Modified: Mon, 29 Dec 2025 23:46:34 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3967ada693fb5bf7c0cf7a0737beaa36c30a827474542f0977f62cd9af94c97`  
		Last Modified: Mon, 29 Dec 2025 23:46:43 GMT  
		Size: 117.3 MB (117323322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c42e6c9ec151ae7f333eced06e493b21b54a2ba2dab6c6e9caa80924838d033`  
		Last Modified: Mon, 29 Dec 2025 23:46:35 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44563db31a48da44584915f5575e73b953dd7dd52374d5231689f75310e42b8`  
		Last Modified: Mon, 29 Dec 2025 23:46:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab05bc258ab5abcbaa1b33b28ce4e9a71ed8626a0ac45734699c4a367eec39d0`  
		Last Modified: Mon, 29 Dec 2025 23:46:35 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7318af0fa7a2684549fd6f6f63bec059077f8a5b499eb56ee940ad01236ddc`  
		Last Modified: Mon, 29 Dec 2025 23:46:33 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4a3a82ef75c32436ace7b3a9d3a2758873bd8bce163e2a87caa636dd901f96`  
		Last Modified: Mon, 29 Dec 2025 23:46:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:edce6de4a88798f62c4f9fc17bf446d47bf15b6ae874fe7987fbd7a78e2ddb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5661076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffa29bdfe1b5dd9a29f556be63e3e39bc3e61df32b61cf1950a9238a39d9490`

```dockerfile
```

-	Layers:
	-	`sha256:14bcff211ff2bae1af12c8e537c822203c96599bcb016a67770ffdb7c03aebe9`  
		Last Modified: Tue, 30 Dec 2025 03:09:27 GMT  
		Size: 5.6 MB (5607266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a2b4e924233e45e6fd798b20c042777963d1e8e5a9ee733162979a759b9fdda`  
		Last Modified: Tue, 30 Dec 2025 03:09:28 GMT  
		Size: 53.8 KB (53810 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:d50f42b5fba576d267c1bce0bb74f3cf1f84da537f219a4329243711470c265f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169107011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf611b5c4689033ded57c12d425ef96fa644994f0f0b0cdaa0ff0b22eabfcbd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:58:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 09 Dec 2025 01:58:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:58:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 01:58:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 01:59:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 09 Dec 2025 01:59:09 GMT
ENV LANG=en_US.utf8
# Tue, 09 Dec 2025 01:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:59:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 09 Dec 2025 01:59:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 09 Dec 2025 01:59:18 GMT
ENV PG_MAJOR=14
# Tue, 09 Dec 2025 01:59:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 09 Dec 2025 01:59:18 GMT
ENV PG_VERSION=14.20-1.pgdg13+1
# Tue, 09 Dec 2025 02:04:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 02:05:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 02:05:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 02:05:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 09 Dec 2025 02:05:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 09 Dec 2025 02:05:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 09 Dec 2025 02:05:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:05:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 02:05:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 02:05:04 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 02:05:04 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 02:05:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e1e14f4d7b041df9ac5fc8de0576537ea278840427d10e9148c696adb70b27`  
		Last Modified: Tue, 09 Dec 2025 02:01:24 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3745b8a53abf95c5c0de5c32dfcb3b3374ddf07ef91fc46c33e5a7e1f1067d0`  
		Last Modified: Tue, 09 Dec 2025 02:01:24 GMT  
		Size: 7.1 MB (7075970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce494898a07197b6881a493ab77d6aff68197d81a66bc208117b16f056aa1f9`  
		Last Modified: Tue, 09 Dec 2025 02:01:25 GMT  
		Size: 1.2 MB (1214722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1cb5cce5854f2b159fd846f364b0dae1a7331a6356d92a487d5c5a537f77b9`  
		Last Modified: Tue, 09 Dec 2025 02:01:24 GMT  
		Size: 8.2 MB (8203970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c04d390fdc287bfc38e367f6ac75664b0147a2e4bff0ec697269892c4c096b4`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 1.4 MB (1394831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9c5eb03727d2f38c3eb284ce3f107244d3441c38b3c9186ff8d0f4b13e481`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec249543bac7d8464c12595e55a8805f97a5535503ed82d2633b4a943e1b120d`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b0bb2bf0dde0cf8e5f0de5a5b39681b2ef50c1c4c06611f0f01de5a94a1341`  
		Last Modified: Tue, 09 Dec 2025 02:06:16 GMT  
		Size: 117.6 MB (117600263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5255f113870fa8b6e735af277a1579086f958ecec54f93dd6d6c4e94e274bd`  
		Last Modified: Tue, 09 Dec 2025 02:06:02 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5569dbcdc15302952e29002ddfaf5e2c730c3aa9ea39bcca62d717f07bbd8967`  
		Last Modified: Tue, 09 Dec 2025 02:06:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb71c0478c0389e6dcdf4e27c6db332a5fbb4dd5c1c9a0a655f07b971cc57db4`  
		Last Modified: Tue, 09 Dec 2025 02:06:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bfbc1edef1d4f1c64e441b3b44f676d17baa0567bd86f2c0412206462106a6`  
		Last Modified: Tue, 09 Dec 2025 02:06:05 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca68430c9839b3094fc813ea2fafbea17a1216476b9efad8cd7bfa6fe1e6e54`  
		Last Modified: Tue, 09 Dec 2025 02:06:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3b128a7d24bc3b7b478e2e40fe3ae9bf07229dd603dd09138a497c82ce2b89bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5652278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab634e65614587178c5cc6e1a88285cab13a20e63ba08271910d21d2e0b6f9dd`

```dockerfile
```

-	Layers:
	-	`sha256:35568a70a770e6e9c49f377439e528500c766c8a733eebe99bf93097a93e8ad5`  
		Last Modified: Tue, 09 Dec 2025 03:08:36 GMT  
		Size: 5.6 MB (5598348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1e701429a67dcbe2c177a6979ee87ded2cfb53ba3b46ca7025f3fa014c3b29d`  
		Last Modified: Tue, 09 Dec 2025 03:08:37 GMT  
		Size: 53.9 KB (53930 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:0df51d30cfe8a2dc05c58340d322af3cb9aa40a4339c53b95e8b434c6d4f8315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89230129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d39fd732982ba8a9d378e88fe4b75d84fba93ae99226670cbbb776b0281f5d33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 10 Dec 2025 13:55:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 10 Dec 2025 13:56:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Dec 2025 13:56:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 10 Dec 2025 13:56:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 10 Dec 2025 13:57:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 10 Dec 2025 13:57:58 GMT
ENV LANG=en_US.utf8
# Wed, 10 Dec 2025 13:58:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Dec 2025 13:58:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 10 Dec 2025 13:58:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 10 Dec 2025 13:58:38 GMT
ENV PG_MAJOR=14
# Wed, 10 Dec 2025 13:58:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 10 Dec 2025 13:58:38 GMT
ENV PG_VERSION=14.20-1.pgdg13+1
# Thu, 11 Dec 2025 04:04:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Dec 2025 04:04:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Dec 2025 04:04:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Dec 2025 04:04:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Dec 2025 04:04:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Dec 2025 04:04:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Dec 2025 04:05:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 04:05:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Dec 2025 04:05:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Dec 2025 04:05:00 GMT
STOPSIGNAL SIGINT
# Thu, 11 Dec 2025 04:05:00 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Dec 2025 04:05:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7509a6e61e937d2861e580aee3645ccc284662e5ff785c3a9eb5fea93cf517b`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd637312070c560044a9b139cf8983fb8e39b5f60b3c51a2c557980815f7101`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 6.3 MB (6291355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7b1b0d8d9bb5d10b5a2d66ecee216d2f1cae8a593baa99e14a05f9eed3afbb`  
		Last Modified: Wed, 10 Dec 2025 16:03:48 GMT  
		Size: 1.2 MB (1201916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cfccc2a828efdeee76cdfc0241a7a2253c5d5e7ec9c2770454a9f217a9c55a`  
		Last Modified: Wed, 10 Dec 2025 16:03:48 GMT  
		Size: 8.2 MB (8203580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87922f2a83f8c445248a001ee77716a207d176d413c183b77f66b22eb3c3aae`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 1.4 MB (1402222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f877525412689d6256ebb5cd6dd6649d1f971ed1a240aa789cd7554715346e`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4086fc5e0163b1fdce9acbb9093daa90b18ab170c9c52c4e31bea0af44599c`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cf0e75afdb53445b4eeff74f3fa59cf6b6b9a94809b7b2127d09e2f1a7b53c`  
		Last Modified: Thu, 11 Dec 2025 04:07:46 GMT  
		Size: 43.8 MB (43837524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf33eac311a2d227f8fec23562d3ff9079fbb3400019ba3610c8fa51c6e6ffb`  
		Last Modified: Thu, 11 Dec 2025 04:07:41 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04624a3f07e4ef305b79bd9ff4a2d76f9bbd17296fd2bfe83b949fed1a56680`  
		Last Modified: Thu, 11 Dec 2025 04:07:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9152c212d5bcb5fcc34b33559f5db175d49f6627e8d039247bb29f13990b917`  
		Last Modified: Thu, 11 Dec 2025 04:07:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622421d0a997b2ee61e939a55cd197209339c946d675f1b6de1cf4ba163eb008`  
		Last Modified: Thu, 11 Dec 2025 04:07:41 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60021489893ba78009a1c02659da2754c33af8e68921f2946634dc64bba38be`  
		Last Modified: Thu, 11 Dec 2025 04:07:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:4606299c510bd85e69930ce6a609ad8c4f0db831d34ae6c77f7f4e7d34f14cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5051862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb982826e4f4ab251d4593e901fff4c2b7d5ecfc36657a2714bf0e04edae2b62`

```dockerfile
```

-	Layers:
	-	`sha256:94784950184169f8454b3bfec40dd5ca7e4514ecd6414b70cbddb92080bcf914`  
		Last Modified: Thu, 11 Dec 2025 06:07:51 GMT  
		Size: 5.0 MB (4997940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854519211fc75bd62e6c88fe1acb9c5cc6a77e0520e26118afb575209a37ccae`  
		Last Modified: Thu, 11 Dec 2025 06:07:52 GMT  
		Size: 53.9 KB (53922 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:23ea8c6bfb2378ae2acbd6c2d7921a84636a78767ee73f7ab8d8a5964071dbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.4 MB (171423152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5133e86b043656e78d9ed4bb7215b803172dbe0f1652422df9b2a00618f1a5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:04:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 30 Dec 2025 00:04:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 30 Dec 2025 00:04:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Dec 2025 00:04:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 30 Dec 2025 00:04:24 GMT
ENV LANG=en_US.utf8
# Tue, 30 Dec 2025 00:04:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Dec 2025 00:04:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:29 GMT
ENV PG_MAJOR=14
# Tue, 30 Dec 2025 00:04:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 30 Dec 2025 00:04:29 GMT
ENV PG_VERSION=14.20-1.pgdg13+1
# Tue, 30 Dec 2025 00:41:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 30 Dec 2025 00:41:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 30 Dec 2025 00:41:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 30 Dec 2025 00:41:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 30 Dec 2025 00:41:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 30 Dec 2025 00:41:54 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 30 Dec 2025 00:41:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 00:41:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 30 Dec 2025 00:41:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Dec 2025 00:41:54 GMT
STOPSIGNAL SIGINT
# Tue, 30 Dec 2025 00:41:54 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 30 Dec 2025 00:41:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03bd633819322cb11cc9513c226982c942eac3e48bfea2d0beb19c3ebd3e150`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015fcb425b0e0871d518edcad4b32033422d0610ee48d41f3288482f4fec20f5`  
		Last Modified: Tue, 30 Dec 2025 00:17:23 GMT  
		Size: 6.4 MB (6408815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92c8bb518bee6ea32d2d42baa957da796efc96dc7ced791f56e79c49a0295c5`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 1.2 MB (1230094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8535702b3710c6fcd3201da506474e2b1283cf1944f25e878d3fd583f7677efd`  
		Last Modified: Tue, 30 Dec 2025 00:17:23 GMT  
		Size: 8.3 MB (8258860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d63ed103a386eaf5a068332156cd65d9319160774cf86554445beccd47ee9ad`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 1.4 MB (1398084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2dd9df4f9a1797f74af4c2cdd546b3644f6a67e7f305b3faa9f6dfbff69a69`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f900bfe654117b3bae9e4f7f94414bf575d933fd78fd8dc60edada8ee0c14818`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a13efb5bbe34aa6909d006fbbd26eedceac63aae44576419322aa946e84e61`  
		Last Modified: Tue, 30 Dec 2025 00:42:42 GMT  
		Size: 124.3 MB (124272515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb372e69895e24b180518a27126c39b2097e10b30df0da3a90855ee43287116`  
		Last Modified: Tue, 30 Dec 2025 00:42:31 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf1e6ec3e1c6a780900ce24252b6e699358ea8c60faf20c0ac86f936fea333a`  
		Last Modified: Tue, 30 Dec 2025 00:42:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc79abab9706a8ac70fea4b5659ab67aa349af129c07e6a32c2c87d071dd19`  
		Last Modified: Tue, 30 Dec 2025 00:42:31 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69d72c9771ace1cdb0c9b8fc4b2657984d4b59fc753012e4dcd67407369b385`  
		Last Modified: Tue, 30 Dec 2025 00:42:31 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0d901678a33e79409ce50b5aa3de10a892eeb2e10afe63f3fb1240865db103`  
		Last Modified: Tue, 30 Dec 2025 00:42:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:bffde720aba4a35fe9cac0608ac266ef8cd728ac5f5fb311ea0cd61e6c66f478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5662268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16206a7702447defbfae33568becb9271fefda7a0bc471804e8fc6de08e9af8d`

```dockerfile
```

-	Layers:
	-	`sha256:dce919e465e4c76e370ea90085dda6151462e9b682ef802005fdd5a4975b2a79`  
		Last Modified: Tue, 30 Dec 2025 03:09:40 GMT  
		Size: 5.6 MB (5608404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efc2d7f6b5bbdb70730ac959ff14694c73a4ab6b2cdc748279a3900e31da8f3`  
		Last Modified: Tue, 30 Dec 2025 03:09:41 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json
