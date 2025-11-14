## `postgres:latest`

```console
$ docker pull postgres@sha256:435fe973d0516bf24165976346eced9c841a890b1a2092cb68c45a93679b1b19
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

### `postgres:latest` - linux; amd64

```console
$ docker pull postgres@sha256:4e72fca616daacad29e7a8d67cea260b7ef1a8ad9e34d79093362bdf9c6da5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162206855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0fdf1c3462a9cc7069a3b040f96eab644a288a485bdc297356e6f569092acd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 19:16:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:16:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:17:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:17:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:17:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:17:09 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:17:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:17:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:17:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:17:20 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:17:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 19:17:20 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Fri, 14 Nov 2025 19:17:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:17:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:17:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:17:39 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:17:39 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:17:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:17:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:17:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:17:39 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:17:39 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:17:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b93c522e67c09ad1ebded7c35ca62608f3cef2f9bd366af06f52423a8ced24`  
		Last Modified: Fri, 14 Nov 2025 19:18:36 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075181f579f6a66cf0198834632f645fe3ef92e1ffa1c5b5a5116e3e84a20c68`  
		Last Modified: Fri, 14 Nov 2025 19:18:37 GMT  
		Size: 6.4 MB (6436662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f091493f402b84cab89d53e7d78bd24ce8525949f00299b051997f9c1d75419`  
		Last Modified: Fri, 14 Nov 2025 19:18:36 GMT  
		Size: 1.3 MB (1256653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8445ce783dbee3c21588e609be96a978581e1b68bb9b86a8a2fa6483fcc7b5ac`  
		Last Modified: Fri, 14 Nov 2025 19:18:37 GMT  
		Size: 8.2 MB (8203727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acd3509f73dfc1bd6ce584363347bc1b8f266f35ee8aa699a370e03ace85415`  
		Last Modified: Fri, 14 Nov 2025 19:18:36 GMT  
		Size: 1.3 MB (1311461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6aafe60359bee8adbbcb26850e817d42b2790e6b0732e60debc6a7bfa4ee28`  
		Last Modified: Fri, 14 Nov 2025 19:18:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50db0aeeb20502752467d5602f8879371160b9771f0f0d8dc0637d60359f32f`  
		Last Modified: Fri, 14 Nov 2025 19:18:36 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b920a99824d4b4286aede7c38c80a50118c0f3a6c6825ec793c8a86a8d7d97f`  
		Last Modified: Fri, 14 Nov 2025 19:18:45 GMT  
		Size: 115.2 MB (115190480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc9fcc38e2a20235de8db6261f767638c30327b53fd99dc82d78d74a8108944`  
		Last Modified: Fri, 14 Nov 2025 19:18:37 GMT  
		Size: 19.2 KB (19191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7310e2ca4c8964d6e60993aa76813d3f6a00414930a32da1e831e45740db0e82`  
		Last Modified: Fri, 14 Nov 2025 20:18:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e1ecf083089a8e3e81e29efd5587dfd8c779ce2322c3e09f19d24a87bf7de7`  
		Last Modified: Fri, 14 Nov 2025 19:18:36 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2511b29bbd17d1c5fc5f280e379772c9cd9c09a705354ef1181b9a7127884d6f`  
		Last Modified: Fri, 14 Nov 2025 19:18:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:719ceacf688c954c81283d50ee6cfe2868aedc48169f118b40d365169795f9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6008936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a1071371144fd4b6be460f160767cf3cb2b599968326010c63df47125c42a0`

```dockerfile
```

-	Layers:
	-	`sha256:9c9de6c200eb2b21e37bad95973b5b965e8ed736e7ad19f970e2e2cb1ff89a48`  
		Last Modified: Fri, 14 Nov 2025 21:17:25 GMT  
		Size: 6.0 MB (5956479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:592ed36e881f02322942665f7f22b70bfc1493901cdf7dc6fffa69af8245f6b4`  
		Last Modified: Fri, 14 Nov 2025 21:17:26 GMT  
		Size: 52.5 KB (52457 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v5

```console
$ docker pull postgres@sha256:82449cc60ab10b05fbbccd08be74dde86e5de935d1a6d818ecbcad6a82b2e974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91398762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaf2df95628424f309c8cfc5ae56a73e7c32f16550f565046b4bf757a8e2c6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 19:20:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:20:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:20:38 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:20:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:20:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:20:46 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:20:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:20:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:20:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:20:54 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:20:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 19:20:54 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Fri, 14 Nov 2025 19:34:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:34:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:34:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:34:02 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:34:02 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:34:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:34:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:34:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:34:02 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:34:02 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:34:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f54e77e4091ea63679d8886ddfcc17bec9973dfa25e472bce10aafc25c34fd`  
		Last Modified: Fri, 14 Nov 2025 19:34:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cbb756a24873a58db5d07e08bf3706620f42d3bbfce9b5eb2b639b2c806142`  
		Last Modified: Fri, 14 Nov 2025 19:34:25 GMT  
		Size: 5.9 MB (5928948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d9daa31b7d8bcafc5a6a99ff0ec4dd97c5912bed3b44c6c43b87cca0bf274a`  
		Last Modified: Fri, 14 Nov 2025 19:34:25 GMT  
		Size: 1.2 MB (1227366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9d221d750b8e2244b12940045c4d25acc4a77baedd407c4b227e324a008182`  
		Last Modified: Fri, 14 Nov 2025 19:34:25 GMT  
		Size: 8.2 MB (8204127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ce5a540dd746600e5c7dc42e393f74620234388d1443db72362c54c0577b9`  
		Last Modified: Fri, 14 Nov 2025 19:34:24 GMT  
		Size: 1.3 MB (1317147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a04ea72072c65885ef9c3ccc83951c24e901ae43a08f17bb69449d6954e2ef`  
		Last Modified: Fri, 14 Nov 2025 19:34:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4261da3794af10d2dc8b3e1ee8fa1065a2b166ff3117fe6e87524e0d55cbb41e`  
		Last Modified: Fri, 14 Nov 2025 19:34:24 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e224d80e71aafe7c79cc936287f0204b230d292a7e05da7b65c40d920d161ab`  
		Last Modified: Fri, 14 Nov 2025 19:34:30 GMT  
		Size: 46.7 MB (46744973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cfa6d715e44fbe07983a429d4cc6fd961e08603d97b3eff99add07858580ff`  
		Last Modified: Fri, 14 Nov 2025 19:34:24 GMT  
		Size: 19.2 KB (19181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c1cafc1b5be2381cb43cfadee8418267c1908c7af477563fda5346278b2f1a`  
		Last Modified: Fri, 14 Nov 2025 19:34:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e154c73e3e4c3395be60b491241af13269d61a5f16721c36ac8c670c755ffc5`  
		Last Modified: Fri, 14 Nov 2025 19:34:25 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ef4406fee59bfcd63890fcb41a09cedc6e83ce1eb31670b4bc322be13161b7`  
		Last Modified: Fri, 14 Nov 2025 19:34:25 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:6c3d1033be66d149d1cb85610c8fd6a747ec491ba5602d7cfec58572b37c81d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84097373167169cd00a22527a2caccbd409c6de1833ea99c138b82b3a0e47cf`

```dockerfile
```

-	Layers:
	-	`sha256:cd10350f2f92b149b79564da272911312ebdff3f817e6c28ed47872fc9d1ddfc`  
		Last Modified: Fri, 14 Nov 2025 21:17:31 GMT  
		Size: 5.1 MB (5119622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fae906de659ba1f9ee2046a15894071b58f7405ca91dd79f34b83625124592a`  
		Last Modified: Fri, 14 Nov 2025 21:17:32 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1d693bc2fcf8753ace6e6419a4ae13079caf769cf5d174f495232bc9a636b28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87720908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4f7ba7ef22aa8b44b49ce8ab00b0baf74f0de7f3682b13f80fd33af4cbaab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 19:19:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:41 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:19:48 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:19:53 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:19:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 19:19:53 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Fri, 14 Nov 2025 19:31:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:31:34 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:31:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:31:34 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:31:34 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:31:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:31:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:31:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:31:34 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:31:34 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:31:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b08bd2af23fa4108a79680ead8f75bb6cf51fadc3c913ff0d88676405e27ed`  
		Last Modified: Fri, 14 Nov 2025 19:32:03 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6366e90ab14cc87549916b0ceb31b37521e48a73b0bccf8c64bc9f58d1b098`  
		Last Modified: Fri, 14 Nov 2025 19:32:04 GMT  
		Size: 5.5 MB (5496778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad323cfd08f969d1ce181898bf3fea74960ae2c6d2f6ccf701d382047c40d12`  
		Last Modified: Fri, 14 Nov 2025 19:32:03 GMT  
		Size: 1.2 MB (1222227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d455e8e8923d8836fbe149c7dc14f1776fba2dcc6bf8a75be5d3b4c7c54e8714`  
		Last Modified: Fri, 14 Nov 2025 19:32:04 GMT  
		Size: 8.2 MB (8203912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff31d338a54b74b848cd90d0ca5923b645326611f0f93aa99ae857a22b37b4e`  
		Last Modified: Fri, 14 Nov 2025 19:32:03 GMT  
		Size: 1.2 MB (1172456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ceacf50c771d87b9c02f820ea264bc6b167d926f02b43b21c9f20428eed133`  
		Last Modified: Fri, 14 Nov 2025 19:32:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53cf77ba3688161fd561e3001910a822a2d3fcff8ccdfb0fe930880322f7f2b`  
		Last Modified: Fri, 14 Nov 2025 19:32:03 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ec1a7c99b328134e9b77b549cd99cbdfa877a0d1728908ed5f46064fde4484`  
		Last Modified: Fri, 14 Nov 2025 19:32:10 GMT  
		Size: 45.4 MB (45382713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5830df1543020f4fcc7030eedc30051a5dabda1d21b7aed0dbb8bc4ab08d3bb6`  
		Last Modified: Fri, 14 Nov 2025 19:32:03 GMT  
		Size: 19.2 KB (19202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b531e051ed1270f4d2ea10f2be5a2911858ff5ec96a8db8a10826d1a77edd5b1`  
		Last Modified: Fri, 14 Nov 2025 19:32:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb82c6446b7bae890313800c8b1d57eab5cd3ffb55c1833ea4d0ad4b1f745839`  
		Last Modified: Fri, 14 Nov 2025 19:32:04 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a29435802781cba5a263f896f3eedef3b01b0f5fd5abc364e642948178997d`  
		Last Modified: Fri, 14 Nov 2025 19:32:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:7e8110c8608f4f74ad2997a25a12a47a089154757e442875286410e3ed743efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5684795526764b2f07f01b4a0c8671e1f84395d261d101dfff809c1b372b15e5`

```dockerfile
```

-	Layers:
	-	`sha256:7458227a7dba888b7c51e9b88253d4abd39977c975c23fa3b496e84955ee9197`  
		Last Modified: Fri, 14 Nov 2025 21:17:37 GMT  
		Size: 5.1 MB (5118927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:753debbd073f9f27924e555743b45049d4f6998e74cf0686965b9f3e1e3015b9`  
		Last Modified: Fri, 14 Nov 2025 21:17:38 GMT  
		Size: 52.7 KB (52678 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c2d27cc675b30a6a2fbad69a224c2499e9e1c9be5bdde6abb243d61cb0d34c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160816862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90e9c757ca144b3138b0127bde2aa2ecaca0e5aa2156f43f1b2c93eb171f5a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 19:16:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:16:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:16:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:16:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:16:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:16:32 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:16:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:16:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:16:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:16:37 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:16:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 19:16:37 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Fri, 14 Nov 2025 19:16:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:16:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:16:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:16:57 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:16:57 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:16:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:16:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:16:57 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:16:57 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:16:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d212b92109e32c380d2522cda7a6fcee6b81f958b918ea55b1a7548e638626`  
		Last Modified: Fri, 14 Nov 2025 19:17:50 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e91eecc064d1f744554e6df3b0efc12582fb81fd3650900256ac1a251456c0`  
		Last Modified: Fri, 14 Nov 2025 19:17:51 GMT  
		Size: 6.2 MB (6231976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc66cab963daea7ba314b8cdfa2c5056fd715e2bd1bcd1a64169829ead26c74`  
		Last Modified: Fri, 14 Nov 2025 19:17:50 GMT  
		Size: 1.2 MB (1209392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efce4fb8eb33a0b042e9a03ae7a790ebc9f9c384c05292d8cb82ef491aa9523`  
		Last Modified: Fri, 14 Nov 2025 19:17:51 GMT  
		Size: 8.2 MB (8203880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fa5a56604f533ae74e42ef848fab9c56f6881a61b92765904c7537bf84ee59`  
		Last Modified: Fri, 14 Nov 2025 19:17:50 GMT  
		Size: 1.2 MB (1220447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523dfda92f69f86783d6d43107b26c8390f4a46ee051ed4ac2da3bc0348e75e`  
		Last Modified: Fri, 14 Nov 2025 19:17:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477e84c75a3a16cf6c6a40bcb286315be344ef617c44c957fc7303a508feb1dd`  
		Last Modified: Fri, 14 Nov 2025 19:17:50 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f803be1ce76bbcae41e8c982df418226ee5753eaeacd9f3ece58e701204c63`  
		Last Modified: Fri, 14 Nov 2025 19:17:56 GMT  
		Size: 113.8 MB (113779093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff763312b1ba307acbdf4057d1fc5231856d90f9e9690ae4993d046bdb0de404`  
		Last Modified: Fri, 14 Nov 2025 19:17:50 GMT  
		Size: 19.2 KB (19186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db13adcc20f3ce05d1fc5f47f72463c4626d64e07d41dfcf05b30d85e9cb9de6`  
		Last Modified: Fri, 14 Nov 2025 19:17:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb83b9a026d928e67c3cb2143ded7ed40b3d002a5cb100d1f187c6799246eb`  
		Last Modified: Fri, 14 Nov 2025 19:17:50 GMT  
		Size: 5.8 KB (5844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f971916e604dab61091205b016f53b952aec70ddd40e05490ead2803b95c8c91`  
		Last Modified: Fri, 14 Nov 2025 19:17:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:c9c595aec6cf9de59186e1442afb79fffbf14df45c38df888edb1488a58484be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fde23ab6ae0ca34346cd3b14734ec1a0c5bfd3e1cf3409e187aa9c9d1abf69`

```dockerfile
```

-	Layers:
	-	`sha256:63569cc76523ecc866f6c63e230316cb7105f2010e60946c9f22e4042cc56a85`  
		Last Modified: Fri, 14 Nov 2025 21:17:43 GMT  
		Size: 6.0 MB (5962852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8dbf5e504182c06e26504328f22d9d36b5ddf7e112739b5d8a236546cd51d07`  
		Last Modified: Fri, 14 Nov 2025 21:17:44 GMT  
		Size: 52.7 KB (52736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; 386

```console
$ docker pull postgres@sha256:b13e60a97e0c8d918e8c4d9a68dc356b13f53b3a2655a46a15af67f7b097dd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97512055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02382d452630487b33c378119f8b760dfb1b45c8142ff33c5168251a2da68f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 19:18:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:09 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:19:14 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:19:18 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:19:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 19:19:18 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Fri, 14 Nov 2025 19:27:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:27:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:27:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:27:18 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:27:18 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:27:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:27:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:27:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:27:18 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:27:18 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:27:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c1a8a453f9fe7573d3e5c87ae5fa04a3a8d7304b63843a46c29f5dff7feea`  
		Last Modified: Fri, 14 Nov 2025 19:27:39 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bcae022ca0c974f81992672e41816194a29e3ab9a91d911dcc9adf69e84f52`  
		Last Modified: Fri, 14 Nov 2025 19:27:39 GMT  
		Size: 6.6 MB (6629494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada63d3c79ccb26f2e07846731ae7700f55f7417584cb92ed25f3916ab8a5430`  
		Last Modified: Fri, 14 Nov 2025 19:27:39 GMT  
		Size: 1.2 MB (1225654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8b429f18961ac1ac2cc418e5857fc2e2cc0fa3e54e94e0014e406e3b84b0b6`  
		Last Modified: Fri, 14 Nov 2025 19:27:39 GMT  
		Size: 8.2 MB (8203925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6af1864be4cd7f5226621849b4afbc12a9797be0a16dd7e7b2b2444c6e6d`  
		Last Modified: Fri, 14 Nov 2025 19:27:39 GMT  
		Size: 1.3 MB (1308114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfbb50f09365ba651fc1d2d488343c29c4b1a7aa8792fe84821912a9614391e`  
		Last Modified: Fri, 14 Nov 2025 19:27:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7725908ac71dc96c9f97b16b412067af8449e19a4a93ed416139e57752ecb97d`  
		Last Modified: Fri, 14 Nov 2025 19:27:38 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d52971393359c5ee5764f8b898cb9f54b8ddd59d93d2c743b98391515b8ccf`  
		Last Modified: Fri, 14 Nov 2025 19:27:43 GMT  
		Size: 48.8 MB (48820314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1c546756479662c3acd8b4c88eba7ab581b2971a661ae4d60e59b31057c4bf`  
		Last Modified: Fri, 14 Nov 2025 19:27:39 GMT  
		Size: 19.2 KB (19186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb52e7d09e68523b6d2c5afd5e815907ab2b8ac0fd56adfd49e3eb2e8701bc61`  
		Last Modified: Fri, 14 Nov 2025 19:27:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57251432bcc547b63a1678210264e74172290c720ba61c9639af5d77b7f58fe6`  
		Last Modified: Fri, 14 Nov 2025 19:27:39 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693fc79ee8d3d851edd218fdc2f98b1d1b45d9aa81b4dd5bd42646b9f2fc7f8b`  
		Last Modified: Fri, 14 Nov 2025 19:27:39 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:c4ac676bbb1cb77f22006aad4da347b0ba99b38f16c108071ec2a58cfc1cf683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637a5ddb7a290b6b05ef2e4e6fce60f1611c966c1a49870e99aa6772c287c53e`

```dockerfile
```

-	Layers:
	-	`sha256:2ffe394afc5b8795ba13047462037072348e92c68661761e546ac28cf5e5f9e2`  
		Last Modified: Fri, 14 Nov 2025 21:17:49 GMT  
		Size: 5.1 MB (5114955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71f1a808db7cf08b140d6c29d691e9a218c10c0c5ec17fcb9ab637ff0bf78b8`  
		Last Modified: Fri, 14 Nov 2025 21:17:50 GMT  
		Size: 52.4 KB (52391 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; ppc64le

```console
$ docker pull postgres@sha256:1c357d1907a66ab3aa5de77e1c557c10c6c6468b86594b355b5d6d4fdb06aed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174629656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc19874ec1065a6cb25d107b1e5963410abdeb3313be99c8f72ee2ee3a95c90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Thu, 13 Nov 2025 21:03:42 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:03:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:04:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:04:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:04:18 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:04:18 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:04:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:04:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:04:27 GMT
ENV PG_MAJOR=18
# Thu, 13 Nov 2025 21:04:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 13 Nov 2025 21:04:27 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Thu, 13 Nov 2025 21:05:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:05:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:05:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:05:08 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 13 Nov 2025 21:05:08 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:30:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:30:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:30:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:30:23 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:30:23 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:30:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fc0061372adf3d63a13d2ca7ad0f3e93c559c4946c804f4b6cd8188fe82e18`  
		Last Modified: Thu, 13 Nov 2025 21:06:27 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ea4eea6db9d73280f2865808f223f2945540e75194b34d58d0d2cd5fdd4dc5`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 7.1 MB (7075854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0055703ee1b9b5dd2d9c1885a2faa38d17a66494ad29256b526f245153a6fc3b`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 1.2 MB (1214665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1fc3e056b0187b8b00b4418da5ff6a096b7b79d7699c38c5d901b98afd435`  
		Last Modified: Thu, 13 Nov 2025 21:06:29 GMT  
		Size: 8.2 MB (8203908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa191b7869bd1800b18f744f13025fd248b9169d56129121df2164e220d7fcdc`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 1.4 MB (1394701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cfd16d3ad528deda1ab9495135db3760b28e8ae530af5fee50698783255c7f`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c324574916baf5af487c21d6adcf241528368e98ec6817195d55bf1c67434b6`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57cd25fc2802cdb6dd760966ca1984b1ef8898495072127b861441e8d583577`  
		Last Modified: Thu, 13 Nov 2025 21:06:38 GMT  
		Size: 123.1 MB (123112104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a987dadb7b62c5b7e304cf83d0402028254e79d00cfb9cc20c5cf85a0c145b`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 19.2 KB (19195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907cdde459aadbc3deb003cca90cc577746fdac7ad9cb8102fc93531fcd67f69`  
		Last Modified: Thu, 13 Nov 2025 21:06:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a34e40586d06608bb05bf210a6b9d6c58ffb530319b0d012204bf7a73d80d70`  
		Last Modified: Fri, 14 Nov 2025 19:31:07 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5783e82494db710b876118734705cb0cfc374e24ba03d5f44beef058f34e618b`  
		Last Modified: Fri, 14 Nov 2025 19:31:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:60f63b8994c124ce71843c36049ed3912a3fd366085d7983ad06974ee97b6a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d941d586c2aabf3c7c8c134b33bce574ab48c17033a148d5a6c0686c4fb5d91`

```dockerfile
```

-	Layers:
	-	`sha256:d7dc0ff926d3283e58692e92cd854f93f31ec50a200f2e79975ab46e52417726`  
		Last Modified: Fri, 14 Nov 2025 21:17:55 GMT  
		Size: 6.0 MB (5963127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc05eef4d84ea875af9d1420db375cfe0e292f1213cfe5535c605769f936ead`  
		Last Modified: Fri, 14 Nov 2025 21:17:56 GMT  
		Size: 52.5 KB (52534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; riscv64

```console
$ docker pull postgres@sha256:d6655954160f44593f31934e63724c5e5072f084555868b25bdf3f524a20ec20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92798076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f44182345138a7be0e47cfd884a149c6f65afc6c9ef18b4369b095130ac51bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 23:37:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 23:38:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:39:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 23:39:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 23:40:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 23:40:04 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 23:40:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 22:03:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 22:03:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 22:03:34 GMT
ENV PG_MAJOR=18
# Thu, 13 Nov 2025 22:03:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 13 Nov 2025 22:03:34 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Fri, 14 Nov 2025 00:06:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 00:06:41 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 00:06:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 00:06:42 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 00:06:42 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 00:06:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 00:06:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 00:06:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:06:42 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 00:06:42 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 00:06:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc37d55c3011ce48efe8b5340c1d17952a31a7ccbd33740e03b4beb1fa13cd08`  
		Last Modified: Wed, 05 Nov 2025 01:45:45 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b15d328aac9b8cd6aaa0b70eb3464d2f18f8e019f9685fd9492eaacda84c3`  
		Last Modified: Wed, 05 Nov 2025 01:45:48 GMT  
		Size: 6.3 MB (6291276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a53caf52e6aba7e4dff6229654beb9afe47145c315e2b283651efb87c5512ec`  
		Last Modified: Wed, 05 Nov 2025 01:45:45 GMT  
		Size: 1.2 MB (1201883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6648770da4d060ceb20dec8e78d9224a4129eadabec3ee7fc56d287c66d5a1b`  
		Last Modified: Wed, 05 Nov 2025 01:45:46 GMT  
		Size: 8.2 MB (8203570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b7028147a73306c16d8351b86fe10a30cc70681d2316fc2d0c3d694664899d`  
		Last Modified: Wed, 05 Nov 2025 01:45:45 GMT  
		Size: 1.4 MB (1402208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67a541f6f6331fbd6d7ea6d3e646d86231d815486c4b8a6c9afaec8bba773c5`  
		Last Modified: Fri, 14 Nov 2025 00:09:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782d3cf5a012c39ef2f2953f74e44665be00398054f1c73231da9064031cc216`  
		Last Modified: Fri, 14 Nov 2025 00:09:37 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e237f51f5dc0bc03dcf64480cf4f736817d957bb97bd0fdb43f8f1d669717086`  
		Last Modified: Fri, 14 Nov 2025 00:09:41 GMT  
		Size: 47.4 MB (47393339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0691ae43af1d98ac82cfb8dc17a321bc689a7578ec060c5565b83559328e39db`  
		Last Modified: Fri, 14 Nov 2025 00:09:37 GMT  
		Size: 19.2 KB (19194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60e69360d85b83354071136e498c7999885c012779d3e150fd3ffab51985a2`  
		Last Modified: Fri, 14 Nov 2025 00:09:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6464a31abcf289952026ab97107ee931cff88cf9e8cbe9c6308dd5115e1cb8`  
		Last Modified: Fri, 14 Nov 2025 00:09:38 GMT  
		Size: 6.1 KB (6082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c527935a068e9fe3d70720a0d633742cc8d155fecac7f5ea56614d48ae3253`  
		Last Modified: Fri, 14 Nov 2025 00:09:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:10b0814f850c490cbcbdb594c86d0d46656276c7d4c456efdff5fff39186b2cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5162422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b7e91b906de5cf1bc8340db42ed2a0575afe9c3bd2c791203754c95c17365f`

```dockerfile
```

-	Layers:
	-	`sha256:9daeddf2043ccaf15e08a294cfe785d6722bf16355adf62a56eef77a8d06c47a`  
		Last Modified: Fri, 14 Nov 2025 00:21:59 GMT  
		Size: 5.1 MB (5109895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135e60df4868d5cfdc6fda00a3a2617c219483a6a5868015e4528c7d5ac1a12c`  
		Last Modified: Fri, 14 Nov 2025 00:22:05 GMT  
		Size: 52.5 KB (52527 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:latest` - linux; s390x

```console
$ docker pull postgres@sha256:a20fa56b7a3e407cebcc1abd5d7fbf5eb258732ca6b78326ea2554937d785d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176853162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9359588bd1b02a7700f9fe5edaff481f46d8d37608202e521dc5321dcb1232c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:10:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:10:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:10:37 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:10:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:10:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 01:10:42 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 01:10:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:10:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:10:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 01:10:46 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 01:10:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 01:10:46 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Fri, 14 Nov 2025 19:29:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:29:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:29:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:29:39 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:29:39 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:29:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:29:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:29:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:29:39 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:29:39 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:29:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5399cecd953e5785d53fd728e61555d1401c24c0d4dacf00f764fa2a1c7ba8`  
		Last Modified: Fri, 14 Nov 2025 01:23:35 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214675e5dffdf46f157bebccf8f515d78b66e3594fe657abfe4e7c5e4a7a38e0`  
		Last Modified: Fri, 14 Nov 2025 01:23:35 GMT  
		Size: 6.4 MB (6408712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d20e73580992aa553706ac149a95945a73f85646a7effc93b94d84b6e9c448`  
		Last Modified: Fri, 14 Nov 2025 01:23:35 GMT  
		Size: 1.2 MB (1230017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95605b90b4f9d4a2084144af7b66349e2c44c34ade300a0cc374c28ace3cfda`  
		Last Modified: Fri, 14 Nov 2025 01:23:35 GMT  
		Size: 8.3 MB (8258768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c3317a3f16a221b53433cbff1652a6e38221aa6a222bbcdaebedd3ee5c4aa4`  
		Last Modified: Fri, 14 Nov 2025 01:23:35 GMT  
		Size: 1.4 MB (1398029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e184b7f9f143f2cf4457cf7bc47232defe0edae2d2f44bea7b65c7bd6398eb31`  
		Last Modified: Fri, 14 Nov 2025 01:23:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7256c340ccdb241ac3c9311e1d70ced985861cb70a0072c6009297165546cd`  
		Last Modified: Fri, 14 Nov 2025 01:23:35 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6662e180b49fcc17c2e41425fb9c4807cb6a9aa654dfaebcb5fdc0dfd78ee68f`  
		Last Modified: Fri, 14 Nov 2025 21:26:15 GMT  
		Size: 129.7 MB (129690475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a56a1dca5e46d6c21af55a2d9ee57751c9b5ecced71a23d3bd45103beb4fbae`  
		Last Modified: Fri, 14 Nov 2025 19:30:23 GMT  
		Size: 19.2 KB (19189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88652b037f9c2012f68fbc9f9fa423c6276cc6f0d35734f366980264205d4dc2`  
		Last Modified: Fri, 14 Nov 2025 19:30:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eba1a2c0c94f1a7a6df2909a85a1e5d335a8675984486f84f2172f7e69df061`  
		Last Modified: Fri, 14 Nov 2025 19:30:23 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82e59a19b9530178b0ce37f54fa04d958305cf0c72fa82f5544b486a17d8d65`  
		Last Modified: Fri, 14 Nov 2025 19:30:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:latest` - unknown; unknown

```console
$ docker pull postgres@sha256:9d0ca8e93df0f512ebbc0daebab3813fb6c6cdfd0c97f9d7262f0847c0ee27e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629fa778083cdf2c2f888e08814779354fff89ad193771afcb9817f7d60904b5`

```dockerfile
```

-	Layers:
	-	`sha256:514bde88d6d4b5d5c040ec7a839e13320390f124704c42c3261efa30693ad751`  
		Last Modified: Fri, 14 Nov 2025 21:18:06 GMT  
		Size: 6.0 MB (5973149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6495938b5e06ca6ba8a1d7829bc9cc182693a20115eed32be92178d449cf8c00`  
		Last Modified: Fri, 14 Nov 2025 21:18:07 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json
