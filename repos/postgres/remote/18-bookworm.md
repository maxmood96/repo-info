## `postgres:18-bookworm`

```console
$ docker pull postgres@sha256:1db8756002899f8177e8c7681365d0127e3005b5e6287d98f074cb76743982a0
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

### `postgres:18-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:b0acb40ffc0bcc654fd0562860032ae0e3cd102136f1c92cad4bef16528d3b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157120456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccd935443356b33d3f033920657c4e1c43362266fcadb4f9f6db109913a310c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 12 Feb 2026 21:03:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:03:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:06 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:04:11 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:04:14 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:04:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 12 Feb 2026 21:04:14 GMT
ENV PG_VERSION=18.2-1.pgdg12+1
# Thu, 12 Feb 2026 21:04:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:04:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:04:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:29 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:04:29 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:04:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:04:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:04:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:04:29 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:04:29 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:04:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cf9c3371344e1e0395a76699ab3b04af0fe9bbc6fa282ae056f5ab48a719cf`  
		Last Modified: Thu, 12 Feb 2026 21:04:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c69dc9b1ea40eadd810b1412359d877380fbe237fda44f72e5e6312e5f4242`  
		Last Modified: Thu, 12 Feb 2026 21:04:49 GMT  
		Size: 4.5 MB (4534229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189de19d0fe1cba7d7b6050a8580850d1d65f96120dd08f1026f3db534f5f8e7`  
		Last Modified: Thu, 12 Feb 2026 21:04:49 GMT  
		Size: 1.2 MB (1249518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f93b164ebb20c6febae7a04dfc7debaf2b7f1660ece7c99a05ecb3ba2aacde`  
		Last Modified: Thu, 12 Feb 2026 21:04:49 GMT  
		Size: 8.1 MB (8066540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1177c08706862c6090d320890326e05ae325fb98a8d877aa3162c8347ebba4c5`  
		Last Modified: Thu, 12 Feb 2026 21:04:50 GMT  
		Size: 1.2 MB (1196388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb078e1d0502166976f546f052f1eb5bee3c44337a696f149fc4b99f4e56a5b`  
		Last Modified: Thu, 12 Feb 2026 21:04:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c588029bee201450134359471efd6a5dafd02d2cb32c288e6ec325bd0e15d7a`  
		Last Modified: Thu, 12 Feb 2026 21:04:51 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1e8326916973c0d79ebf733cfbd84d027473fea45e74b9761cf895810c124c`  
		Last Modified: Thu, 12 Feb 2026 21:04:57 GMT  
		Size: 113.8 MB (113815478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0face4f668d4c6d24b22ffa2b965df9cadcfe667539ddf6ce24ee6957d2de769`  
		Last Modified: Thu, 12 Feb 2026 21:04:52 GMT  
		Size: 19.2 KB (19233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b297da5a68c3388d5561d53946b04cf105abfc2145bbf85409c0d7208532e7b5`  
		Last Modified: Thu, 12 Feb 2026 21:04:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcaeeff9060d19f1b7db0b56f9a833a69ca1b3996ddd36fca200f3fd5785345`  
		Last Modified: Thu, 12 Feb 2026 21:04:53 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb28d43cb42ba76b1556659e905ddf7597f30ebe17b28f8b0207927272860d34`  
		Last Modified: Thu, 12 Feb 2026 21:04:54 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f3c5cd5e755eb0da63934bb3499e3250ef117dc84d21d2e39c03c44da8c3fcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a1deec0f1edc94d5302d7407cd8e91b85a95d1ef8b7b57117c475e1a8df747`

```dockerfile
```

-	Layers:
	-	`sha256:74068e5662ed6c7303cfa2ba76c8fb7b844a3093260fbb76826b4c16ca9164f2`  
		Last Modified: Thu, 12 Feb 2026 21:04:50 GMT  
		Size: 6.2 MB (6156497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd09a05ad1a9256839f8bce43943efd563b59cce8ef3facf303b613a00faa0d0`  
		Last Modified: Thu, 12 Feb 2026 21:04:49 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:e0f9f04bccafe96bc817887f422be5b5e6a0f74add67391c030441dc58ce4729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87155277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2544d38923d272f16019632aa3bf5d2d60e787ede9024c1ec23cd4754c9716a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:53:14 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:53:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:53:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:53:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:53:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:53:39 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:53:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:53:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:53:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:53:45 GMT
ENV PG_MAJOR=18
# Tue, 03 Feb 2026 02:53:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 03 Feb 2026 02:53:45 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 03 Feb 2026 03:05:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:05:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:05:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:05:48 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 03 Feb 2026 03:05:48 GMT
VOLUME [/var/lib/postgresql]
# Tue, 03 Feb 2026 03:05:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:05:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:05:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:05:48 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:05:48 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:05:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6036aff531a372e1e9da48952322760c8c052f6735e66afd3251a32e5baace8d`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 25.8 MB (25757618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b55adc0101ea0ec826e3c064e0c7c4f52bef3685e3a31382a229cb20780ec65`  
		Last Modified: Tue, 03 Feb 2026 03:06:01 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9bed1101c3f4a3cef30fe9e9ef263c71dec54189c81f13f8f32e84338a4be8`  
		Last Modified: Tue, 03 Feb 2026 03:06:02 GMT  
		Size: 4.2 MB (4151296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98fcb85f0c729d8eef0007a85cf7bfcebbb665484bba8410a3443ff0437042d`  
		Last Modified: Tue, 03 Feb 2026 03:06:01 GMT  
		Size: 1.2 MB (1220288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd41884fbc1260dec0bf4628fc4e3f94f93726a7ae3821d4a8638cc601289c07`  
		Last Modified: Tue, 03 Feb 2026 03:06:02 GMT  
		Size: 8.1 MB (8066630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccb310af36347a15a6fa7dc2a18956fa2e94c48ba845fc6e07f34134a0f364b`  
		Last Modified: Tue, 03 Feb 2026 03:06:03 GMT  
		Size: 1.2 MB (1195065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018508c63c3541c40110608f1718d8dc8d7999f7dffb4a5c3746841af38333e2`  
		Last Modified: Tue, 03 Feb 2026 03:06:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1d5d3196524f2b023fd10856a8416e32dce3c058b3bfc880835664caa26c1a`  
		Last Modified: Tue, 03 Feb 2026 03:06:03 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb10e0f7d5c384baf1136688a41a85b781077df23c6e574bb57bb648b8465f8`  
		Last Modified: Tue, 03 Feb 2026 03:06:04 GMT  
		Size: 46.7 MB (46734702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828e51d0346190ed46a983a8c3d885c83937c1597a9e5d8844e0e22bd7b46923`  
		Last Modified: Tue, 03 Feb 2026 03:06:04 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283b9b60e0360696de578ac7cc2a864b8e150a9d15e25da117745dbbb4b7fc6d`  
		Last Modified: Tue, 03 Feb 2026 03:06:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8892b09069701ffdba79b9d218de5c06731bd5673dfa611a7a3f5503f3de8f16`  
		Last Modified: Tue, 03 Feb 2026 03:06:04 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6174293a1c473bcb4a053d761565eefde4289125f69f15dbb0d21ba79362f1d`  
		Last Modified: Tue, 03 Feb 2026 03:06:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:48ef6855636c25156cfe0753085545452c1179539b11b09d0d19494c42f77f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec0ce61da8d30f51a511241fbb2879eaddfa2fa6f83b5b82f20eb845f80159a`

```dockerfile
```

-	Layers:
	-	`sha256:5abc4262457377c860d6d2b5da7f1b365ce0b2c8c6a0cb50e87b36dbe0b5677c`  
		Last Modified: Tue, 03 Feb 2026 03:06:02 GMT  
		Size: 5.3 MB (5317016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8db4400a879c7398270d421bd84626e593734af0b5dc424b00591647ff2523e8`  
		Last Modified: Tue, 03 Feb 2026 03:06:01 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:73be5a395acc3cc433d366c32f57f0efb8b518916b1a1ee26dfc0fa3ae28be55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83278070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a03af828733d3b36931f0b33a1f382cbe1c0fe4e4b52a18124ff3243e759b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:59:42 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:59:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:59:55 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:59:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:00:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 03:00:01 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 03:00:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:00:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 03:00:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 03:00:06 GMT
ENV PG_MAJOR=18
# Tue, 03 Feb 2026 03:00:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 03 Feb 2026 03:00:06 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 03 Feb 2026 03:11:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:11:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:11:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:11:31 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 03 Feb 2026 03:11:31 GMT
VOLUME [/var/lib/postgresql]
# Tue, 03 Feb 2026 03:11:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:11:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:11:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:11:31 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:11:31 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:11:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6053ef550138764fcd251dba34323d756ff0cd902105b166bd72afab046d97`  
		Last Modified: Tue, 03 Feb 2026 03:11:43 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414e352f44ebe5b9801696878ae59bfcf9c7d174246dc28e158d562b5f5a7b2b`  
		Last Modified: Tue, 03 Feb 2026 03:11:44 GMT  
		Size: 3.7 MB (3742679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fec06f941a537a4bde3b97086596ae80c96c8f5150f7e921be205b6f9b0551d`  
		Last Modified: Tue, 03 Feb 2026 03:11:44 GMT  
		Size: 1.2 MB (1216107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daff9a9e211dbef7fd5ec0f9689fffcad014a0e74edbf11eda9bfdcf7bd69db4`  
		Last Modified: Tue, 03 Feb 2026 03:11:44 GMT  
		Size: 8.1 MB (8066420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c892755a3da257b3213c8ee4a832685f8ba9a45ae1ad7242684539896701e76`  
		Last Modified: Tue, 03 Feb 2026 03:11:45 GMT  
		Size: 1.1 MB (1067283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605d251fbe8d5f4a86586b5454dcbf9da1bebc40a84c3c925f131822cff02fdc`  
		Last Modified: Tue, 03 Feb 2026 03:11:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908ec7cd1eeb2f0fca542f0e76aa7b79de8ede56e5cfa6f56353accd75f7496`  
		Last Modified: Tue, 03 Feb 2026 03:11:45 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c84e5a5fe2a6f831da8ed55ea34e410ec5eeca16d0ee4d2b0c022eaa463607`  
		Last Modified: Tue, 03 Feb 2026 03:11:46 GMT  
		Size: 45.2 MB (45221809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc24896603599b8a4396d4721d6892a7fa6030cfc46cc45356429945a04439d`  
		Last Modified: Tue, 03 Feb 2026 03:11:46 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d8149b5b64dd04b8b0784b24fe91aed7099e75b0fe4de43f98928ca7ca07ee`  
		Last Modified: Tue, 03 Feb 2026 03:11:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92620b12d4f5d1be196f9ef765bb626013de591dc6eee1b7ca9bb4930692e38`  
		Last Modified: Tue, 03 Feb 2026 03:11:46 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d4b9ff761b7b9dc599d033ceff6449c80759214bdaad212fb941c06bc5524a`  
		Last Modified: Tue, 03 Feb 2026 03:11:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:df814a8b7ca47277f44787a1af1da00d6990c09ad54f2173dd7ca2733c4c4410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5f01b4d557e1848c757145395fd99a20d18498fb4ee4d80dc3983c14577e2b`

```dockerfile
```

-	Layers:
	-	`sha256:3318a1aabbcec87ef17cbb150e03c19fd9435d37d1c9ab23a4c41d8eb09dfe69`  
		Last Modified: Tue, 03 Feb 2026 03:11:44 GMT  
		Size: 5.3 MB (5316267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b0b7dbd4c0d48b3dbfdf721b9170d251b45d80e3876372b05df7fd4c7073674`  
		Last Modified: Tue, 03 Feb 2026 03:11:43 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c2d8cf6e12ab0bb0de68647085221b73d1d1dfcb7d0e064a74325b73c2b17de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155110095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5678d58e1f4ad196f6923ef85d63b00e375a6ca1d8bcac3178f8820bf76f38a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 12 Feb 2026 21:03:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:03:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:55 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:03:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:03:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:03:59 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:04:03 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:04:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 12 Feb 2026 21:04:03 GMT
ENV PG_VERSION=18.2-1.pgdg12+1
# Thu, 12 Feb 2026 21:04:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:04:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:04:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:20 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:04:20 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:04:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:04:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:04:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:04:20 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:04:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:04:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48d472067fdb590959be0f6c194ccaf53963695492b961e37c13e67e7bdf286`  
		Last Modified: Thu, 12 Feb 2026 21:04:40 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e1a62feae802ef700880a6e8fdeca3d732664c0c914301c7499d914505e60`  
		Last Modified: Thu, 12 Feb 2026 21:04:40 GMT  
		Size: 4.5 MB (4519480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3815a2b9bba7f450207026a607663df18e803a4cde1064cbed8b080e6fdca0ee`  
		Last Modified: Thu, 12 Feb 2026 21:04:40 GMT  
		Size: 1.2 MB (1203287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577bf4838070ac51fa91bf38874c8b91af6ca9198cbfce6aaeb8973ae74937bf`  
		Last Modified: Thu, 12 Feb 2026 21:04:40 GMT  
		Size: 8.1 MB (8066482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98985544708605f42c0f8106629d3b60fbeba18bb3d01cb0800bfe9341bc904c`  
		Last Modified: Thu, 12 Feb 2026 21:04:41 GMT  
		Size: 1.1 MB (1109006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6855c2ce828e5f8340d025dd2b2a86fb85a3d52e7c2a693975c1890717b9dfd`  
		Last Modified: Thu, 12 Feb 2026 21:04:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dce4fed40f408f71e40c3e0933aa7185c421b4c57b9056784db1504657a30ee`  
		Last Modified: Thu, 12 Feb 2026 21:04:42 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862a67c2cc14ee5d976543340f20e0d34ff75889c7150e5c8597971553d70368`  
		Last Modified: Thu, 12 Feb 2026 21:04:44 GMT  
		Size: 112.1 MB (112074203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc61a59ac6d37cd444b19f5026dbf976a80a1dac7ddee726c7b833f21a0948ec`  
		Last Modified: Thu, 12 Feb 2026 21:04:42 GMT  
		Size: 19.2 KB (19231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12118820e2a25970031a2dd38c06c08002cc9e500d46924bae49e99ea8bf6cc3`  
		Last Modified: Thu, 12 Feb 2026 21:04:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c5590d99a3fe221df39ecf8ebe0a76e4ad781d49efdbda794ea7e3c3f90541`  
		Last Modified: Thu, 12 Feb 2026 21:04:43 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3695d8fba79b4ef786a0d4a95cc646ec57d956f9b3d0da849733a55a2154be6a`  
		Last Modified: Thu, 12 Feb 2026 21:04:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b4b5f08a63d19f59fc2bcf7482ce6e58f5b5983daf2cbced60200696438ada68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516458d04d1df17bc996c537657291cb08ce89fb1c0368a5712915809e8ac637`

```dockerfile
```

-	Layers:
	-	`sha256:83457818d791c65db4186f596421495fba39c1de33340283a658014bee1095b0`  
		Last Modified: Thu, 12 Feb 2026 21:04:40 GMT  
		Size: 6.2 MB (6162822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0cf1cd67c588acdce7b91744dd1b39c467ab3980aa655dcf8ccac3dd40ee1cb`  
		Last Modified: Thu, 12 Feb 2026 21:04:40 GMT  
		Size: 51.8 KB (51832 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:8ae554233d9c030ff5febab73641d2a3e22ada8370d9d4dbe9b55072f9c3dd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93926565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1908c3653d24febf0ebc542222131cddaef4c11f354c2c38590fdb34bf5591c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:36:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:36:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:36:49 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:36:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:36:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:36:54 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:36:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:36:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:36:58 GMT
ENV PG_MAJOR=18
# Tue, 03 Feb 2026 02:36:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 03 Feb 2026 02:36:58 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 03 Feb 2026 02:45:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 02:45:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 02:45:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 02:45:35 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 03 Feb 2026 02:45:35 GMT
VOLUME [/var/lib/postgresql]
# Tue, 03 Feb 2026 02:45:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:45:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 02:45:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:45:35 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 02:45:35 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 02:45:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f93d228262ac8f12d9af5f87a89d9722b3f4d559df30edfa91327db9f457723`  
		Last Modified: Tue, 03 Feb 2026 01:13:52 GMT  
		Size: 29.2 MB (29210015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95332b59f6a2f7749ab825c45cfe3eff21edcdef510ebc159d8f946ece92d3b1`  
		Last Modified: Tue, 03 Feb 2026 02:45:47 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30c0e65cfcbc025cdec1613617b6fcbfdb3be4444ece78431d253bf38528825`  
		Last Modified: Tue, 03 Feb 2026 02:45:47 GMT  
		Size: 5.0 MB (4966114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de70f1b52605b260995f2285bf200045f3ee23e8e2382c0585237250319b97c`  
		Last Modified: Tue, 03 Feb 2026 02:45:47 GMT  
		Size: 1.2 MB (1218657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198532cd3a7f1d4d7db4bc5fc2179b117a6e2e1b189bd5d7e65f097bcd70ca80`  
		Last Modified: Tue, 03 Feb 2026 02:45:47 GMT  
		Size: 8.1 MB (8066438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2495ce6559388d7651a53ad91f1f00f4eebf7e9c04cda6e6b59e81dca40a04eb`  
		Last Modified: Tue, 03 Feb 2026 02:45:48 GMT  
		Size: 1.1 MB (1137476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca45c246fc2ba741b85299029e71bf886124e5a99cc5b1741c42fba2414b0a6c`  
		Last Modified: Tue, 03 Feb 2026 02:45:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d095c25477478a6b6ac5d4b07d7c34beca5fb6dc03bc14b62512cae0161aca87`  
		Last Modified: Tue, 03 Feb 2026 02:45:48 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581f6efb114465e41b233546cb03c0c3b4d0da0f57960eb8db65ba455542aed2`  
		Last Modified: Tue, 03 Feb 2026 02:45:50 GMT  
		Size: 49.3 MB (49298185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a9ba782578c4043e2af711be82fec672652246b30ca0beb60f71377353ee1c`  
		Last Modified: Tue, 03 Feb 2026 02:45:49 GMT  
		Size: 19.1 KB (19094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925b92b19af476a18226e2dda32b24740e5bf7da5c88735c1177d777af2e247e`  
		Last Modified: Tue, 03 Feb 2026 02:45:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97852984e13df7f096eba081f56cadac8ffa0f4b9ea148ccd3c8f0d2b163f29c`  
		Last Modified: Tue, 03 Feb 2026 02:45:49 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37bff4c6eac32fed2ac81b10a473df3d0cb5d0d90889de30af41a7db49718b4`  
		Last Modified: Tue, 03 Feb 2026 02:45:50 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2e8fac50870c14356a0ae92d01d19650f3a6d2d21b3d8817b15b6ca5ada43f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b78d8711aeb916bcf17e4d6887e0bbbd7984bba17794954f617b174d3951495`

```dockerfile
```

-	Layers:
	-	`sha256:631f7f3d9843bd804c0d4fed22d2916207eb279c7c813137bccbaa1e5d523467`  
		Last Modified: Tue, 03 Feb 2026 02:45:47 GMT  
		Size: 5.3 MB (5311582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:288cc3c6e52a6b2a27c7dbbcdd07acc809990f6ef46d26d1e18409c9b5d1c068`  
		Last Modified: Tue, 03 Feb 2026 02:45:47 GMT  
		Size: 51.5 KB (51538 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:bf63ad487e8e98190dd39815d778c338628b728dd86bf3294076846e41a210cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155916045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f01eba03f240a6bbb82b164873fcd7e46a3dd74a1cc39e1274a77474afee20`
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
ENV PG_MAJOR=18
# Tue, 03 Feb 2026 09:36:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 03 Feb 2026 09:36:59 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 03 Feb 2026 10:47:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 10:47:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 10:47:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 10:47:33 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 03 Feb 2026 10:47:33 GMT
VOLUME [/var/lib/postgresql]
# Tue, 03 Feb 2026 10:47:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 10:47:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 10:47:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 10:47:36 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 10:47:36 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 10:47:36 GMT
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
	-	`sha256:0cd15560e25c2135f58ddf8525044dedd3bc30f6cb7c0e370a0a1dd588572816`  
		Last Modified: Tue, 03 Feb 2026 10:49:51 GMT  
		Size: 112.5 MB (112488611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef902266c91726749ff9de21f22dff7c960db6ce0358af05c3338fcecbbd0922`  
		Last Modified: Tue, 03 Feb 2026 10:49:40 GMT  
		Size: 19.1 KB (19100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8e4818b40e9b862784cb4568f973235ab96f1a58b9b7fe4369f3067985d6aa`  
		Last Modified: Tue, 03 Feb 2026 10:49:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbb4f0e5ae80b5f645e238e7e6db2b108dfd24d38f1f34c42853ba188776296`  
		Last Modified: Tue, 03 Feb 2026 10:49:41 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acb7ff5f1f580553176d09596557a98efa9417d91a9d175b1f7c70afab71385`  
		Last Modified: Tue, 03 Feb 2026 10:49:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d36b28d94b39ba9c6a17f7ed244b3f669cd87b9bfded014a96114f8f483c54ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 KB (51462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95074216e7901cdf1594fc1e2ebc6ea5d90ef3253a9b9b2c89cc0728e67d0d01`

```dockerfile
```

-	Layers:
	-	`sha256:8c965dcace5d12dfc84690fb46a40ac1602473f561b35bd2b1c268ad54f06ed2`  
		Last Modified: Tue, 03 Feb 2026 10:49:37 GMT  
		Size: 51.5 KB (51462 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:406b20c8fecdd3f61e55144ca871c51d316bae86417c407cbe0d9e2f9b04a9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170018858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3946c9d011f08efc71be56c385bf6ad67107986b3468735e5403534b2706ba80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 12 Feb 2026 21:02:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:03:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:22 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:03:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:03:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:03:32 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:03:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:03:41 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:03:41 GMT
ENV PG_MAJOR=18
# Thu, 12 Feb 2026 21:03:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 12 Feb 2026 21:03:41 GMT
ENV PG_VERSION=18.2-1.pgdg12+1
# Thu, 12 Feb 2026 21:04:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:04:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:04:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:25 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 12 Feb 2026 21:04:25 GMT
VOLUME [/var/lib/postgresql]
# Thu, 12 Feb 2026 21:04:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:04:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:04:26 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:04:26 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:04:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dd2116d4f00610191cab66c1981409e66c43cfcea0b7afce48664af9ada05a`  
		Last Modified: Thu, 12 Feb 2026 21:05:15 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226c2595c6ea114ee68b859c18962a56d08e5f6e70ae6f5bd08239facffb7fa9`  
		Last Modified: Thu, 12 Feb 2026 21:05:15 GMT  
		Size: 5.4 MB (5368690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886ccdd2ea90a746506cfa6ead1d27db10a1112f83dead5a52ffbb1c4cc0ad41`  
		Last Modified: Thu, 12 Feb 2026 21:05:15 GMT  
		Size: 1.2 MB (1208197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1323557ba8f39ed8b2b81763264f19e77b228414e42ae186fcf8812cd38d9275`  
		Last Modified: Thu, 12 Feb 2026 21:05:16 GMT  
		Size: 8.1 MB (8066565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135b2f1d6394f7a7e9e8c5dfb2a2e5eb4cf84d2bb2de43a9864931bae945ec6a`  
		Last Modified: Thu, 12 Feb 2026 21:05:17 GMT  
		Size: 1.3 MB (1283681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6135a0f5b1ec1f61f7010e9788a4f47006e7692b1cf1ecf1c53e1edbe4a92def`  
		Last Modified: Thu, 12 Feb 2026 21:05:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2188dc6d4cff2ba3405546607dd32c67f155d8d9a47c83797dc3fa61b0196caf`  
		Last Modified: Thu, 12 Feb 2026 21:05:17 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c42e340d113b84278b0c4bae73fc830b12866bb6d988028b6cd27b3522a5437`  
		Last Modified: Thu, 12 Feb 2026 21:05:20 GMT  
		Size: 122.0 MB (121993200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0f8daae0851c056c3817a887636d450e275c714d62f0c0d2b6f7814dfbfcf5`  
		Last Modified: Thu, 12 Feb 2026 21:05:18 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde31daa905e202513b8f7e2a4bc1665d664972561ca81b46805b0c24e248e8`  
		Last Modified: Thu, 12 Feb 2026 21:05:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3740b367ddc5c42d77c654e1998eb6d7fd6e30a391c3b5fb964e2de05dfd32fb`  
		Last Modified: Thu, 12 Feb 2026 21:05:18 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6f2ff6dafb5d5e1a3e61a01943d56207a1db5baf476314fb3e874927687d63`  
		Last Modified: Thu, 12 Feb 2026 21:05:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ba9306f261e005919a990b001a337cb9c0b23b8b1567f2324c2e4593d1649a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb54750a9b1ac9187b592f8223805a9089749f418ba9b7960123079ef654e3b`

```dockerfile
```

-	Layers:
	-	`sha256:ffbfd2d6deacaf1ba5c96e18e8eb93804612473502d2054d7542b2c2f16a02d1`  
		Last Modified: Thu, 12 Feb 2026 21:05:16 GMT  
		Size: 6.2 MB (6163882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:197e5fb4a0d880dea23847cb95fc29f85dae2a94f187701b8748967ecf7993e3`  
		Last Modified: Thu, 12 Feb 2026 21:05:15 GMT  
		Size: 51.6 KB (51648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:a460c4e20d75867b6e8a7a7729bd78a3712878271368b043ea22d7dc3537ab81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166374608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83514ab19e9246c6b2427e0cfb336bd0ca8a8953ca850d905b869895d464ef78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:11:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 03:11:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:11:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:11:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:11:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 03:11:50 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 03:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:11:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 03:11:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 03:11:54 GMT
ENV PG_MAJOR=18
# Tue, 03 Feb 2026 03:11:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 03 Feb 2026 03:11:54 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Tue, 03 Feb 2026 03:24:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:24:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:24:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:24:08 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 03 Feb 2026 03:24:08 GMT
VOLUME [/var/lib/postgresql]
# Tue, 03 Feb 2026 03:24:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:24:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:24:08 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:24:08 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:24:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caf9cb5b61a1437581b2e50c491831571f8fa964c4171b93b62ec7a8fde03f9`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56af6bf01ae5568ebb854217eeb99b4207e6debd6e6ba219f3fa5a7d16d8b6da`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 4.4 MB (4391265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476771bcf8bb2eff664fe00274c169f6d81258e2721617ed1cf59b6c4b3742d`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 1.2 MB (1222843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89ac86c385fae930c5989986f8411eed309b6a43e5677bd86b6e218be30b54d`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 8.1 MB (8120737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fd342744957265a6381f30baeb36e88f5a2c01a146c7417ce2443ede1bd847`  
		Last Modified: Tue, 03 Feb 2026 03:24:37 GMT  
		Size: 1.1 MB (1097066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c4ec609b5abbeaeed48abea949af6f341a697e28259b9c60943b55f28501ff`  
		Last Modified: Tue, 03 Feb 2026 03:24:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c44c919787d9aeb83f1ef71fda2a2556a3c8e651ab83b73f41f0fd2f051219`  
		Last Modified: Tue, 03 Feb 2026 03:24:37 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d88c5d636ebaa4fc7b126e09af749b4520c0c3b28a5e99d67e5fc59d5b1b07`  
		Last Modified: Tue, 03 Feb 2026 03:24:41 GMT  
		Size: 124.6 MB (124628638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c38af816829c40d2e50f9fe044f5a30bf83ce558a0e1cee336d5d2f40bc867`  
		Last Modified: Tue, 03 Feb 2026 03:24:39 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1149aa942f7ceef5db386f98ce7f749dcdfca9b7f5831c4bbbbe35a70c92eb77`  
		Last Modified: Tue, 03 Feb 2026 03:24:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc664d058de6860605b8362282d5b5de7d4b6cbeb2a574b9879e647dc64a1a2c`  
		Last Modified: Tue, 03 Feb 2026 03:24:39 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4033ca2f2d397ff40ba174c1aa0d6c882166f5b895f97f6a878a09c4424d870`  
		Last Modified: Tue, 03 Feb 2026 03:24:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3c5a69d61c1acd80c5c17597aba0e2cad376a3ab3a4487b7258f42f48cf8927c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7b10547e4991dd75157a612a06456a1dfe45dbd27f818a46faa428122a162b`

```dockerfile
```

-	Layers:
	-	`sha256:338dd2d8cdb285833f76182b2f43d9fba2e87fee685e6c53d030483cc397236b`  
		Last Modified: Tue, 03 Feb 2026 03:24:39 GMT  
		Size: 6.2 MB (6171155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3defad3bdf60f731ab33f2ccb1e8204cf2f3745d88b169fc1e620298951903bb`  
		Last Modified: Tue, 03 Feb 2026 03:24:39 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json
