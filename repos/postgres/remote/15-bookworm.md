## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:db7d0bc4c3d07c600d48abebbba2dfe587212727ee01bd7d2118a6cab72a8f70
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

### `postgres:15-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:6a651bc46a96bd9466e6fc10182a1edfbda61b48e26258bef94bf3efc55768e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151267857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8056eb3aa10520a3f2fc359f770e38ca902462263e1d4d1f9415911f28d9c640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=15
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f414cc63209809ee122ffe50c1d70b47b3d8bdf5a94f06f8c08b3a6360228e`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d525e3e821df6104e16bb49600f76cd3b5d00db52448c0fae78af9dcbbb2a17`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 4.5 MB (4533488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f5a1ca5cc710c2ae0cd1ab981469117a64ea9dd26a51be8aab0a5a7e899681`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 1.4 MB (1446679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fd5918b0ae78b19ec008d1b5372c49ca8abb8ca8af627777f44d09a1f05dcb`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 8.1 MB (8066199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45a1a3e63ad9922c49da6ec3ccf11924fa2de9e39a04d6e24062b8a1e9e6979`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 1.2 MB (1196049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e824c09e869012375198e4625330fd7a948762d1b6965c60d9d9e030307ddd4a`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6efafa9ff610618d43e9fb5ce6f5ca668698036673515acb94afc91c1281ea9`  
		Last Modified: Wed, 10 Apr 2024 02:55:59 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e723a6ea1ef5618b7f65aa7fe8fa9a459e8c4dd08a87fcca7fff6f5f23a37c48`  
		Last Modified: Wed, 10 Apr 2024 02:56:00 GMT  
		Size: 106.9 MB (106873980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58aed2eceb710f4183cf327c08c453e0745187502818891c1ce68e4f7d889ce`  
		Last Modified: Wed, 10 Apr 2024 02:55:59 GMT  
		Size: 9.8 KB (9778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a7c0a3507740ef8d4614400d6ec00834073f6b8f939d3d1eddc60714b49cec`  
		Last Modified: Wed, 10 Apr 2024 02:55:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61a2dcedb7974fa5f9891a37358a9de72799f24bc309fefc593df8b00452f0e`  
		Last Modified: Wed, 10 Apr 2024 02:55:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964cea5278d452aa561000d7061a6c86e873627db29d3609244997d50a5db03b`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5836f6601d6343fbd07beb3077ada1cf59f736cfa627228b0c545baac0890905`  
		Last Modified: Wed, 10 Apr 2024 02:56:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b7dd2f4076215087fe09066567687b30db2fcbef4e6cb55cba92cf656b08f760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5708401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f74ee1e0312df50d7bf775a1b316f34e32aa4656c340448c50fd923d5a09c00`

```dockerfile
```

-	Layers:
	-	`sha256:1e0ed19123922dd46dbcb240d218d53f41f8c2a8be2f618bb67aede0d36057da`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 5.7 MB (5653777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e902d2b954242b3c684ad1989a093e992e081b252812d12117c9a2319069b22c`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 54.6 KB (54624 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:fcb4ce2391b971fa041355b02422e3e9860a378e71950c849bb604f9f21e8f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143953349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017c3960a7bcd4e92dcbd61e067df793aa2f3f2d82a4cbf25af82c70ac591d99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=15
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b7e25e29f27289e038b18e93d3224ed3a0fa6c7efee12f22d0cb5948e7cf6f`  
		Last Modified: Tue, 12 Mar 2024 18:40:33 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1026c04a466ad11a0463f3871101332ed1d7b2a94c6c8658967b61b816051318`  
		Last Modified: Tue, 12 Mar 2024 18:40:34 GMT  
		Size: 4.2 MB (4150678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb97f1d294940480b4284e2d2aa5e56e483efc5604366ddb7adc91adbd4c13c`  
		Last Modified: Tue, 12 Mar 2024 18:40:34 GMT  
		Size: 1.4 MB (1423814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb0feaba46be7763be4397048a1ea9227022b27d9fb1f40436fb8177f5208e3`  
		Last Modified: Tue, 12 Mar 2024 18:40:34 GMT  
		Size: 8.1 MB (8066355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ad86e823691876e310be0154994dbc835c1623b00137f8bf205f5b9c81078`  
		Last Modified: Tue, 12 Mar 2024 18:40:35 GMT  
		Size: 1.2 MB (1194851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6614676044a8ef6f94a90cb6f33340edd4ab98019376ed5aaed5dad2ad15057b`  
		Last Modified: Tue, 12 Mar 2024 18:40:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02acc895a13abcac8992b9988d7a037a5caded8d135a7517c536f759043f0131`  
		Last Modified: Tue, 12 Mar 2024 18:40:36 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ab29222a02ccb01c069e6b74feef52bc06920a16ea121b92bcc5744fce0791`  
		Last Modified: Tue, 12 Mar 2024 19:13:32 GMT  
		Size: 102.2 MB (102213523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24a80a23cf490378c1360a69e1923b9dbc729ff7fa3818bf4b2c9cdb537e4e3`  
		Last Modified: Tue, 12 Mar 2024 19:13:29 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5283a980fe2777009022e18df36f60511fe98b4384793d23f3d43c936b560a49`  
		Last Modified: Tue, 12 Mar 2024 19:13:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84a091635e90aeb002b7564e1832ba5fa15088fe413e4adf3b8cdcbdef4dd94`  
		Last Modified: Tue, 12 Mar 2024 19:13:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e309c3fbb5ac901701fca8df03378a407f2e4bf0afc737f4a979b011be56f7a0`  
		Last Modified: Tue, 12 Mar 2024 19:13:30 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e208016d2651689ea437d7ed883ef9dd215d92e21ff2f7d6f7b5c1b2eea6ddb`  
		Last Modified: Tue, 12 Mar 2024 19:13:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1eb6743950a0ee9535be74723a96152399f7eededfb1551909817e192b9178d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5721146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead35f09c7721deb39b2afb6d5b73b9085dd4463588ad4a71a3050607badca26`

```dockerfile
```

-	Layers:
	-	`sha256:daea2ee35ada88a0a70545b390b9b96731dc327cd5f934ef9fd81c0c2ba924c3`  
		Last Modified: Tue, 12 Mar 2024 19:13:29 GMT  
		Size: 5.7 MB (5666475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2d13648b66eb125fc6c4df3fa10f9c4aba2fd7c8d9032da3e07d2e457a12ec`  
		Last Modified: Tue, 12 Mar 2024 19:13:28 GMT  
		Size: 54.7 KB (54671 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:522b9694db77a837bcf7979c9e815cdcb5c1b8365905cf939ff442f82416543e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138702895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be83eb54a53fa4e5f6ad81bf9d45b11c68b08dc0211a0c8d8e512f61799f253`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=15
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807d342090414975cf9ebe119d0b9fda4f30d39ad1184aa555bd9eafa7cebf01`  
		Last Modified: Wed, 13 Mar 2024 06:02:03 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f16e3dd933c0f4a5cfa4bd4503de7b9ce57b2f00f49a490935fec74088471a4`  
		Last Modified: Wed, 13 Mar 2024 06:02:04 GMT  
		Size: 3.7 MB (3742448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844a1e04f54e7f856212a2a0ffac8eaadfb2598b04e502ecefb775c3a6ef9abc`  
		Last Modified: Wed, 13 Mar 2024 06:02:04 GMT  
		Size: 1.4 MB (1413602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3e99b78565b4cb3a298a0f455fcb77bf408305d0a767aba35d9780d9a6e299`  
		Last Modified: Wed, 13 Mar 2024 06:02:04 GMT  
		Size: 8.1 MB (8066227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b359a7ae0dd961f16e6e27af6eaa5c8646947d87c9b20dc9a4aa7d2e6ae24b`  
		Last Modified: Wed, 13 Mar 2024 06:02:05 GMT  
		Size: 1.1 MB (1066941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbbaf375cb392522b01353e4e5a8bfae3ff54647b52b6f39a1f206bf8564fc4`  
		Last Modified: Wed, 13 Mar 2024 06:02:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9147c95c29f7ab8f7e65cb85a251b1ef5c5d7e1216419dd71eb4a5ed0a32ed88`  
		Last Modified: Wed, 13 Mar 2024 06:02:05 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7706c74158994ac52f384a41ce28abd06bbda36fbc45c9af81a474a6dd8e4c`  
		Last Modified: Wed, 13 Mar 2024 06:31:52 GMT  
		Size: 99.7 MB (99676844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40190c7cf8a1614be26a5828e902a180442ee02c3cffed8f3e4ef1c29f7aeeca`  
		Last Modified: Wed, 13 Mar 2024 06:31:49 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a1dfc4bf6d7649a82acb291f3a639201e629f2ce6b8cb30775bbb75b80b0fb`  
		Last Modified: Wed, 13 Mar 2024 06:31:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb013dae57e529d2cfe0576655bce07c5af58af23c38e8f8cb82ba9402deec3`  
		Last Modified: Wed, 13 Mar 2024 06:31:50 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249f6955acd6ff6cf297aa7d706ade0d7e41f381cd17fb6d05a0992397b074d7`  
		Last Modified: Wed, 13 Mar 2024 06:31:50 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1ca59d7453e8483a0078894a681ffcc400f7357876f738cdf08aebca0cd3dd`  
		Last Modified: Wed, 13 Mar 2024 06:31:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c73443cd8101c9336377c0e285347cc012b0f72e7cc3507c2a7cf6df1733e09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5720952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014010eef849595b62d9316943f1af5023e6c4ac5a96653044feab731d9fdfb3`

```dockerfile
```

-	Layers:
	-	`sha256:e153530364d9e4ead4875e2901536e032784d626a7ebc4a5175c0315d92efdf4`  
		Last Modified: Wed, 13 Mar 2024 06:31:49 GMT  
		Size: 5.7 MB (5666287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5c66c8554bf863a92e7695911b0eb45e904a46190728eeca9ae430378bc12c`  
		Last Modified: Wed, 13 Mar 2024 06:31:48 GMT  
		Size: 54.7 KB (54665 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:cbb3b6e7ad3ebff4edf015e90bacbe9b78f196ba50e769c6cda8524b43caf64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.5 MB (149486049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86034bee565cc6e4b45ce6f334adeef245f0c0b37fe06ba0309e1ee4bc8887e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=15
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf75f217268500ad7e781f5a11660d9aba2adb3e24951da3322be648ecb83ba3`  
		Last Modified: Wed, 13 Mar 2024 03:52:53 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7354aa82f25b199783ffed4abb2934fb9c47dfa0497ebb931409e692aa13219`  
		Last Modified: Wed, 13 Mar 2024 03:52:53 GMT  
		Size: 4.5 MB (4498792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f2f4668b6a9886b83b69eebdc95a30f1b480fdbf002085df25a5f498229a8f`  
		Last Modified: Wed, 13 Mar 2024 03:52:53 GMT  
		Size: 1.4 MB (1378686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff84ef54facfbb2d9d933089f865eba3f4ad079a4f4205569d45595197bd9b79`  
		Last Modified: Wed, 13 Mar 2024 03:52:54 GMT  
		Size: 8.1 MB (8066297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2047c8c12c2d41c9ddd6515a74e5c3531a3e010ceddb4567eddca5eb0c4dc3fd`  
		Last Modified: Wed, 13 Mar 2024 03:52:54 GMT  
		Size: 1.1 MB (1108652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a6174203e1a308d49571f7ec0103c06492df572e4b5cdedd5161748a7907cc`  
		Last Modified: Wed, 13 Mar 2024 03:52:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99eea1c16ac89bed0ae2f94017e70c378193cfdb5f0a624453e316fd2107ade`  
		Last Modified: Wed, 13 Mar 2024 03:52:55 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb04454854881f52ca375c91a17221b0321876e50b0167365a8ddacf5910630e`  
		Last Modified: Wed, 13 Mar 2024 03:55:07 GMT  
		Size: 105.3 MB (105257081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a752b85a77a34fe0cbd7b513a7600aeb11d029b0a79a0e9b110893453d87103d`  
		Last Modified: Wed, 13 Mar 2024 03:55:05 GMT  
		Size: 9.8 KB (9777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c18e4f8db80fb65156e666b389ef3a07a3048cf9b7f43ad2b1cd7aba1db8e`  
		Last Modified: Wed, 13 Mar 2024 03:55:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d582d7983e89b03be0fe33c4e6a43ad4fed6b3baf971a9f5a3d56fa51ce93898`  
		Last Modified: Wed, 13 Mar 2024 03:55:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728eade610c4f62b57d73454835a8d4795b27c05bea03ecd42d9e4bfc56fa0b2`  
		Last Modified: Wed, 13 Mar 2024 03:55:06 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bd0a4bf2c48eb8aa22faf6ee12fbc906760205a8b48640b0a8a79b0c8ed44b`  
		Last Modified: Wed, 13 Mar 2024 03:55:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3d6c84d888d4ba38a947918207d485d303496a94308ed457f6f906826d3e3afb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5715825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6195c8db308a9c74f1950bdea02816fcca596b443ae87f7d458e7543991a93`

```dockerfile
```

-	Layers:
	-	`sha256:0f545ca28d1d54b2d40b41242341676af35d0094b7bc6566fd8e8e6fb0f919db`  
		Last Modified: Wed, 13 Mar 2024 03:55:04 GMT  
		Size: 5.7 MB (5661357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a4901058b43e7396af60e6df40a7e1b91573d592ad709b05a46247d75933dab`  
		Last Modified: Wed, 13 Mar 2024 03:55:05 GMT  
		Size: 54.5 KB (54468 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:2f2f8ce1b341776cb49a16f77bad6e16beb0153a823718d48351fbeb1615f8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159300808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6642f59b5827dc34b7154dc6f2e3583a89e8c1385008fedc5358d74df9272075`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=15
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f82a3f4850d0b20ef665d91a8fe5b6159bc70cb20d64afb9624f7272a2712f`  
		Last Modified: Wed, 10 Apr 2024 02:16:46 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc4428feddcd520fc581eb8092665ce66656216c0fdce82d0258d52c05b08ec`  
		Last Modified: Wed, 10 Apr 2024 02:16:46 GMT  
		Size: 5.0 MB (4964448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799307dc2286d0e3e4852305826d2bbcd45074aaef3a522a2201317c8c14cf30`  
		Last Modified: Wed, 10 Apr 2024 02:16:46 GMT  
		Size: 1.4 MB (1422093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201521f20a314ca46c9a1ff987d88b473db97c84e0419ef6b8a0df31b0c9c3b0`  
		Last Modified: Wed, 10 Apr 2024 02:16:46 GMT  
		Size: 8.1 MB (8066271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d015c334ae015b66f2cf07e859b07195711d2cad67cbdf424fed3a1edf83ba46`  
		Last Modified: Wed, 10 Apr 2024 02:16:47 GMT  
		Size: 1.1 MB (1137141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ed4571f7a0f1a3087d97006486379e3df4703724c21f72dc101eae36087af3`  
		Last Modified: Wed, 10 Apr 2024 02:16:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526a3c7921204a3036a6c27f270b0186847f3776da45ccc57108e3451b1c9fa2`  
		Last Modified: Wed, 10 Apr 2024 02:16:47 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73af3db8fa347abc23cf0eec4c82076c85c6b1c7734de7cec4cd2bd07da0a77e`  
		Last Modified: Wed, 10 Apr 2024 02:16:51 GMT  
		Size: 113.5 MB (113544222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6a6715c83189f9439221688fa7bda5d4df6f0e45836348fbe174301c41971d`  
		Last Modified: Wed, 10 Apr 2024 02:16:48 GMT  
		Size: 9.8 KB (9787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f911d11f740735e00b4bf765b1deb8d3c4694df22547d9198c2099c0e8a36d`  
		Last Modified: Wed, 10 Apr 2024 02:16:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149cd368ebee38efc0ba83434a0e57e386ca1c1ee0997a83a043949d6eb8bbaf`  
		Last Modified: Wed, 10 Apr 2024 02:16:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecf21237509ad3c539b9167823c7b718c9df75955165e13763ae9dc04e0acfb`  
		Last Modified: Wed, 10 Apr 2024 02:16:49 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02c439cd8f6ad880c90040543c528c6cd9ffd3769c4694834430410333b4713`  
		Last Modified: Wed, 10 Apr 2024 02:16:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:50e702712cfe3b9af2086e5b3654d83448773f559b346df8c7e548a8144518c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5717828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fddbd930f43a08476364cc10e1f249142edd9fad19d4881b2d98e62e89e46be5`

```dockerfile
```

-	Layers:
	-	`sha256:716cd4754066790af90e00505d7af025ebc70b6b9c564bb0a322f344940e0bf6`  
		Last Modified: Wed, 10 Apr 2024 02:16:46 GMT  
		Size: 5.7 MB (5663254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f1117816136219ce85766663f8cd2910fdbe567724f00386c453340ef12167`  
		Last Modified: Wed, 10 Apr 2024 02:16:46 GMT  
		Size: 54.6 KB (54574 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:ae34ff79d1cf4124e23bd7811375af389cdd8897922932e5122fd9acc24c5420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146651352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc281bfda7f8c5ce1d8d9d1c3edefb3a33fcde5d8d5ff1b285c4ed33c5bce98b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=15
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a30af2f3ec090c03e7d7a2b5d0d2dddf7b5dbdd77dcde663345478af995cbb2`  
		Last Modified: Wed, 13 Mar 2024 17:13:13 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0601e54a6797001b9435e78c78126a616bbda8ef9f0e5f8a43582dc7d5676dfb`  
		Last Modified: Wed, 13 Mar 2024 17:13:14 GMT  
		Size: 4.5 MB (4474435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66d20408250df1df7e030b13a3a0bca33b8b8747ed5c2838e6dee74c14eaddf`  
		Last Modified: Wed, 13 Mar 2024 17:13:13 GMT  
		Size: 1.3 MB (1333732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fdfdf507f59acdcfef1c6ad755ce7dfc25868e0aad2b22e5062f63bb9fcc56`  
		Last Modified: Wed, 13 Mar 2024 17:13:14 GMT  
		Size: 8.1 MB (8066411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1cf8a272ec43206e517fc55430ed0bf3f9bb0d3892f0cea9745238f53a67d6`  
		Last Modified: Wed, 13 Mar 2024 17:13:15 GMT  
		Size: 1.2 MB (1182572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9eb7585030eed05da021b1eb44837ba11151389fe448f4710d86b2b52194b`  
		Last Modified: Wed, 13 Mar 2024 17:13:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33b2761328ca07faf0b2a55fdf02a546e70d6595f177aeaab5c9301be640f83`  
		Last Modified: Wed, 13 Mar 2024 17:13:15 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bf4b17b73bfa702e69b863ab8da5a0d3ecdbc193f52b0e19775462b905f044`  
		Last Modified: Wed, 13 Mar 2024 19:35:51 GMT  
		Size: 102.5 MB (102454882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff4c76e80282ab7f06fd30195cc79fc4b145fc864805054261595dc2a3b48fe`  
		Last Modified: Wed, 13 Mar 2024 19:35:42 GMT  
		Size: 9.8 KB (9788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6b4c7c4193752dda96ecac8a6daae4d3002cdd486736015a50524241b529e0`  
		Last Modified: Wed, 13 Mar 2024 19:35:42 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171d52c3123a675f196c237dca55b942bcacdd1ddeebb61cca6c4af944d9cadb`  
		Last Modified: Wed, 13 Mar 2024 19:35:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9360eba7459d2fd53e78b838a657cbbafe8c6f901e85641e594bb27949cec6`  
		Last Modified: Wed, 13 Mar 2024 19:35:43 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e367a8e1f6e27ed87ceb9fc81722ed659e4eccc659d4b881f2aa2ce05a8d2241`  
		Last Modified: Wed, 13 Mar 2024 19:35:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:97c41015b426b0daa362d8b54f16ecad75699e68e7bbc63bb42b966fbc884d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 KB (54333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c13df36670aee12466431dddf60382e6cbdb2b979f723803bdf828d12dbd9f1`

```dockerfile
```

-	Layers:
	-	`sha256:e219dc1a6bab4997695d4d1861d818078383e726d0a6414163a713a3d72d0864`  
		Last Modified: Wed, 13 Mar 2024 19:35:41 GMT  
		Size: 54.3 KB (54333 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:4c1a1ceb1eb4054f175693b317dcc1b6d0a76ddad65a6dca9e3b787c7bcb6cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163445916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8cdfb3dfc82090d90ddf0d41dcdb2316d8ea7bf69ef00c0ff54b30fd607236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=15
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a930ac8e959776320f9b0be7afcfb086cb1feb77f62c9630bd0fe5c9614c22c3`  
		Last Modified: Wed, 13 Mar 2024 06:15:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eaba282419d7afd073bceeb887f9dece5c9c8ff119e1fdb28ab8cfefd236368`  
		Last Modified: Wed, 13 Mar 2024 06:15:44 GMT  
		Size: 5.4 MB (5368100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c00a48383c965fcda0d10f02ce8ab025e519a9aff5ff9c59ed177287ed5ba7`  
		Last Modified: Wed, 13 Mar 2024 06:15:44 GMT  
		Size: 1.4 MB (1368616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aa41261a56179b463f394862883cc21afeae8937fd877e030f824ce2697894`  
		Last Modified: Wed, 13 Mar 2024 06:15:44 GMT  
		Size: 8.1 MB (8066373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fca10622f0f7c745e192a804190963b0e8d74d7e5dc68e33d51e8d1131a311f`  
		Last Modified: Wed, 13 Mar 2024 06:15:45 GMT  
		Size: 1.3 MB (1283504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ce995114302dab0b1aa5afdfd1296c0a7f54e7d294ef3e557531bf5f1d7196`  
		Last Modified: Wed, 13 Mar 2024 06:15:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad0e452f685355921e5f44e0db6ddfea6c514719d6da79d7c61349985a9b5ef`  
		Last Modified: Wed, 13 Mar 2024 06:15:46 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4239df2b7494cd1d97a8560b1a7cb3302d35770f4298df12ba39e4956e574b3`  
		Last Modified: Wed, 13 Mar 2024 06:19:55 GMT  
		Size: 114.2 MB (114220193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1956b284326cd2483785e1fd2e78366488f05f459cb3e144404950eddacbc183`  
		Last Modified: Wed, 13 Mar 2024 06:19:52 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e730af9e68c8a04205286142b4f348fa7810121430446f0daab670fb86819c`  
		Last Modified: Wed, 13 Mar 2024 06:19:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26df2f4481cbf0f3b283e1d859a05326508eb8ec84004c59651aeed57a61bbf3`  
		Last Modified: Wed, 13 Mar 2024 06:19:52 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eece229f6e0bff6b0ddc00876d0934c730f825791821cdb2ef75291216342b`  
		Last Modified: Wed, 13 Mar 2024 06:19:53 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6077402eb01c535aee9ae3569a0c7af00b16cf56ef32d72b2b015a2c2e29af4`  
		Last Modified: Wed, 13 Mar 2024 06:19:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0df9bcaa0b413a022f7455f1881a47055c6c607d1225144b041d20ff35b625cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5716808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd4d27c65f0da455239b0aaef284760756047a9e7ea7bcafd7f6cc319a25525`

```dockerfile
```

-	Layers:
	-	`sha256:531e75ac73d1e32a6e0e0ac17deb831d40d1ae6ca132423dae3ac1b13a9607fe`  
		Last Modified: Wed, 13 Mar 2024 06:19:52 GMT  
		Size: 5.7 MB (5662290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bfce7e17d89de468ee294bd2d7f24d68e1e06b86c252de353d8245225eff322`  
		Last Modified: Wed, 13 Mar 2024 06:19:51 GMT  
		Size: 54.5 KB (54518 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:f5c93983f243b3d72f009119f554b7e229e1e944b48c72267eea507f50b6cbee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156801269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86072e114210fb5463e34996acc3435be31f92deded4e34f0b923adbb09a5faf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["bash"]
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV LANG=en_US.utf8
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_MAJOR=15
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=15.6-1.pgdg120+2
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Feb 2024 00:46:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 21 Feb 2024 00:46:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 21 Feb 2024 00:46:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2024 00:46:13 GMT
STOPSIGNAL SIGINT
# Wed, 21 Feb 2024 00:46:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 21 Feb 2024 00:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7509a7295798085c87f35a4e4b3f9fe7387acf0bc9e84d38f3007ea04109a98a`  
		Last Modified: Thu, 14 Mar 2024 04:09:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a4528c8c02f8ef1e012d85db736588508c59ff6cabba05d73b668b8ac6f5f`  
		Last Modified: Thu, 14 Mar 2024 04:09:34 GMT  
		Size: 4.4 MB (4390732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd7c4c65ee157ff2fb619114b56837576076d749a4ffcf42a9a581638001ed9`  
		Last Modified: Thu, 14 Mar 2024 04:09:33 GMT  
		Size: 1.4 MB (1412579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26f853e97781ae7605bbc7c63a781f2ae2f138d7739b282c4194d67bc4db977`  
		Last Modified: Thu, 14 Mar 2024 04:09:34 GMT  
		Size: 8.1 MB (8120360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8219d4530cd9a7613563058811e9a9ee6ee8dd61917875ea275e2e105d2e27`  
		Last Modified: Thu, 14 Mar 2024 04:09:34 GMT  
		Size: 1.1 MB (1096652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6867bef0cb35798a966d170107ff9fe85920e5fbc987083aeee98767150391`  
		Last Modified: Thu, 14 Mar 2024 04:09:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d712fe75df8cf2c6cdcf140b0571e9c86857a6555a5593d3c77a51c8d9f6745`  
		Last Modified: Thu, 14 Mar 2024 04:09:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ece83532f0be016bd9d1816191c0895f3dfc52c325c80ebd8c2861bed1b371`  
		Last Modified: Thu, 14 Mar 2024 04:16:31 GMT  
		Size: 114.3 MB (114272162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae91db2cc2cb58c41a44a5ed2d1db30b0932c221aa462482accf383439c6ff50`  
		Last Modified: Thu, 14 Mar 2024 04:16:29 GMT  
		Size: 9.8 KB (9779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fedee4a8b305367d0beb42832dc1542fd53785f113aa378e12ecd2968b2674`  
		Last Modified: Thu, 14 Mar 2024 04:16:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2822bf1c9a99504f74a200ee3a6d79724b19c8bedb5db33c9692c05205a9f508`  
		Last Modified: Thu, 14 Mar 2024 04:16:29 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96252d992733c4eafc03facec725776aa9893102bf2aac9ea5bec3e0125506b6`  
		Last Modified: Thu, 14 Mar 2024 04:16:30 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed8c4af495917d7261cd07a3fe1744405297bb70bd9a8fa9e14ade4b7adc11`  
		Last Modified: Thu, 14 Mar 2024 04:16:30 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:661734e92c3d8368cf26a59760dc100b41a8d2f5de9ca94b07ad97f4b323a739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5708913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d3472ab579b28bed645d150f8e685cc91a68912ceb277f6bbc7541fd886db2`

```dockerfile
```

-	Layers:
	-	`sha256:42dcdbe3f1ace2f06a9192381e9d9cdf53abe1079c535076bb468d120b829966`  
		Last Modified: Thu, 14 Mar 2024 04:16:29 GMT  
		Size: 5.7 MB (5654455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df50f713862eedbc140b60bfdd496551023b0b1a5c97f361321a3c8763a3dfbe`  
		Last Modified: Thu, 14 Mar 2024 04:16:29 GMT  
		Size: 54.5 KB (54458 bytes)  
		MIME: application/vnd.in-toto+json
