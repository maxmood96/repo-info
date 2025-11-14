## `postgres:16-trixie`

```console
$ docker pull postgres@sha256:10c797ca5b577b78368fae4660499cbd8305216fc71272036a415fe6dc89918f
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

### `postgres:16-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:5f23cf4be980211393a229d0134e2f4cb38b7bf9f8e2a4aa12aa9e07b4f562bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160093994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231d210b81d69455daee62f5f327b44538b093176bfcfbff7788cd7dd451b9ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Thu, 13 Nov 2025 21:05:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:06:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:06:06 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:06:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:06:10 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:06:10 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:06:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:06:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:06:14 GMT
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 21:06:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 13 Nov 2025 21:06:14 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Thu, 13 Nov 2025 21:06:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:06:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:06:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:06:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:06:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:06:27 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:06:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:06:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:06:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:06:27 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:06:27 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:06:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2f76c3e01af58e38e1bc7e3d28505d9f5382f2a4c8718230df4057b8b32067`  
		Last Modified: Thu, 13 Nov 2025 21:06:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66a13a7f21792ecfec27de41a18247f178d2527058fd01b4257c6e01498ddd4`  
		Last Modified: Thu, 13 Nov 2025 21:06:56 GMT  
		Size: 6.4 MB (6436597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf58b1cfdd91d65491e6a46e07e9977581fb726dfc2349b7fef1318820406bb`  
		Last Modified: Thu, 13 Nov 2025 21:06:55 GMT  
		Size: 1.3 MB (1256633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f915d575b2171d60faf17c6d0f84ff4bc73830a2cd433ab548e7e900ec682f96`  
		Last Modified: Thu, 13 Nov 2025 21:06:57 GMT  
		Size: 8.2 MB (8203669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04190db502b11c48dcfea3bc4ec00f866796bfa4d36b08e86ae6ebed05fc8440`  
		Last Modified: Thu, 13 Nov 2025 21:06:55 GMT  
		Size: 1.3 MB (1311449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcbae59ea6675fca2fb9887644c47f426278ef327002b45edf817948e9da80e`  
		Last Modified: Thu, 13 Nov 2025 21:06:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5745be5791b1f657000740addb179031b4bedc62fa41c6222bc79482b35c7c1e`  
		Last Modified: Thu, 13 Nov 2025 21:06:55 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a32bb9eb1e920b5e26693d39365ff5f4d0a6a4d16d238ef0bdbd76b2a774d3`  
		Last Modified: Thu, 13 Nov 2025 21:07:14 GMT  
		Size: 113.1 MB (113086543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61f021cf60d29e801e814136882ee0d2ffbeb986acb3a45e73009190d3124cd`  
		Last Modified: Thu, 13 Nov 2025 21:06:55 GMT  
		Size: 10.0 KB (10016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cadc651aecd4673e18d1d7b02144c8089e8ba5b2744b7db6588b2d8ad4ab896`  
		Last Modified: Thu, 13 Nov 2025 21:06:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3e249891c616791245b33bb695bf3b7f5cfe63e559854c3f7b5be7d7494ca9`  
		Last Modified: Thu, 13 Nov 2025 21:06:56 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e01419f12cbdcddcebf9666463a287821b9bd366f4c3020cd54578b47fb198`  
		Last Modified: Thu, 13 Nov 2025 21:06:56 GMT  
		Size: 6.1 KB (6080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ad62f6f3595b5b5a1545831598c2c0d99faa99b80b0e9a1f42b0721617f994`  
		Last Modified: Thu, 13 Nov 2025 21:06:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b738196b13e2fd14fe1b0203ac41f460ff9ffdbb2ade0c570ba1563e20ba91c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4192a2b7e644ac588deedecba6bd3d86be83a36e0a5b397a547694a75879dc`

```dockerfile
```

-	Layers:
	-	`sha256:d735b83b868f52eabfc9dddddf1d05df196e51e5d496d8723190ff8692afd0cb`  
		Last Modified: Fri, 14 Nov 2025 00:15:27 GMT  
		Size: 5.7 MB (5708452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd697eef3aa2a3f0041dd4d815ad7e25723bf54c7dd950071274a73aba05282e`  
		Last Modified: Fri, 14 Nov 2025 00:15:28 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:418ce83feca26f614c7deef41c89717184771e3ae56ee7c756b13ece272297d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154129914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23f069bd1c27d20cc487a38d94a885b8f3ac5b5b116d2ffadfa43266c6f000c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Thu, 13 Nov 2025 21:28:56 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:29:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:29:16 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:29:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:29:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:29:25 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:29:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:29:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:29:33 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:29:33 GMT
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 21:29:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 13 Nov 2025 21:29:33 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Thu, 13 Nov 2025 21:46:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:46:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:46:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:46:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:46:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:46:29 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:46:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:46:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:46:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:46:29 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:46:29 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:46:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47413862cdef39f5168140cf10736acca64b622e973df028d54ca0d553fb41d0`  
		Last Modified: Thu, 13 Nov 2025 21:46:58 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97edbeaca4d4c0d8deab75ce8d2fef8f3f9cf590a43dc33a42dcc765552c7e7`  
		Last Modified: Thu, 13 Nov 2025 21:47:01 GMT  
		Size: 5.9 MB (5928937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9b61fe2d7d4b43180811d8a80ef8ebbd6fdf8287a5d1bc87619b1a852e5a90`  
		Last Modified: Thu, 13 Nov 2025 21:46:58 GMT  
		Size: 1.2 MB (1227328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caa23ef6038d492880df9f04e79428c18281f62696413b08d5c0eea4cdce66b`  
		Last Modified: Thu, 13 Nov 2025 21:46:59 GMT  
		Size: 8.2 MB (8204114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65e33a20df8753582c4e57dc6a557a196e86a0e77999866dea7768751c4f1db`  
		Last Modified: Thu, 13 Nov 2025 21:46:58 GMT  
		Size: 1.3 MB (1317109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b0a5a90d8f7e26af69551f75790e390957640b346e2dfc88754852a09057e4`  
		Last Modified: Thu, 13 Nov 2025 21:46:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b5e0fda3a628efe72e23b9f65e687cf6861d09c2f19ec8f7e2933baaa11af`  
		Last Modified: Thu, 13 Nov 2025 21:46:58 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378267ee915ab8c137126879b4478282ebfed69abfe27cbfa339ff8dff686cf7`  
		Last Modified: Thu, 13 Nov 2025 21:47:09 GMT  
		Size: 109.5 MB (109484992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0712f6825885a1516df4a2acfaa6fa29dc0ea84e62b3a795f5b0e5d1574b93d`  
		Last Modified: Thu, 13 Nov 2025 21:46:58 GMT  
		Size: 10.0 KB (10012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dfa66f3dddb1ff9fb7a3551403a93136e610caf02cc9c5c0ee57ab6cdd4c9f`  
		Last Modified: Thu, 13 Nov 2025 21:46:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f4601533bbf737ba295b148a208699e6bd6e52a5f0e9aa2cf106b21c6835f8`  
		Last Modified: Thu, 13 Nov 2025 21:46:58 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd4e524c8d489ef5cce2bcb44f7fdd6a38bb44f09edbff93254d26613117e83`  
		Last Modified: Thu, 13 Nov 2025 21:46:58 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d809690aff6e244d3806f2f23371b44c32a32601a061fc0cf106a09508d402e`  
		Last Modified: Thu, 13 Nov 2025 21:46:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:24e1da7d6096d9bf3a3e2c5edb1979e9fad1c5adbcef8e69276d0e7ccb3415d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3517c5e68b72b6917d116710717d7275f86334f3ac28dd57b49820fd3d3c11`

```dockerfile
```

-	Layers:
	-	`sha256:6e5b6ee4da41d8a51c64f76411d4f4da2f38098f13e6ee92b319d9d0d7c49541`  
		Last Modified: Fri, 14 Nov 2025 00:15:34 GMT  
		Size: 5.7 MB (5725090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c39ef83cc9b2a150757fd7f0a6e9692fd755bad6075e3adabc9871737c2da5`  
		Last Modified: Fri, 14 Nov 2025 00:15:35 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:5fe002d240cd52d08db7aa1fe2070f501b8a656625d0c29a8e4d2fbccac83dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149187799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e482096064eebbbe9bf0a0707d8c8979fff72b26cef85e384e9302cbcba1cead`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Thu, 13 Nov 2025 21:12:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:12:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:12:41 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:12:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:12:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:12:48 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:12:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:12:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:12:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:12:54 GMT
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 21:12:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 13 Nov 2025 21:12:54 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Thu, 13 Nov 2025 21:28:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:28:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:28:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:28:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:28:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:28:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:28:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:28:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:28:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:28:07 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:28:07 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:28:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1368425d4d60385f6b93c853e46a4d8120161098c4a371caac694eaa69d91d`  
		Last Modified: Thu, 13 Nov 2025 21:28:37 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd73360c88b20aaf314390098fe76d435dda048d7f6acb7afe9ec75b999203f4`  
		Last Modified: Thu, 13 Nov 2025 21:28:37 GMT  
		Size: 5.5 MB (5496733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f086b875f9092847416ab102af3a0314319423698c9fd2ba9c2a24f58a057451`  
		Last Modified: Thu, 13 Nov 2025 21:28:37 GMT  
		Size: 1.2 MB (1222211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6234c2ec60a58b28684b07ce038d2c95c95d32d9731f65a7a59a1e0dd14738e3`  
		Last Modified: Thu, 13 Nov 2025 21:28:37 GMT  
		Size: 8.2 MB (8203912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270cfc7dc3304a7e0b3eb2cdc836caef19ce9344721c3b181aa9dbb277985b3a`  
		Last Modified: Thu, 13 Nov 2025 21:28:37 GMT  
		Size: 1.2 MB (1172438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e46faba6b05cc8b736f17778c2edad512c206f29e7eb797757883648af650f`  
		Last Modified: Thu, 13 Nov 2025 21:28:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c531ceb9b63eac7d32ce2da9c1e66f8afb753ee58dbb81d6eade15c457c0259f`  
		Last Modified: Thu, 13 Nov 2025 21:28:36 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f12a2e700816abf38d2d53f4f4beb1c358f0db6c4fe28d4308cf22eab56b5135`  
		Last Modified: Thu, 13 Nov 2025 21:28:51 GMT  
		Size: 106.9 MB (106858447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90aa42919cc45ed602382acc48b04e70e47a395541af5b63eb55b01a3fc3c56`  
		Last Modified: Thu, 13 Nov 2025 21:28:36 GMT  
		Size: 10.0 KB (10029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33b353613e938781ef13937dfd5285514ce6afacc8fd3c1358193702fc26c18`  
		Last Modified: Thu, 13 Nov 2025 21:28:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca301069b59dc44c485e4f34c994ce87c2b71af69242babf3e32cf430c17966`  
		Last Modified: Thu, 13 Nov 2025 21:28:35 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d7bfdff54f4934efc3e14d8c30431a10c760674cde5ace8c9aebb5fe242ca8`  
		Last Modified: Thu, 13 Nov 2025 21:28:36 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a58fbd67c0311a71612718f00361f97b7059ed95ba924b39cba94cc4b1c9b12`  
		Last Modified: Thu, 13 Nov 2025 21:28:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:8ba9da78f073224138d61f24afce2226623d9fb40e584f210357df0b12490243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a4a6db7d835e53ab26c370f3af4f00132f63084c69f0ad0c5616a9bddf81f3`

```dockerfile
```

-	Layers:
	-	`sha256:3a4164f5be05cb01633d112e80e64603a3a62a70499860e8b78d65c3518f9fa9`  
		Last Modified: Fri, 14 Nov 2025 00:15:40 GMT  
		Size: 5.7 MB (5724395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16191163d5c5bd8fb4da630907abbbeb3f2de267255c1780a64cfaf188000b3d`  
		Last Modified: Fri, 14 Nov 2025 00:15:41 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:cfeafa814c65ab01f04b1699562817f29a47ba7c51ce4b9bebeaeeaea85176c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158727890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c62cd09409d5c8ca4013d84f660846ab5194f21b3fa152c725504e162b9a70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Thu, 13 Nov 2025 21:06:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:06:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:06:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:06:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:06:19 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:06:19 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:06:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:06:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:06:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:06:24 GMT
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 21:06:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 13 Nov 2025 21:06:24 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Thu, 13 Nov 2025 21:07:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:07:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:07:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:07:31 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:07:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:07:31 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:07:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:07:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:07:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:07:31 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:07:31 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:07:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15423387f194832aebcb45a43a0e3c540536e5d10eb2b499afbb5ec4350b804d`  
		Last Modified: Thu, 13 Nov 2025 21:07:08 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8687d5b37f0ebb3b5807be9ff3dfaebaa17d98a76daffd08d187e6cdb737a3b6`  
		Last Modified: Thu, 13 Nov 2025 21:07:10 GMT  
		Size: 6.2 MB (6231970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1183f06c300a72345eabf68ee5492c4900bce080e3f0324651e587c32ae94b`  
		Last Modified: Thu, 13 Nov 2025 21:07:08 GMT  
		Size: 1.2 MB (1209369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be383daf50ea30e04ad111359426188d853aa3ffdf3591a0f19bd0d10a5cee5`  
		Last Modified: Thu, 13 Nov 2025 21:07:09 GMT  
		Size: 8.2 MB (8203863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5c71945f0fd2fd85b1a2d811f6049b4c673a73355571d63dbe74a8b7258b87`  
		Last Modified: Thu, 13 Nov 2025 21:07:09 GMT  
		Size: 1.2 MB (1220399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343d44b62aa0b28e94612b616ba19c8940bae9d3f6b0da300566ea6b20385173`  
		Last Modified: Thu, 13 Nov 2025 21:07:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d935f16db36ff44bb89f7aa909a4bc0fbee80767215ab3579c1fa2341b6a617e`  
		Last Modified: Thu, 13 Nov 2025 21:07:08 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54eb8e22f6e660a9be6ee0cbedd8662411c3be7606dfd015c7b0c078e41286e2`  
		Last Modified: Thu, 13 Nov 2025 21:08:20 GMT  
		Size: 111.7 MB (111698986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e313eb8f7fd6ed51b00d650f7c2afa2dd0c2f63441346264a3cc165ff4a1266`  
		Last Modified: Thu, 13 Nov 2025 21:07:58 GMT  
		Size: 10.0 KB (10017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d57085366254beb172b30635b72ec6998e8aeb0b4d03b90a2e9ab213425e3d`  
		Last Modified: Thu, 13 Nov 2025 21:07:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce06062c6277350b5fbd50ff7b083a2d0f7658416d1b529ad226c51a2f1b387f`  
		Last Modified: Thu, 13 Nov 2025 21:07:58 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee63f29b8cd00c98d8b637a1c79504d43f656b98c3be800ec1e7c4a58986bca`  
		Last Modified: Thu, 13 Nov 2025 21:07:58 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef1a72d157136746540cddeb7eda33c0850d107233386b88a2a1bc543aaf602`  
		Last Modified: Thu, 13 Nov 2025 21:07:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b6a2525f94c1beda8a1222dbdf7486d75ff4736cb6873e553498f05ffd045498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747eed398c95485447f91fb6401cb30ed804ac45b0e74204e73b0a681fa1154c`

```dockerfile
```

-	Layers:
	-	`sha256:2138e486d9dc909d042b36130b1b5308e0a22aa424ef4b11ccf6eceece09edcc`  
		Last Modified: Fri, 14 Nov 2025 00:15:48 GMT  
		Size: 5.7 MB (5714798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7a445109e0bcfdfd6421f229b5e2f603ad2099507b85ee311b63b7aa57bc61`  
		Last Modified: Fri, 14 Nov 2025 00:15:49 GMT  
		Size: 54.1 KB (54136 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; 386

```console
$ docker pull postgres@sha256:0e5304879c115d8beced1accb5af076ceda67b4d70e2dd8b974a037d74eeb72b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.2 MB (169224324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3da3be9b9d17447eb516172085e27ec2accf5f89e0b70a237853aaca92479af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Thu, 13 Nov 2025 21:10:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:10:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:10:31 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:10:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:10:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:10:37 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:10:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:10:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:10:41 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:10:41 GMT
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 21:10:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 13 Nov 2025 21:10:41 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Thu, 13 Nov 2025 21:21:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:21:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:21:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:21:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:21:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:21:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:21:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:21:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:21:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:21:23 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:21:23 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:21:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161e430ba6a9e1f2a70747ad57cee52e5a522bc26c6d109609940320fd73b76c`  
		Last Modified: Thu, 13 Nov 2025 21:21:54 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf9633f4704906e5b173d69cbf397f45e774a62334ab9b57f5e878ec8210f1f`  
		Last Modified: Thu, 13 Nov 2025 21:21:55 GMT  
		Size: 6.6 MB (6629450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616a7d2783f23f6ad99262f0aee87967261c25f074c8a6d7d1927b90ce555a02`  
		Last Modified: Thu, 13 Nov 2025 21:21:54 GMT  
		Size: 1.2 MB (1225630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6016cc9ea3b73706be4fdb6cead2d68b9c3ba153462c861cd70efff51de826`  
		Last Modified: Thu, 13 Nov 2025 21:21:56 GMT  
		Size: 8.2 MB (8203899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637a12a3f7c04ceed1ff58300027f810223ec1f607ea7fe2b5394e24fda56449`  
		Last Modified: Thu, 13 Nov 2025 21:21:55 GMT  
		Size: 1.3 MB (1308101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455e7ab16b0f149a50498549f588076345bc7c99058a8b60fdf29b851ba2e699`  
		Last Modified: Thu, 13 Nov 2025 21:21:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894239233b1deaa03ecd3114842d23c0892a16a317bc2686d1adc9f5e97bd0e7`  
		Last Modified: Thu, 13 Nov 2025 21:21:55 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa1da4c5c9b281208e9084353a6660119225e49f5a4d05838569ad93c5c0e70`  
		Last Modified: Thu, 13 Nov 2025 21:22:06 GMT  
		Size: 120.5 MB (120541445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca57b06fb5e8f2eb45d819307004d1fa2d7b5ec19df2ec95fa08eba7782f873f`  
		Last Modified: Thu, 13 Nov 2025 21:21:56 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca135aa70006c48afa4e4dbfeec9170fcd02e999ff10d8381de32854001224`  
		Last Modified: Thu, 13 Nov 2025 21:21:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb3e0b8b89e30b93114b368b725813c7777ac65e0d2ee7e36932738eb0b52a6`  
		Last Modified: Thu, 13 Nov 2025 21:21:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7875249ad7f21c82cb07d7ed5035657a215504794ee69a9303863ff6f76f4af`  
		Last Modified: Thu, 13 Nov 2025 21:21:53 GMT  
		Size: 6.1 KB (6080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ccaa27faa936ee6ff8c47c6529dbc886421977d18217b85446e522bc8c22e`  
		Last Modified: Thu, 13 Nov 2025 21:21:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3638257f9cf4efa005c888c5fe27b762f3ea98e21796cb4f2cdddabc231b947c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdee60dd84e657db095c7110dddf10e75813d88ec49e4a45d0c45f80f8884884`

```dockerfile
```

-	Layers:
	-	`sha256:9e178c084673bbdcfef848d5fd56014b686a7c647a0d2f7f2bbb4a15eb64cdb0`  
		Last Modified: Fri, 14 Nov 2025 00:15:54 GMT  
		Size: 5.7 MB (5723983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b735138e1d8f8d95a8730fb626f1c378010e4bc0fc824ccd5e5b9a4cf43661e`  
		Last Modified: Fri, 14 Nov 2025 00:15:55 GMT  
		Size: 53.8 KB (53814 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:9d7136ba29cf065e20bc72169af336a8de1a378e3c67511d5b35a54115d12da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172376602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d29eb7e5db5dbb34360dbd2ef08d26d09b4491a5de7ab02069e6ba3292303e`
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
ENV PG_MAJOR=16
# Thu, 13 Nov 2025 21:04:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 13 Nov 2025 21:04:27 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Thu, 13 Nov 2025 21:27:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:27:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:27:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:27:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:27:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:27:19 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 13 Nov 2025 21:27:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 21:27:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 13 Nov 2025 21:27:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 21:27:20 GMT
STOPSIGNAL SIGINT
# Thu, 13 Nov 2025 21:27:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 13 Nov 2025 21:27:20 GMT
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
	-	`sha256:231d6148e4eb4e282ab3e9094fb3da8eb320faf504a30e30d234c00b104ebeba`  
		Last Modified: Thu, 13 Nov 2025 21:28:28 GMT  
		Size: 120.9 MB (120867827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a59bb620153ba6d11e2dedbb081202c95fdbd87ad1989cee519a7291df01d5`  
		Last Modified: Thu, 13 Nov 2025 21:28:15 GMT  
		Size: 10.0 KB (10014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ec99b6dfb6cc3bb6e38d5381ddb8a629eb42ecf61c416bedef916028daf0e6`  
		Last Modified: Thu, 13 Nov 2025 21:28:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0712708d7f3c8408648dc7033cbb6815ff5e011f4d1c6ce7719e5b87d40c50b`  
		Last Modified: Thu, 13 Nov 2025 21:28:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654eaf71da4fb1c2dfb510810c614bd576c851d7d2ce026ee96b4d1e0f1ada8f`  
		Last Modified: Thu, 13 Nov 2025 21:28:16 GMT  
		Size: 6.1 KB (6076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dd1929bca0cb4c9edb3e358e34178e19b8e6d71b4de1d31cd595e46962e142`  
		Last Modified: Thu, 13 Nov 2025 21:28:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:668095333d4437f4d5c1003b17bacf06c1d63a48b19eb7d5d5eb5f7510ff5591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2851b7f011ab058d9d20e31a75fb9aa8a8e58a651ad5deca12fc0071d556106`

```dockerfile
```

-	Layers:
	-	`sha256:65a79f722747c0e362e2540104c36d2e0ca5691f18fb714f1f386f1ad00240e8`  
		Last Modified: Fri, 14 Nov 2025 00:16:00 GMT  
		Size: 5.7 MB (5715065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7194587508b4f9acdcec95aa7e236ced961dd143dbf05a89266b02be91dac3a`  
		Last Modified: Fri, 14 Nov 2025 00:16:00 GMT  
		Size: 53.9 KB (53935 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:4bb24cd9589599a7130c7ee48221fcdd02582e6211428c2205c153bc10ef1bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91555741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144b06903748e3f6ca880d7b6729b665f6ecd88bc30fdb5122db339df29d7331`
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
# Tue, 04 Nov 2025 23:40:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 23:40:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 23:40:44 GMT
ENV PG_MAJOR=16
# Tue, 04 Nov 2025 23:40:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 04 Nov 2025 23:40:44 GMT
ENV PG_VERSION=16.10-1.pgdg13+1
# Wed, 05 Nov 2025 05:56:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 05 Nov 2025 05:56:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 05 Nov 2025 05:56:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 05 Nov 2025 05:56:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 05 Nov 2025 05:56:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 05 Nov 2025 05:56:54 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 05 Nov 2025 05:56:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 05:56:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 05 Nov 2025 05:56:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 05:56:55 GMT
STOPSIGNAL SIGINT
# Wed, 05 Nov 2025 05:56:55 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 05 Nov 2025 05:56:55 GMT
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
	-	`sha256:5af6530943e62dddd2214c6214c58c02099cb95a457b9c738100e4a19effed57`  
		Last Modified: Wed, 05 Nov 2025 01:45:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48eab6e502071b87813887619a512bc10b86131fd46b99fa09a9a19b4386811e`  
		Last Modified: Wed, 05 Nov 2025 01:45:45 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668a823ecc08bcb22d962d45c09cd0024776aa771934f32a2a2dc88f8aa0e843`  
		Last Modified: Wed, 05 Nov 2025 09:12:35 GMT  
		Size: 46.2 MB (46160014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742d76d94c48fc835ead242a90331939594267d6e8f4c31d3ddea6299b82a927`  
		Last Modified: Wed, 05 Nov 2025 06:17:33 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d68341dc22b412f26bfc1405c7894019079913a0ff5c9cf5aee5133c06f84f`  
		Last Modified: Wed, 05 Nov 2025 06:17:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1e54c8c7355e505530a1c8f6224d4927b2b3b4a8e005465ad07b37929ec5ce`  
		Last Modified: Wed, 05 Nov 2025 06:17:38 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6588e3b7fbfd2b47333cb501631695a2e6fc15728f9366c6f1891e4b033cd5`  
		Last Modified: Wed, 05 Nov 2025 06:09:14 GMT  
		Size: 6.1 KB (6077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb65344cbb46a9f790504f698d037813dfcce7716e784807ed387bb8a20414d`  
		Last Modified: Wed, 05 Nov 2025 06:17:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:780359da0d23ac325a87d506a9effa1e7e87765790c0917772343727ce6d8598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5128658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca19c88266b52ba3bc8dfebc9a4a9b32a867d79b41bf972410578370272d3ac8`

```dockerfile
```

-	Layers:
	-	`sha256:0116abbb8f538f797345008ca396c39030253f204ab8afb4b4be71590616aae0`  
		Last Modified: Wed, 05 Nov 2025 09:08:43 GMT  
		Size: 5.1 MB (5074731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0c97cb1c0e109fa4961979670876d86b271aae369828210fb351c8d8f97af00`  
		Last Modified: Wed, 05 Nov 2025 09:08:44 GMT  
		Size: 53.9 KB (53927 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:d15bd101e36a85166f90b43fafba1cc158f7f1c78f6f1a3b54bdf43510f6eb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174625520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e8fc3ca99ada253f1d8e74bd444dbbf7af190d2f3d92554eae53c5297a9e75`
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
ENV PG_MAJOR=16
# Fri, 14 Nov 2025 01:10:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 14 Nov 2025 01:10:46 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Fri, 14 Nov 2025 01:34:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 01:34:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 01:34:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 01:34:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 01:34:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 01:34:55 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 01:34:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 01:34:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 01:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 01:34:55 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 01:34:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 01:34:55 GMT
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
	-	`sha256:44b00d0e58818afdc631c2e94d21741a402f818e506ba0d46808169e1d19f881`  
		Last Modified: Fri, 14 Nov 2025 01:35:49 GMT  
		Size: 127.5 MB (127471603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87843820fcc4ee948e2f99c72064c153f029233906874c92034d457586356712`  
		Last Modified: Fri, 14 Nov 2025 01:35:34 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78568d0decedf4c6a8da433c98e6fcd948d38d3d617131f73be0881b6880698`  
		Last Modified: Fri, 14 Nov 2025 01:35:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5275b35876d34b48442af358111588b60217b9931395c3c328bc83872b6a5d`  
		Last Modified: Fri, 14 Nov 2025 01:35:34 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b555047ca485e8ccfb3451162a1b592a724f00b8ba75b7fd8f8b22df57ae8d`  
		Last Modified: Fri, 14 Nov 2025 01:35:34 GMT  
		Size: 6.1 KB (6080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429f4cd662d2f8f352a55df4b85302e80af537c5f90b507134bc3db370fb335`  
		Last Modified: Fri, 14 Nov 2025 01:35:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:f4be0ffb69db56d3d1682b1eefd627c9a0a0289137336e21ed22b8dfa760ac89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef687113e1506d9e50d1727cf0952828bfd3da471b158f227d45d34cf758399`

```dockerfile
```

-	Layers:
	-	`sha256:4aee11a3536ebb00449b8c5dc1945a7128c3e3be811407e7274918363e5aca80`  
		Last Modified: Fri, 14 Nov 2025 03:09:04 GMT  
		Size: 5.7 MB (5725121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f125fd74268fa7d3f80c7939df8f87f5120212c16159b523a54be1950f51c1e0`  
		Last Modified: Fri, 14 Nov 2025 03:09:05 GMT  
		Size: 53.9 KB (53868 bytes)  
		MIME: application/vnd.in-toto+json
