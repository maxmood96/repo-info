## `postgres:18rc1-bookworm`

```console
$ docker pull postgres@sha256:e8ed3d72a00eaeead9fb10ca7d59cb53250829436e657402af5490f04fc76491
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

### `postgres:18rc1-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:13c238f0a17eee5ede7f5346745f3b69dde182be21853eeca94ab303485c312e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157278766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6e044377baff49fde9698ba3cc75818568f02be6e9bff5f22356f2a14de7da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18~rc1-1.pgdg12+1
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde9b6d2c51239ae34af4fc3e36ad2cdf574dcef2e94ee5ab903b9ebcf556ab6`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab733d7b8d376f184be7b00203dd4cb706a4099005d21c1eab12614d7e1f5369`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 4.5 MB (4533736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab375dfeeb77d6dba08a73c1ba25292374c9d3abc1a9966bc11aa36b62ca87`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 1.4 MB (1446770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdebc74167c49377add0ca7a2febfcc724a41e968e58c5bc4f1a29217c287683`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 8.1 MB (8066284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e49c179f644314272720e70cc147ea054755dbc1164fcaeeb349d07a3b832b`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 1.2 MB (1196128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727bbdbc0133757343c4c7460728743ad7e3c2ead79725d6a98ed148da09ab73`  
		Last Modified: Fri, 05 Sep 2025 21:46:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739372bb6b4f9d1b693c2ab6361b71376d8ff171ddba5dcb9d8a60ece3d9038a`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb490d937b1a843c47766c3a276b26db4ea49de29c0b1c090167294388c1611`  
		Last Modified: Fri, 05 Sep 2025 23:32:35 GMT  
		Size: 113.8 MB (113775654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692c9e9fa177a4cff169ff7ca57f085e8cf2a8c4834cb042d3d4a61d2a4ea0a6`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 19.1 KB (19087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b6db481c32d2e62d5c4d8a3242437c349888e5fb383e1556d4f88f604d247`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2a8392e02c2a035925d125c1c4f53c9f0287da061de06edc178e3088ecad2d`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e3cf143cb614b0dfc59019b37111ed3b23c6f5b1d1c271ac6722111e32f702`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b856aa459414cbca63c2ee8e0ccf3ae02cfe79b38da0340c4e0fe32365e169eb`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d8835ce6d5efefd96b16973661c3e5a9e9b09808d7b09841f3bd371bc79d0339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6290004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a579119ea96977bb66c1f1dc6b1996a40750bbedb426bffd0367e35915e28f`

```dockerfile
```

-	Layers:
	-	`sha256:b297bcb94e02b2179cd6c252aa755e3b4eeec43e0bd9af729e4b26ee46106579`  
		Last Modified: Fri, 05 Sep 2025 23:14:39 GMT  
		Size: 6.2 MB (6235865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14cde0f881f46172600b643f5f83305346fec998ee2176e7ce3f8d3c9cc59c77`  
		Last Modified: Fri, 05 Sep 2025 23:14:40 GMT  
		Size: 54.1 KB (54139 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:e6450372d5a2310f4e072157cdb7c5a113c48fd83cba0d5f1ed0cf9c0249864d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87405905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1e4c5114b498ecbc9f80733b7247e9fa5aef3868a27e5f6a0e0e7a8d946713`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18~rc1-1.pgdg12+1
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b424299efd3c177df3ac4a00bdc9fbf1116c3205c415fac6112b388ca627939`  
		Last Modified: Fri, 05 Sep 2025 22:01:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bde0dc094c582ab7a21a3c85203c9c3fd34774f995ac33460e1516b06b58014`  
		Last Modified: Fri, 05 Sep 2025 22:01:02 GMT  
		Size: 4.2 MB (4150945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7cab0580d5339c883fd131c8633d3cb83d99ec20c3514fb103bf93a3fa0083`  
		Last Modified: Fri, 05 Sep 2025 22:01:02 GMT  
		Size: 1.4 MB (1424026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67515b199cc0687ea354b92d909f40f9dc5cea3a53d1a86a02f6f4dc67f2487f`  
		Last Modified: Fri, 05 Sep 2025 22:01:03 GMT  
		Size: 8.1 MB (8066385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513b8f58276cb2ce192eaec0276218d358aca09f91260547317fb1e568330eee`  
		Last Modified: Fri, 05 Sep 2025 22:01:03 GMT  
		Size: 1.2 MB (1194867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9dc5213eae023ba63a6186a492190aa68c299670f843123bd0bf1181699267`  
		Last Modified: Fri, 05 Sep 2025 22:01:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec623edf18450aa195821a5f6273a42c49db89e34abace3e4e5f50697d0c0811`  
		Last Modified: Fri, 05 Sep 2025 22:01:02 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05d6a1a2956b6108aa2a80f7f19d09f264327a4741ceee734768346be10c70c`  
		Last Modified: Fri, 05 Sep 2025 22:01:10 GMT  
		Size: 46.8 MB (46777020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21e9414cfea1671e0e49dcfa6af6c0a460a112f004c0bdb9b02c69b3a0b5c9b`  
		Last Modified: Fri, 05 Sep 2025 22:01:04 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8562747b14fc9d89fcd515ae3ef21e456a88d47ea3cc8162d08a89b67abc14fe`  
		Last Modified: Fri, 05 Sep 2025 22:01:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2159d0621b4b1c286d7e3b6579a445e39ad7a3c32f713c0c20a4ebcc18881390`  
		Last Modified: Fri, 05 Sep 2025 22:01:03 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80eb25589a39f453457cc11c8daf249c191d3fa1f868fa9ac4dd2c6334c00d6`  
		Last Modified: Fri, 05 Sep 2025 22:01:04 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975856a2dc4dc5a28e7305203f6053b39ed06ef54722739c1f925409bf6a7e8c`  
		Last Modified: Fri, 05 Sep 2025 22:01:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9c04fd9b02d22f669830e2f145c375d30826205bf0b288c6c44d0d72d22ccebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e2e73ca8d3ff47ac934988db39668b1febf44a9d088b22f3e285acd2b7d0c`

```dockerfile
```

-	Layers:
	-	`sha256:9d01393038626ad4a47ade0e46a6786f59fa024a0952856e8f9ada2b71ab67fe`  
		Last Modified: Fri, 05 Sep 2025 23:14:46 GMT  
		Size: 5.4 MB (5396368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9191301a473540b89bbd98567452923b9613f6a39c46dff2551d409b710751d0`  
		Last Modified: Fri, 05 Sep 2025 23:14:47 GMT  
		Size: 54.3 KB (54332 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:257394ae76d3708ab4cb6b2551b08c64b0f9d46f6a5519204204a09e5371bf6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83516783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3d432bca61e13f2006f93be99c19e56b1ca51155e62daabdecf644c1daeb0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18~rc1-1.pgdg12+1
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d71953da4989097f1e3a63e662723835e3905da38632b16b912735cd8db0e8`  
		Last Modified: Fri, 05 Sep 2025 22:17:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3efc275e6a19d18330be2149a94a5a6a1874e2bdec3c943cf80284e5235f1f6`  
		Last Modified: Fri, 05 Sep 2025 22:17:12 GMT  
		Size: 3.7 MB (3742529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f778fb09226afd38917f1d3562914f3e5fc9bb4d28eb0750dd8abd5a6aebbc`  
		Last Modified: Fri, 05 Sep 2025 22:17:11 GMT  
		Size: 1.4 MB (1413753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3a4e6d5fc2fca00a39aac2f8a68bc443acd1e56e08137b220d701cc0da1e1`  
		Last Modified: Fri, 05 Sep 2025 22:17:13 GMT  
		Size: 8.1 MB (8066277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99fee11ebbe56f98eb3cf3ca837ed5e49362ab14be8a9ffe13d8b5731b62f32`  
		Last Modified: Fri, 05 Sep 2025 22:17:11 GMT  
		Size: 1.1 MB (1067045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d433606d95d5b754ad8e3c7adf4935761c7c5ccacf128e3678ca268687249`  
		Last Modified: Fri, 05 Sep 2025 22:17:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7360e63d15bb549a7912f177b9e8bc03244bef92b8505909a87b160be0941f`  
		Last Modified: Fri, 05 Sep 2025 22:17:11 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dc49041fcf93cff3f6cffec5abb98e7c444fe6156693a24737c11bd94969cc`  
		Last Modified: Fri, 05 Sep 2025 22:17:24 GMT  
		Size: 45.3 MB (45258306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc1ce685a102baee6436202213614a6beeb37e05c7ea276cc63a730a8a49955`  
		Last Modified: Fri, 05 Sep 2025 22:17:12 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08bf3384470d70cdfc619d8426913e70592120a9b3603806d4b6d81917ed29c`  
		Last Modified: Fri, 05 Sep 2025 22:17:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bc12d380db44fcdc614de260c27aa1f0c44b28f244bfd9ba30ffbac7d49548`  
		Last Modified: Fri, 05 Sep 2025 22:17:09 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7287ab40b2b90ae88776a7dd86f54d922bb33c1e85c6580a7c5698342d3c18`  
		Last Modified: Fri, 05 Sep 2025 22:17:09 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec9ca6f2d1e2b289856113bc924a1fe9fbe63bb9a2cb61c3392eb9d1404f33e`  
		Last Modified: Fri, 05 Sep 2025 22:17:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:aaa3859962881269927af946888a61087d5b39bc2ac1ce7de6992e6118bf4c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfe2448fce36088a3b45f0268d87bf5c0c8126b5ba894ef07bc42a700e15edc`

```dockerfile
```

-	Layers:
	-	`sha256:67d061362139689d46b6ac72d586a8ba1f8a4ca1b07c3a00542a6849a22df157`  
		Last Modified: Fri, 05 Sep 2025 23:14:53 GMT  
		Size: 5.4 MB (5395627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f009fdbf9dab765bb211b478716f29fb3ef80758888bd38d1d00a9abe9f5c70`  
		Last Modified: Fri, 05 Sep 2025 23:14:54 GMT  
		Size: 54.3 KB (54331 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:29093109718034bf90bd17bd95d115838eb2520fd848adc05eb43f6b136a7f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155177759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259de938619fb740e930da1f6d66d7282222b85636799042314b3fb988688a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18~rc1-1.pgdg12+1
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befcce40b621fbe95f73a30721620ad16271d6676bbabf57d0cbfe4c57d1891f`  
		Last Modified: Fri, 05 Sep 2025 22:03:56 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85675c2ca9ed184523c98566332f026377c55f0117e027c5a1ba435afc02291d`  
		Last Modified: Fri, 05 Sep 2025 22:03:57 GMT  
		Size: 4.5 MB (4499254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80c060c058ee212d05ba29cfb6571be7642a92de24a2eae93be3aafc2aff1a4`  
		Last Modified: Fri, 05 Sep 2025 22:03:57 GMT  
		Size: 1.4 MB (1378825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1164de88ca69203ab67dda98d627ece2406d2fe10c7b559b9dfa387c7261ac`  
		Last Modified: Fri, 05 Sep 2025 22:03:58 GMT  
		Size: 8.1 MB (8066341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f770a9b39eca36486462244b70ce86b1775d43ac5af04ce22d7231e829de6`  
		Last Modified: Fri, 05 Sep 2025 22:03:56 GMT  
		Size: 1.1 MB (1108763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53319d5765b41067de981c4ae327dcae12baa8896ea884b95d10e3dad633c2da`  
		Last Modified: Fri, 05 Sep 2025 22:03:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52400312eb8ac3260e942134ff18ffa7a6f2fd9ad760e2b6016868f7b0cf525c`  
		Last Modified: Fri, 05 Sep 2025 22:03:56 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f354a200b3d06044aae47bdc3778d6a7c62232526ed83108787b058a79b6f45`  
		Last Modified: Fri, 05 Sep 2025 22:04:15 GMT  
		Size: 112.0 MB (112012633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7ce7c6a79bff07166071d4455c39110033da156db3d5c258ee259b31392f80`  
		Last Modified: Fri, 05 Sep 2025 22:03:57 GMT  
		Size: 19.1 KB (19088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dc0aa0f81f0d1f391f7625ee032474a924e18e853e26c53d3609d4db03d291`  
		Last Modified: Fri, 05 Sep 2025 22:03:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b918df2c2e815baeedb81d78c9c641787a8858556a6c6386b82bf7e01f0884fb`  
		Last Modified: Fri, 05 Sep 2025 22:03:57 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaa4acefd3ba29aad6e5c772fb50dafc2e631a65bc2dd3f6f788bb602dd816a`  
		Last Modified: Fri, 05 Sep 2025 22:03:57 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae53b076a9cb904967fae4ee7202cab80a10847544585031616fec605313c71`  
		Last Modified: Fri, 05 Sep 2025 22:03:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:07cf10fd9da409fc61d41d45f98caa6eeace883ea2d6caed13113421302a60ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6296542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9458111d313a4b53e1409a1b33e383a26ed58c857202b8c7a000cbef6a74559d`

```dockerfile
```

-	Layers:
	-	`sha256:c75b0b73e1d53c74ebe9417c7f89e294449da22e567f9c9e3e07499f5d827bd8`  
		Last Modified: Fri, 05 Sep 2025 23:14:59 GMT  
		Size: 6.2 MB (6242170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d2194d16370c529cbff5de3995773909197605090dd9ee96ebb6484cd901ea`  
		Last Modified: Fri, 05 Sep 2025 23:15:00 GMT  
		Size: 54.4 KB (54372 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:969842bc21ac2712dfe7dffdfe1c11953228fa43d44f4986266bdd1763bfaceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94177066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd27f106a24030de0d38c4ec9bd7ded2ba1503f3c5c5cd1207f91ba3793690e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18~rc1-1.pgdg12+1
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123a404bd3924641d7a1c632623932aa1afd1ccfcc5d05c9c651d663643583ff`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc76191d46fa25a90fc8e538603b3f2babe566c33a019ead65e896318763a77`  
		Last Modified: Fri, 05 Sep 2025 21:56:15 GMT  
		Size: 5.0 MB (4965151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a325a3dced37dc155d2446cb612041168cb518a41882c1ebde9a1c6d203de60b`  
		Last Modified: Fri, 05 Sep 2025 21:56:14 GMT  
		Size: 1.4 MB (1422314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41752c1b8fa0615b4cce8dbd9e0299e5cabe59fa8dce6ebc7fedba764a660c2`  
		Last Modified: Fri, 05 Sep 2025 21:56:15 GMT  
		Size: 8.1 MB (8066277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531b880eb2c6ac878c2b7fb862b2510d001d5ec981313b76923ea3fef4871338`  
		Last Modified: Fri, 05 Sep 2025 21:56:14 GMT  
		Size: 1.1 MB (1137192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6fd646359ee69ece0ccb3fc559616a29528b878a3fc351c7f7d77a00b286da`  
		Last Modified: Fri, 05 Sep 2025 21:46:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686cc60ac40840556a81a975e6c867c7e12bcb0c2a2528132de60eea27846347`  
		Last Modified: Fri, 05 Sep 2025 21:56:14 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61bf2e179da21f99e42048104f0dc73d2db3319cf2c74a8bca2ba10a9dc60d4`  
		Last Modified: Fri, 05 Sep 2025 21:56:24 GMT  
		Size: 49.3 MB (49343580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c96e92a0257ce9c51b33a1411fb84d3bf78861617ba94827ab0033187be499`  
		Last Modified: Fri, 05 Sep 2025 21:56:14 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae7e0288c6aab7fe33ddb0e086c59ec32b0622f7e1c8a8bfa871ba81181d20d`  
		Last Modified: Fri, 05 Sep 2025 21:56:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7859954f63ecdb1db455fa8c1740ed5d850031387252f69825fd0ae906a9f9c4`  
		Last Modified: Fri, 05 Sep 2025 21:56:14 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af2cc97ed73332ac5e4fe5eda1be5521d41cdc03724d3bb5fa30b2e23b166de`  
		Last Modified: Fri, 05 Sep 2025 21:56:14 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08265de30faf603467ab2800632e47c54966e87ebd86657a75bb4d5644c03df`  
		Last Modified: Fri, 05 Sep 2025 21:56:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c191cedf659f3e011ed8de1064bc4ede00d60a9eead31b51fd2fcd2f3cf1e943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7b6a6ce585ac41818e09654d36bcd871be2665a2440b9428757ed703c659e7`

```dockerfile
```

-	Layers:
	-	`sha256:3f39ecf6befe5cf959a055ce11576ba020a1921d7dab64baee69b6ca43237965`  
		Last Modified: Fri, 05 Sep 2025 23:15:06 GMT  
		Size: 5.4 MB (5390948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598f91d8f6d844a155ac025962a43dac2eed226ea1e3c4c057d79676450abbd4`  
		Last Modified: Fri, 05 Sep 2025 23:15:07 GMT  
		Size: 54.1 KB (54094 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:e8eaedf4acd5f26e57f1d31b206455f9bb9ad9ce7fd7c3da1cc10e798fc82a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156118094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c2df3d87f473b735c7a57367d31600c1e2382a977a18ec8aeb4cc8a53e9554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18~rc1-1.pgdg12+1
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83bd2d8e15bdca1c657f4e1229c9515648aa638816bf4ae6a4be5a7afaee3a81`  
		Last Modified: Tue, 12 Aug 2025 20:45:57 GMT  
		Size: 28.5 MB (28516923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29312da7268b11c0e420282a3de73777dd60323a6115c94e4770a3967d1008dd`  
		Last Modified: Thu, 14 Aug 2025 19:34:18 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadf75f6a42f2ec57e669503e79a92f31752f394516ac3907e5fb7ad2261db38`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 4.5 MB (4475161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edb5cc62fc658d056d649cb284f0a020e6a6c0b57162be2680462937f71ab57`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 1.3 MB (1333909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474838f47aaa89f71355146b0a39b988275244759ef97d0cf6e616a991c9027f`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 8.1 MB (8066502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e17ad67a5ccc4d969ff6abab8130942de3726b9e6fad6051c12601f1f8343`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 1.2 MB (1182641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31de7c74bad6aba9b4e3ba53d1a4cfc29234f0d874650d8b3ecb0e3678aa8c07`  
		Last Modified: Thu, 14 Aug 2025 19:34:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cba190353263630bff7d7d1f8db3bf41c59f3df3ef093a60839ff9e4950b3`  
		Last Modified: Thu, 14 Aug 2025 19:34:21 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a123647e63363b32ae2fe86061278c56091cbe4284867509f83cc73139a3b65`  
		Last Modified: Fri, 05 Sep 2025 22:59:26 GMT  
		Size: 112.5 MB (112513003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684123c440dd734269d7340e60c25db4ec4cfc82ed5ceb04ac34ade600c0a0fa`  
		Last Modified: Fri, 05 Sep 2025 22:59:19 GMT  
		Size: 19.1 KB (19098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bbd6ec085ba6839892af8b66fdd04c0ef442b757950b68e231b39d8b19df25`  
		Last Modified: Fri, 05 Sep 2025 22:59:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76ecd62e3294f0726ce1829391d84708d985af6559c7cf6d36a08585ce49008`  
		Last Modified: Fri, 05 Sep 2025 22:59:19 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26ba681cb02d77f589387a495485af0d946c3e05575a25da21adf9045911b8`  
		Last Modified: Fri, 05 Sep 2025 22:59:19 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d6dd1eaad87feff8fb9c1ec8158c01ce7ef2c0205f4ba3cf1cf55af9674f0d`  
		Last Modified: Fri, 05 Sep 2025 22:59:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5158b8794505f3c8586450f6fc78519d7b74284ba12df5ea7c17f260020baab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 KB (53995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d9600ed482f60b209383686834f3b1bf0ee16eaae657e92a30657aa2089ff7`

```dockerfile
```

-	Layers:
	-	`sha256:13a6c171aaf13a11b527a07274deb5f0907459ac72a3161f71c41ae5679fafa0`  
		Last Modified: Fri, 05 Sep 2025 23:15:12 GMT  
		Size: 54.0 KB (53995 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:de388498f8b0a6906a120cc12077666349062f3c22e4af55ecbb7f50f06ba0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170127855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9fd67d157688426a886d1a74b0e196c95e61bd0cd506d1b1b62aa01b6243ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18~rc1-1.pgdg12+1
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8f0a138243b625b991a13aae0989588d5d8ed19498390d04eb08c6603f00fe`  
		Last Modified: Fri, 05 Sep 2025 22:44:30 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416aab4a8205a7d21a17e854f13baf4d5b29cfb10a1c0c27149794378300678f`  
		Last Modified: Sat, 06 Sep 2025 00:00:33 GMT  
		Size: 5.4 MB (5368241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f651748581d2517f6c288b5dd529db3839f0c45a7c62ab58f183211c40b27`  
		Last Modified: Fri, 05 Sep 2025 22:44:36 GMT  
		Size: 1.4 MB (1368769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c91846e8cb9e3d992f9ff61bc1e6f62caf973d753acf3e858878ae587e76595`  
		Last Modified: Sat, 06 Sep 2025 00:00:34 GMT  
		Size: 8.1 MB (8066446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a34128c53d8f3aa219f4b4ad96d559d8605eacc192ed31b7db853d31ec69ec`  
		Last Modified: Fri, 05 Sep 2025 22:44:41 GMT  
		Size: 1.3 MB (1283591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ab6eb21a0d2d2a67d227a28669c9cdcdae932cd343cba6a91dc0725791cd9f`  
		Last Modified: Fri, 05 Sep 2025 22:44:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219addbe85ed3cab3dfbe4ccb5e6575ac78543f97b380120b661fa6884f5cb8f`  
		Last Modified: Fri, 05 Sep 2025 22:44:48 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7144608f4bccb571dfd6e2778ec02f87976c3f246b7c06abdf681102d29174`  
		Last Modified: Fri, 05 Sep 2025 22:17:21 GMT  
		Size: 121.9 MB (121937439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110efcfd33d87cc9fbe0ef0f0d3165a308f133286a94f310e3161635a1e08118`  
		Last Modified: Fri, 05 Sep 2025 22:50:41 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1a8b4c3c0eba6c7699d72d02221b207c09e7e116aecdfcb0baab14abe12f5b`  
		Last Modified: Fri, 05 Sep 2025 22:50:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9664e7c8cc188a0f713c4daba9bed33d3fce09311c122aa07a32e76b99bc7b`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b115697f6c45462b476899cd9627d8c5629377c441a2c0280563a7743af8165`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22acc553f4cc67dad20dc79b3ca664b0fac1a07c63c92e4f58f278b5363e1d10`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:231de7d5ff4eb639ea9680be07ae89df613bdfa78a0d62b2842cbcd3584d3a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6297445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bc282e148e29326c6ace847f1b2a59b1f8699a9c8aa2665d5a63e87e42e3e9`

```dockerfile
```

-	Layers:
	-	`sha256:bd9d6f1847d40bf88f12dd3ed1c306f53c94aeb0958463b1a3f566856ab6a734`  
		Last Modified: Fri, 05 Sep 2025 23:15:16 GMT  
		Size: 6.2 MB (6243258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de36601a0f330194ee57e5022cc03a37473cf1432f09c3c586ea4124462119e`  
		Last Modified: Fri, 05 Sep 2025 23:15:17 GMT  
		Size: 54.2 KB (54187 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18rc1-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:223680ca7f7731a12bdc0bb8839283f1587898249fe1eb5f4904b48bd49b10a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166608514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c270c6bfba7c46956de54189f8371555007a2d3529ac665c58be1438ad8c7e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV GOSU_VERSION=1.17
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV LANG=en_US.utf8
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_MAJOR=18
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PG_VERSION=18~rc1-1.pgdg12+1
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
VOLUME [/var/lib/postgresql]
# Fri, 05 Sep 2025 00:02:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 05 Sep 2025 00:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 05 Sep 2025 00:02:55 GMT
STOPSIGNAL SIGINT
# Fri, 05 Sep 2025 00:02:55 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 05 Sep 2025 00:02:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa6ce8adffa1425479d7a72f9cf11bf190eeee46b57d96d4b015386aab9abca`  
		Last Modified: Fri, 05 Sep 2025 22:34:58 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a267ea6dda9f0972c683227e3ae037cd8dbc3fc312db3f658fafc8b836f133`  
		Last Modified: Fri, 05 Sep 2025 22:34:59 GMT  
		Size: 4.4 MB (4391086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38533847c890318e4bdc36a88859b10b00e96193fd9b0e03cd1513ff5acd1360`  
		Last Modified: Fri, 05 Sep 2025 22:34:59 GMT  
		Size: 1.4 MB (1412762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb3d4b40acd275aacbcf892721695d4c2d17719b6889e1f2ec48f2b124e80f5`  
		Last Modified: Fri, 05 Sep 2025 22:34:59 GMT  
		Size: 8.1 MB (8120471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c275411c33ec8bbf04f7d16164a69644f59ef82738597630441815ef079dc43`  
		Last Modified: Fri, 05 Sep 2025 22:34:59 GMT  
		Size: 1.1 MB (1096832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c076c971bc7b31e3062babc5d6e18482d073d563154aaf8d06717a633f60a4`  
		Last Modified: Fri, 05 Sep 2025 22:34:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2533d5febea8677b2b0b62a51928f0794126c5dbfb08f306afa9af77ee4b68de`  
		Last Modified: Fri, 05 Sep 2025 22:34:59 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0517dcd4dcd5f295f607d6ee7780651ec6fe7d32dda301cb09eb96ecce2665`  
		Last Modified: Fri, 05 Sep 2025 22:35:14 GMT  
		Size: 124.7 MB (124669587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af76c4970c5fbfabdfec2bb3bddd6f2f1a7adfe6332aa35f8852e7b6713e7e2c`  
		Last Modified: Fri, 05 Sep 2025 22:34:59 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fa262cd29dc1a65b9a97dc945c11a33dc00ec70246612e0f909ba26e5782c4`  
		Last Modified: Fri, 05 Sep 2025 22:34:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288950d3892fb31b6cbe3d2170587b18f89d4ac9d12560644a261643ab9cba7a`  
		Last Modified: Fri, 05 Sep 2025 22:34:58 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc7435ed4bed5651fb1303f55c7b0f7ca3e0b02427103f992c7766a98f6812d`  
		Last Modified: Fri, 05 Sep 2025 22:34:58 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a05d4da77c1e8a1e05c9ec51f5f645c34841c815450c1bbb74708adf626680`  
		Last Modified: Fri, 05 Sep 2025 22:34:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18rc1-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2cb250140e18b3a4e641a086e6176d1bc426cd4d412457e3797d877fe26493bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25477530ed62331508b4f1da5a26f1be148eba0b035faa837e5cc05035487645`

```dockerfile
```

-	Layers:
	-	`sha256:99f6cad187614d4ad6be78058648f739642ce560c34216c1275188b19314fce1`  
		Last Modified: Fri, 05 Sep 2025 23:15:24 GMT  
		Size: 6.3 MB (6250519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d373b99d9d8b126114054bb7e83a22960b3cd62322323b29c5dcdc85f987e75d`  
		Last Modified: Fri, 05 Sep 2025 23:15:25 GMT  
		Size: 54.1 KB (54138 bytes)  
		MIME: application/vnd.in-toto+json
