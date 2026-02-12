## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:b18b19787658bc797748110888d2f59afa319873fc0cdcd7805ae21631dd89e7
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

### `postgres:17-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:026fc7ff17784b439f37947d55fa9ca1ff505e0e93fd2d6b2f8875959b2c386b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156059413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b139cb5c885dc680ca2bb662d2b95bea512dea98ac8ba178cb3f05781fe5a972`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Thu, 12 Feb 2026 21:03:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:04:14 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:04:17 GMT
ENV PG_MAJOR=17
# Thu, 12 Feb 2026 21:04:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 12 Feb 2026 21:04:17 GMT
ENV PG_VERSION=17.8-1.pgdg12+1
# Thu, 12 Feb 2026 21:04:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:04:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:04:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:04:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:04:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:04:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:04:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:04:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:04:30 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:04:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:04:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4a0348ad2ec5ea06571cfc7134ae1aed6319cdb76ecc131872b8ed2a105520`  
		Last Modified: Thu, 12 Feb 2026 21:04:50 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6aac9d7476b54400e8b96cdeb340741bdab230052598f7b9ab26b8f49cd54c`  
		Last Modified: Thu, 12 Feb 2026 21:04:51 GMT  
		Size: 4.5 MB (4534287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a310896f84854a3b3c0d590084f78fda655f5be960f44b52b44e4bee12a1bd`  
		Last Modified: Thu, 12 Feb 2026 21:04:51 GMT  
		Size: 1.2 MB (1249543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bb4ce30ad3dbe30ef29fc34e80964bc998ee35767e5c048cc98e7e2063c6d3`  
		Last Modified: Thu, 12 Feb 2026 21:04:51 GMT  
		Size: 8.1 MB (8066472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b6f2223c4b872741747b67ec53291fefc3616472bdb57456f3690547747c06`  
		Last Modified: Thu, 12 Feb 2026 21:04:52 GMT  
		Size: 1.2 MB (1196441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da35c01411f0c1ec986b2dbee214f6e3c055adeb1ac2a3846aebaecb40a6c0e`  
		Last Modified: Thu, 12 Feb 2026 21:04:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6809e067bc1457bbebbb5f2e12e88976cde0b8f97cd7c714d2bc41acdf43a50`  
		Last Modified: Thu, 12 Feb 2026 21:04:52 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10643155f46305ff6e0d6ca0552fab98e1e0f2f9925d4b489cf687817f93dab3`  
		Last Modified: Thu, 12 Feb 2026 21:04:55 GMT  
		Size: 112.8 MB (112763136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ef49b2a615db694a3f2bf6b14f1424c6ea299dad307a0a343010ca4a91e47d`  
		Last Modified: Thu, 12 Feb 2026 21:04:53 GMT  
		Size: 10.3 KB (10299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d37472e7c3c6f84d2772810b67a1d8db6ac6784d9338118bc9a9454e96f319`  
		Last Modified: Thu, 12 Feb 2026 21:04:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2363af18250194a7e05ea493c0051ca3eb4f6e2bbd6af27e4abae6da2e9970`  
		Last Modified: Thu, 12 Feb 2026 21:04:54 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a14fbbe260a357c15864b585857d904570ae664a5f15e28c936ff2975fd5341`  
		Last Modified: Thu, 12 Feb 2026 21:04:54 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cced4a98c7e92fb825f48e89b55c90232a0aaa90d2e2f2fb56be9c9b5a0b7f5`  
		Last Modified: Thu, 12 Feb 2026 21:04:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1aefae27b81fb6cfd4b35ae5d62d0c08a1dc35e8f33fe1c9c811d47593c6a331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263e0d0a10572d8661d7735146869e66740abec27b60c040dcb864ea55f5559f`

```dockerfile
```

-	Layers:
	-	`sha256:e2468fdab732e20ee8133028f64b2f95a4ba8331c96fd31ea16b0368c99d59d1`  
		Last Modified: Thu, 12 Feb 2026 21:04:51 GMT  
		Size: 5.9 MB (5927466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d4486d6392efc800e360753d0e77c1db1b5820b365d7108791854f004adf45d`  
		Last Modified: Thu, 12 Feb 2026 21:04:50 GMT  
		Size: 53.3 KB (53290 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:5092a9b1f97ff253c98b858935a555ed20d4883a83058573e04f848599559939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149055224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56eaa17f4146ac78daee2dcf60f2b2dfc1ffcde18c9a0ef99f0aa2a3488c1c9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:54:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:54:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:54:51 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:54:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:54:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:54:58 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:55:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:55:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:55:04 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:55:04 GMT
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 02:55:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 02:55:04 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 03 Feb 2026 03:10:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:10:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:10:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:10:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:10:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:10:38 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:10:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:10:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:10:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:10:38 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:10:38 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:10:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6036aff531a372e1e9da48952322760c8c052f6735e66afd3251a32e5baace8d`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 25.8 MB (25757618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266fdd3c41f9d26de63497a3343eaf8d937908511f9f7ebd4a1f8dd8770a5d9a`  
		Last Modified: Tue, 03 Feb 2026 03:10:56 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ae2be26f04326be69da8e5f7012a9416bb0e7016a72048ff8775c216c94a4e`  
		Last Modified: Tue, 03 Feb 2026 03:10:57 GMT  
		Size: 4.2 MB (4151285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692cb1b7785160ead2484ee16148ce8535d352bc0ca4aec779b2ea59dd514eeb`  
		Last Modified: Tue, 03 Feb 2026 03:10:56 GMT  
		Size: 1.2 MB (1220276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d079543c57564820e836d1285fa325feea00475317fa4385f8521b1709cd6493`  
		Last Modified: Tue, 03 Feb 2026 03:10:57 GMT  
		Size: 8.1 MB (8066646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7b9ab0038910db23afa4c3469ef7fec0764dea340ad8bb3ffe34070690f05`  
		Last Modified: Tue, 03 Feb 2026 03:10:58 GMT  
		Size: 1.2 MB (1195084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fe5fa446764d798598d365297b97cf73f7a4913a50c837f076e732f4549b88`  
		Last Modified: Tue, 03 Feb 2026 03:10:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b384a2e98bf7b3287e52d77785119a55da745a82a4b077b2b40540c1ae46880`  
		Last Modified: Tue, 03 Feb 2026 03:10:58 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b4d78adbf54f347fcfb6df54c033388c98c7bedfc1986e3c8384a29e097da6`  
		Last Modified: Tue, 03 Feb 2026 03:11:00 GMT  
		Size: 108.6 MB (108643321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5599f731ae57b327f96424a32c0941a5e427230ec4342a3346b63cfe7f788407`  
		Last Modified: Tue, 03 Feb 2026 03:10:59 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26865a59c0eb49723fd2a2f97e26bf337c4084361ea7ee6a349d3dd46086c110`  
		Last Modified: Tue, 03 Feb 2026 03:10:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d307cabdca931d3bc132ca7a2f8872951cdcaba05819f0befd2c1feb14b842`  
		Last Modified: Tue, 03 Feb 2026 03:10:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efc54af307f1ec6998879770d70786dc964c4a615b5f7518e60d9d4addf4e58`  
		Last Modified: Tue, 03 Feb 2026 03:11:00 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ccce2224a8a04baac283ce9625e3c6bfee7808c901bbf1771dd8e8a55b7008`  
		Last Modified: Tue, 03 Feb 2026 03:11:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a455a167661b0aed4efcd70d427d93819a27ec59b66b3caf6dd8179c4d1cdfa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ebcb279699f8ac7ad4ddab8016f064ef4eea435c476ad121341380f88db3eb`

```dockerfile
```

-	Layers:
	-	`sha256:59848f5da8da7fe58de6505c7b5cdad3ec07772e44c9ba7d581fa0af2f3d0fe7`  
		Last Modified: Tue, 03 Feb 2026 03:10:57 GMT  
		Size: 5.9 MB (5945781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7998a88c1a5ace5348a9034fc6dbe15b7660f9edcdf7a697884c9924859ee225`  
		Last Modified: Tue, 03 Feb 2026 03:10:56 GMT  
		Size: 53.5 KB (53495 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:11b4e611689d239b9cf09c0aeb6f6ca0e2c8661ae010a54ffbc7dfba2623443b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144059335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2df71f1f4339f17befaea873f3f3f9339dd0bc42be7f0f243570713aa39f68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:11:09 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 03:11:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:11:23 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:11:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:11:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 03:11:29 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 03:11:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:11:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 03:11:33 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 03:11:33 GMT
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 03:11:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 03:11:33 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 03 Feb 2026 03:26:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:26:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:26:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:26:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:26:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:26:24 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:26:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:26:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:26:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:26:24 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:26:24 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:26:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca557f1c3df27b69d443f904253feb3dd25b32691e3188d9eaa942373831322`  
		Last Modified: Tue, 03 Feb 2026 03:26:42 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822715dd487c8c2b725318cb1ea88b3ed050a0a40c106a77447cd7da8b5fb15f`  
		Last Modified: Tue, 03 Feb 2026 03:26:42 GMT  
		Size: 3.7 MB (3742666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99d510ff7a8196f736c86323ae2bf137a618e6037f1dbf9e16ba9acbf0f8e5d`  
		Last Modified: Tue, 03 Feb 2026 03:26:42 GMT  
		Size: 1.2 MB (1216118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7760fa57deadda9ba8729114b6c661fc1ccbe73d0b6d812451f6f220b06f049`  
		Last Modified: Tue, 03 Feb 2026 03:26:42 GMT  
		Size: 8.1 MB (8066407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f852b1c1fdf4411144ba7f83b2aa9d31839dc68a1b8b8ca83a9da7b0ff4001`  
		Last Modified: Tue, 03 Feb 2026 03:26:43 GMT  
		Size: 1.1 MB (1067283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bab16672b64691ef2b98c2ce5dafb9868520b3a0632d220ba73d5ac9f2cb546`  
		Last Modified: Tue, 03 Feb 2026 03:26:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2862813049a983dfff0cacb2c99a12833b37fdd59b815ebd52fa7fe9399d10`  
		Last Modified: Tue, 03 Feb 2026 03:26:43 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98d3b565e4bcd456a881c1859ab8e1610e808912f6d35fde3adc726fdda8298`  
		Last Modified: Tue, 03 Feb 2026 03:26:46 GMT  
		Size: 106.0 MB (106011779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9363bbb20734a9dd13d924a395253d928f1295183e17a7308b69384430d61cf`  
		Last Modified: Tue, 03 Feb 2026 03:26:44 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1a04afc872e22b7ffa349e78f766a6b1fec88dd520ed87da7975505a8bd6e6`  
		Last Modified: Tue, 03 Feb 2026 03:26:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c4eaa5896e83888a6fe4a563ba2d74cbe6b3c9c423acf9a88972d03b3b8351`  
		Last Modified: Tue, 03 Feb 2026 03:26:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e6e6cc855f006e11e8b7debb2d9c8f3f5a28d706dbf0d947ac4ad149ec3ed9`  
		Last Modified: Tue, 03 Feb 2026 03:26:45 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601b4ce9529bc86220ff5940254840fbd43c405ce0ced8f1cafbb17c59d51d5f`  
		Last Modified: Tue, 03 Feb 2026 03:26:45 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:134d0f774ad18e46ace71917576c5a0ca90769e76aaf78e18f4d5fb2cfb5713a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc221c6dd0bb77b374cc0b19bb477315bc2eca82b9c491337a5bb0bdb17b617`

```dockerfile
```

-	Layers:
	-	`sha256:8492571071b30986ed30b0fd566fdb0d249e65f47763dcbd50b9c6625e3f77cf`  
		Last Modified: Tue, 03 Feb 2026 03:26:42 GMT  
		Size: 5.9 MB (5945036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6848148b39ad85641fb81d2ffea3eb20effd9cee06785a3961dc838551213c8e`  
		Last Modified: Tue, 03 Feb 2026 03:26:42 GMT  
		Size: 53.5 KB (53497 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:66ef4b9d556431f029c7e5a975b85d911e50884905515821f4f2c7687ad69657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154056079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce3cfcf7f8ca9e186982f3dc126a63c0a365fd69997b67150e52871ee22b0ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Thu, 12 Feb 2026 21:04:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:04:22 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PG_MAJOR=17
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PG_VERSION=17.8-1.pgdg12+1
# Thu, 12 Feb 2026 21:04:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:04:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:04:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:04:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:04:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:04:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:04:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:04:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:04:39 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:04:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:04:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6914720142f92895f9e5ae988b2691f901ed9fc7ebd135038cf634f71f6ba4`  
		Last Modified: Thu, 12 Feb 2026 21:04:58 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47617e2a8ab7ae59c0787b9915f57eaa7d70e6fbd51c87d1b73394791a42e45f`  
		Last Modified: Thu, 12 Feb 2026 21:04:58 GMT  
		Size: 4.5 MB (4519528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ac4c71e8668f875f840085f8f1ba5cd37be3294e17c0d9bc923af92994cab5`  
		Last Modified: Thu, 12 Feb 2026 21:04:58 GMT  
		Size: 1.2 MB (1203298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f622af2e214f4e1282d1c83722c17ad16a6d71130c1f149eb4c55f0d677ba820`  
		Last Modified: Thu, 12 Feb 2026 21:04:59 GMT  
		Size: 8.1 MB (8066481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8c795a3030b4e1818cc75611fbfc0cb1a194bf99b5abc02e395518393e63ff`  
		Last Modified: Thu, 12 Feb 2026 21:04:59 GMT  
		Size: 1.1 MB (1109001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac2aa55d9c41aad4e147f44ef6d7cfd2d5153f8c552892fd21d7c531aae00eb`  
		Last Modified: Thu, 12 Feb 2026 21:04:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141fffb8655e40be7794f0a8a0f4f00e8486b14dc0748a8d47affe1a9704b224`  
		Last Modified: Thu, 12 Feb 2026 21:04:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc70d0eee2aeeebd5a44e549dc04893d9a9704d788b3fc8a4288fd45910c672`  
		Last Modified: Thu, 12 Feb 2026 21:05:03 GMT  
		Size: 111.0 MB (111028906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df527ee656329486b14bbd52e01f33e83e40fca7769dfc6d14050c657c4afc58`  
		Last Modified: Thu, 12 Feb 2026 21:05:01 GMT  
		Size: 10.3 KB (10295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d87a80a66eab14dea7b50b04774dcfd1a517e4c97954c2f944c2d66c3bf6b`  
		Last Modified: Thu, 12 Feb 2026 21:05:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc96fbe9ee9e4f2923dae284c6ed67c607afcfbab383dfbc692221b07ebc702`  
		Last Modified: Thu, 12 Feb 2026 21:05:01 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2e51011ee75b10043a63a74f00550ebbb473752f4e9c731f9b8c71a22a1554`  
		Last Modified: Thu, 12 Feb 2026 21:05:02 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69527ffd6f491430e97abbd45bf32558e85814d674f56bc4e78fb03b1bba707b`  
		Last Modified: Thu, 12 Feb 2026 21:05:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:faa5b8f17f9f8133b9bdc85830c91e3c5039d841019ce3528cebfadc5ba635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5987312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a343de87132a77b62dbfc3b4200a49ba64a2970585c7b5384d4a0e260cb64f68`

```dockerfile
```

-	Layers:
	-	`sha256:7747ab01f8a009426031dc4a4c7bcba7d3d5bbfe4641d8388687da3ebeab269f`  
		Last Modified: Thu, 12 Feb 2026 21:04:58 GMT  
		Size: 5.9 MB (5933777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eb40be8e86a42075b9815c8af845aa88e3cec50e7876eb508b6646044118894`  
		Last Modified: Thu, 12 Feb 2026 21:04:58 GMT  
		Size: 53.5 KB (53535 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:e33031b196a8b1b507ea2adf8e1da2ce54b826d687ed6c23ee2e1fbc37859263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164890696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc6d9268f742797803ea6fff59e28cc26d6a14cb0a19e3da9383d718bab947`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:37:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:37:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:37:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:37:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:37:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:37:37 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:37:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:37:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:37:41 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:37:41 GMT
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 02:37:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 02:37:41 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 03 Feb 2026 02:49:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 02:49:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 02:49:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 02:49:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 02:49:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 02:49:30 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 02:49:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 02:49:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:30 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 02:49:30 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 02:49:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f93d228262ac8f12d9af5f87a89d9722b3f4d559df30edfa91327db9f457723`  
		Last Modified: Tue, 03 Feb 2026 01:13:52 GMT  
		Size: 29.2 MB (29210015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba67afd3900d88f6ee3ed496332143e258c5a698b2df21c5103204578b3a16f`  
		Last Modified: Tue, 03 Feb 2026 02:49:50 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f21f3d1e547e3aee5321da3088673e4801648dbed4443b776aa9efeb0ed1b6`  
		Last Modified: Tue, 03 Feb 2026 02:49:51 GMT  
		Size: 5.0 MB (4966150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c478104b500b4ee37f61f9ecf5e93bfc5625834f82cda97556d92bf0f05bbe38`  
		Last Modified: Tue, 03 Feb 2026 02:49:51 GMT  
		Size: 1.2 MB (1218684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fff43c9134b424cb96e23c7c0d0fb8f5e84f35eb6d8f1ac40f7d08c6ac18aa5`  
		Last Modified: Tue, 03 Feb 2026 02:49:51 GMT  
		Size: 8.1 MB (8066472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a3a38c7e79d41fbec97b12167d3e2dcc65657daa0fb260913bda97ab3c5a42`  
		Last Modified: Tue, 03 Feb 2026 02:49:51 GMT  
		Size: 1.1 MB (1137486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811a7099ae936b7b753cae64e9a3a690d67fdaade6f8a6561d78db3b6cf1bb5d`  
		Last Modified: Tue, 03 Feb 2026 02:49:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7d8c914bd8620bb562e15547b6164b986f3d874f0b53c58d663d512b171bcd`  
		Last Modified: Tue, 03 Feb 2026 02:49:52 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e93fd0373a019a19c321bdc81bb05d58576ce99cdb4fbb81a2f4445904d4b7`  
		Last Modified: Tue, 03 Feb 2026 02:49:55 GMT  
		Size: 120.3 MB (120270892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21abbc71a5195d8df4a0d0919e4e5346fe1b377a01c54e7f0b6727883078478`  
		Last Modified: Tue, 03 Feb 2026 02:49:53 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379612142bb672e005836cb475d352e93d0f6428054e00decfd47d513143a41a`  
		Last Modified: Tue, 03 Feb 2026 02:49:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2854ac4d6c560272fd3e00d71cf8838b60848b6e3624b276c5b955e2bbc9fb62`  
		Last Modified: Tue, 03 Feb 2026 02:49:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37f071a417b235eb2c8b97b583f52d0c02d2c228b48ce2af1478d6d751d4b93`  
		Last Modified: Tue, 03 Feb 2026 02:49:54 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c222b05faa66f937cd5f498c33e2e0430ac63701732b6d72766223d4a52d6c60`  
		Last Modified: Tue, 03 Feb 2026 02:49:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e31c200cecc98f0e2e6e350def7a72f6c3ed515751cc45396612ce1c951d59c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5997170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73feb99ea31a574c09442a408b71e7289a84aac11be09abe2aef751cbc202a6f`

```dockerfile
```

-	Layers:
	-	`sha256:6f43b333c9aa3a2e5c7cd6f47e11b40616ef92eed8c0df40870342151157e5f6`  
		Last Modified: Tue, 03 Feb 2026 02:49:51 GMT  
		Size: 5.9 MB (5943924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1267385610d8e6d845b09870c1e5144ab6f93af63631c4296a2cc0d8f65191d`  
		Last Modified: Tue, 03 Feb 2026 02:49:50 GMT  
		Size: 53.2 KB (53246 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:21af9de0c799c60d19be3ae1750bb76d152489f0c68dc7b3f81e31a3563a795c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154896781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2646210a0b1ffd3202eb7f66846818cbc3467863255720c0e85c4dcf2c5ea79b`
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
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 09:36:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 09:36:59 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 03 Feb 2026 11:59:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 12:00:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 12:00:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 12:00:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 12:00:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 12:00:03 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 12:00:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 12:00:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 12:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 12:00:06 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 12:00:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 12:00:06 GMT
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
	-	`sha256:91dc2d9c133ac88eb8ce803bc58ccfaff499c7f7491fd7c1989e3dbfbe4d61b3`  
		Last Modified: Tue, 03 Feb 2026 12:02:18 GMT  
		Size: 111.5 MB (111478033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666df6094cf06d8d9eb15d7cfae7917d62994cf8514751685bd7d0d7215a9006`  
		Last Modified: Tue, 03 Feb 2026 12:02:07 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb51272737784b8a7e59af86b883697e5ad2d0c8a4d61a3ba8d2d6042b310e4c`  
		Last Modified: Tue, 03 Feb 2026 12:02:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95140d510b684c95f9e2055a04a47c9e064b5b31641c27e76517d6bb9b5ac241`  
		Last Modified: Tue, 03 Feb 2026 12:02:07 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0bb991f0eff3687e36b284a6ace7981ed238b70fb864fd8f621952f378c2d1`  
		Last Modified: Tue, 03 Feb 2026 12:02:08 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56d57b9f19dd160f09271412bbea2ffb86a87ef2c79eba1ae1294bb094cda0`  
		Last Modified: Tue, 03 Feb 2026 12:02:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:edc5e4545311eeab8f1c28e9106d4df902f5fd46eb5e9da6530a60d6b159fe7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416655862cfb22854303a5a57de04b7afd176e8bfab53391fcd23db82ecbd522`

```dockerfile
```

-	Layers:
	-	`sha256:7e352d4a8a316b70c8230a674c6869d174dfca5acb3595049a86549e68f27dd7`  
		Last Modified: Tue, 03 Feb 2026 12:02:06 GMT  
		Size: 53.2 KB (53156 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:3ba6aa7aa67bee6f4f46db16f0f50761f768021e3a7c129eb666d826f74f7b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168835417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fe767e0e5f380c35be2ece6e486ba332c92b342b35e2464aab0465faab5682`
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
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 05:03:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 05:03:14 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 03 Feb 2026 05:05:36 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 05:05:36 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 05:05:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 05:05:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 05:05:37 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 05:05:37 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 05:05:38 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:05:38 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 05:05:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:05:38 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 05:05:38 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 05:05:38 GMT
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
	-	`sha256:14f6ade08ea503a76d0c0e0644034795bc105233a8e5f0828ab9693916c2fc10`  
		Last Modified: Tue, 03 Feb 2026 05:06:29 GMT  
		Size: 120.8 MB (120818852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03c0567617b94497423724864c93a48604eebf5665ce5947ecc92d7031fbb53`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90332b7e4521b816150caba60eb8207fdcdc72a686d5f3ee099a1d8caaeff724`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db274d8213a62e7a0f2988b7e64c70e1352599118ad999211c6fc0774473c20`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e849e7d3ce406ca3779b2760dbd8ae204712d163403b8679e9cb9154e6dc28d`  
		Last Modified: Tue, 03 Feb 2026 05:06:27 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4afcd3e53e0c54d9f08ce0af58e519c4ad853d2eedd143d0d23846716cf2a21`  
		Last Modified: Tue, 03 Feb 2026 05:06:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d640903e82cbc5022761a997376fa993cb268a6f402609fae8d632ba9a58caef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8e01dea176a6fd5f17e177fc04909b277fe8e176d1439e8cdff981eeeb566b`

```dockerfile
```

-	Layers:
	-	`sha256:f683b5dfa96b487cd51b9810506eb564470eee770571c37756d474ab1a72e6ec`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 5.9 MB (5934827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6f4c838d0c08724d0132ffa98ed1f1f4ee38f46b3aa67ff3dab2aa8cb734f7c`  
		Last Modified: Tue, 03 Feb 2026 05:06:26 GMT  
		Size: 53.3 KB (53344 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:f9cc71ee3cc8ab6d6d6df0cc453ea4dd34014e025844d8278fce8b7b4fa79a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165303806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aafdc4412577b2b2650e7824f63cd45f86f2a34af1b757644745418c52c623`
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
ENV PG_MAJOR=17
# Tue, 03 Feb 2026 03:11:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 03 Feb 2026 03:11:54 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 03 Feb 2026 03:24:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:24:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:24:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:24:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:24:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:24:07 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:24:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:24:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:24:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:24:07 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:24:07 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:24:07 GMT
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
	-	`sha256:10b8da719f78824d1c9cbc65c14e1e2682e1064a111681f99af23e928e5b8eaf`  
		Last Modified: Tue, 03 Feb 2026 03:24:40 GMT  
		Size: 123.6 MB (123566516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c088d466af3dcdcdbe8e012c2264fb8b16fa511d933728b82dc4708ca228e476`  
		Last Modified: Tue, 03 Feb 2026 03:24:38 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cf680fcd1ad3f2d0d80956724c882184c48f877177b4e4c3b4e466b02ea2bd`  
		Last Modified: Tue, 03 Feb 2026 03:24:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60afce1f4f3c0f5f5b40a53f0983a49a8a5b5fd7d51c63353074d21356e1d7f7`  
		Last Modified: Tue, 03 Feb 2026 03:24:38 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb25c307b4566a5c86ce3796e9f4b15e7044bdea7a4c7737a32809424adf2ae2`  
		Last Modified: Tue, 03 Feb 2026 03:24:39 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2de97c312b9c54f61957e878b2925989c1dcbe45d9194d22732e6a7398c36b5`  
		Last Modified: Tue, 03 Feb 2026 03:24:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:bb2759da5abcb6de88259f40dd191ae04c9233fe7bc4ed245b42637958bf8935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5993690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50cb16b456ec5868c4f7a97491eddc15611f744de31f59aa498c59fd0780b65`

```dockerfile
```

-	Layers:
	-	`sha256:9a13f6c4d302d1f5dc885a1f91c8bd9cb6a3692029538b72db369669195db0e1`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 5.9 MB (5940400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c2e5715c0ee372a4ae1b0273d26afee486963c93119e7c8f8e475c2cbbf608`  
		Last Modified: Tue, 03 Feb 2026 03:24:36 GMT  
		Size: 53.3 KB (53290 bytes)  
		MIME: application/vnd.in-toto+json
