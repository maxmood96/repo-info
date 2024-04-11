## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:224f53426f190151cb02b03db1499b999e06025c71b6e73b021b0c83c608ecad
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
$ docker pull postgres@sha256:7e30f5b61fccd7fc08ee5d5594bcebac83f1b8c77d05c88bd43fe563ca266a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153363009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60dc4bd84c0a07f26f1eb9feefcc94d1dbb3a2d478a0b705aa5e7311353108b`
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
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg120+2
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
	-	`sha256:e59e71301578159674bb282350342be355637dc9bdbbf4c3fba9e1234f2407b1`  
		Last Modified: Wed, 10 Apr 2024 02:55:55 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30258475ebe692e9b60d517e07df053f091bab49a77a43c859db77346914bdf3`  
		Last Modified: Wed, 10 Apr 2024 02:55:55 GMT  
		Size: 4.5 MB (4533459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0c37c3ab3cb0f44a3ca1b4f76367789b752a6ae307705358820dd51cfa0eed`  
		Last Modified: Wed, 10 Apr 2024 02:55:55 GMT  
		Size: 1.4 MB (1446658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80df7455ae43c0bc5f3efa93665d8e5ba3f8f271f1405088683e7e958854882d`  
		Last Modified: Wed, 10 Apr 2024 02:55:55 GMT  
		Size: 8.1 MB (8066235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c200c670beef95e3ed03684ed735f0b8f6a3eb0ec2c1e0c12566973750dd82ce`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 1.2 MB (1196030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d051a616a8107545aa0dd241fc344a40bb8693f40d908c087ecc1de917774317`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c27dce0c4df503a97ac77cff4f74145f86173ce2d6996d6d3218b4cacbb791`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dae96d372746b42bf2ed46b5e429372b05f644d921631121b8f478fb0ce1e59`  
		Last Modified: Wed, 10 Apr 2024 02:55:58 GMT  
		Size: 109.0 MB (108969025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e5e72a98e9b95998ed04879326abeb70a60caedd0c4237f22ca013a8ea5af`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 9.9 KB (9917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73301da916ba246310a4f20a81767ca29301169efb8a77513e1cfd10fc6aecd4`  
		Last Modified: Wed, 10 Apr 2024 02:55:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673a1691030aa21b5067d93f15eca6f65b32b473a7790313f93afa920a590d9e`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d03b1cb8d86b4636df11019cec54bdac0722aea2a291cad8359c0e84337189`  
		Last Modified: Wed, 10 Apr 2024 02:55:57 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d680d6449b51d9dd7211ee35cd58e29092fabc8c8ead5eb0d79b268c379db41`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6c634452bfb2095fe25728562d8351a1cdea718256fc9278c3b08737a1e21712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5774424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795e47b7a6ad1e2088a232fbebe1741ff795d077fba8259ecd798d9a46ea51c1`

```dockerfile
```

-	Layers:
	-	`sha256:6b87c9958b37b6ad24e7d77fd3b263baacfebcc08d9961d38e787f054cf91d63`  
		Last Modified: Wed, 10 Apr 2024 02:55:56 GMT  
		Size: 5.7 MB (5719191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:221d973deff9eaf8a2495b7346950f7c4d8e3aa761e16ea600904b512802b771`  
		Last Modified: Wed, 10 Apr 2024 02:55:55 GMT  
		Size: 55.2 KB (55233 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:7a6816eb0028b8803b86ef523bc53162b69badf64a05ec8f4b34d8583f6e0044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146108013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943d9cea79451c647deb6851fc2206e277b68f9c6cf772930fea475e98e362f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
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
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg120+2
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
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155d3a4880f07836b2e537df01530f5d923444c7951d951ab7fd05f2a1d74c55`  
		Last Modified: Wed, 10 Apr 2024 19:51:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee6df1a8b247af2d7dd5a0ec2ec59769980ac60712bf7024b8078c662479e72`  
		Last Modified: Wed, 10 Apr 2024 19:51:24 GMT  
		Size: 4.2 MB (4150765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b6213477a018cce25fd1c46e80f5727c9b26707a86b3d128645c7d6dad69c1`  
		Last Modified: Wed, 10 Apr 2024 19:51:24 GMT  
		Size: 1.4 MB (1423846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b08d577a233235e6f495aa7ac9b59bef0c2bb8a3b2e9c2497311f50066aa821`  
		Last Modified: Wed, 10 Apr 2024 19:51:25 GMT  
		Size: 8.1 MB (8066319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17c672ead182aeb6eb02434a42dc01ca8e61164efa7d2dfc1eb780ba805e889`  
		Last Modified: Wed, 10 Apr 2024 19:51:25 GMT  
		Size: 1.2 MB (1194848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdaa782fb51041c74aa5f9edf161da10efab118c4698222822dbca7cc0a9074`  
		Last Modified: Wed, 10 Apr 2024 19:51:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de1f8472a402f7e352a9699cc383fe78f77a3dfbdf1f32c89bc847d5176f057`  
		Last Modified: Wed, 10 Apr 2024 19:51:26 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6176d35e07f63080f3f9738b095be9ec65513e2b0a779ca80eed8e9028ec3cc3`  
		Last Modified: Wed, 10 Apr 2024 19:51:29 GMT  
		Size: 104.4 MB (104361419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb09da036759a334fffd21fbcd6c7349ba06253f23b24618e2629e69b3194a9`  
		Last Modified: Wed, 10 Apr 2024 19:51:26 GMT  
		Size: 9.9 KB (9926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58458f4bd45994d4ae8a8df8469c660f39789bf9a3ed985facdb581df973c13d`  
		Last Modified: Wed, 10 Apr 2024 19:51:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fc2052d0cc4372c5de3b03e3a0b5743e64dd16506170996390df7ce463d8e0`  
		Last Modified: Wed, 10 Apr 2024 19:51:27 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d983ffcf6ecc34429c1253088d409e78f7809274fa49f17aa45eb60631a4fd2`  
		Last Modified: Wed, 10 Apr 2024 19:51:28 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbf001ada9c957cdb54148c3f05e12b62623eb84b6b5e47b3aaadc4aea60fbe`  
		Last Modified: Wed, 10 Apr 2024 19:51:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:770bf6257e3156ec073faa21185f63b40d156d24458b6b0d81dd32c996be0d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bad032256583f91550d0c7ad55ea7a6d8bb919ee603275323cf8144699a7989`

```dockerfile
```

-	Layers:
	-	`sha256:08dbbf0aa489ac276477943ce5262eb04d3acfcfeae1a2a3791594422bcc982d`  
		Last Modified: Wed, 10 Apr 2024 19:51:24 GMT  
		Size: 5.7 MB (5736316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7cb5d77e10d456772339d90a7fa20d58446a6bb8c04526e1e367394c375e40f`  
		Last Modified: Wed, 10 Apr 2024 19:51:24 GMT  
		Size: 55.3 KB (55294 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:107b2607ebae6bcff8454503c433da73fb5fe87d100b4cdfd7bc68adbfd427f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140839949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c444bca0221fdda24c1ad2e2906af3d67cd393f2a92e8e5a9c1c6b8d833c52e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:405264a6fec3e83d872f4297605fa82dd8f7a7724cbccbb7ebf06438266aa933 in / 
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
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg120+2
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
	-	`sha256:c774609c4cd3f6537d30d03e0ad1c935b83618698a710164c43debe51dadfd87`  
		Last Modified: Wed, 10 Apr 2024 01:04:25 GMT  
		Size: 24.7 MB (24722923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26825e0337a560fed35b540ff00c2afed49ddb1a54481903b349bca0f04c1ab0`  
		Last Modified: Thu, 11 Apr 2024 06:40:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc34362f67cf60e61ce4847d515781b56786ae0eecc8f275955e52ef55f96747`  
		Last Modified: Thu, 11 Apr 2024 06:40:25 GMT  
		Size: 3.7 MB (3742464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117bb1dfbb4303db45eae16b1f8274ec3e29a87b7df1977ebb74a007727bdd95`  
		Last Modified: Thu, 11 Apr 2024 06:40:24 GMT  
		Size: 1.4 MB (1413612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe2628bf7e7774b0a4d4e6da2e6fece3b6df260db31d4f1df060bfb4275bad8`  
		Last Modified: Thu, 11 Apr 2024 06:40:25 GMT  
		Size: 8.1 MB (8066212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682e08b2a73bfcdde1d17208bedae85502a0a1a587fc6547abd5252fe616174c`  
		Last Modified: Thu, 11 Apr 2024 06:40:26 GMT  
		Size: 1.1 MB (1066953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780b65613c101309c25a3ea9e6c26ef1b739764bb681be2f15f50b010c15c5b7`  
		Last Modified: Thu, 11 Apr 2024 06:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a8c27024768c7658a498536a8da2a4ec19557b262652dad3df97357566bbdd`  
		Last Modified: Thu, 11 Apr 2024 06:40:26 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c285dacebc4bd0a6169d11fdb5d400c2aa041bc6ed04ed83a366dca7c5e7c42b`  
		Last Modified: Thu, 11 Apr 2024 06:40:30 GMT  
		Size: 101.8 MB (101807539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bde5dec5786e348909628734ae00d820db8aee11da93cba05f2b4861e0a744`  
		Last Modified: Thu, 11 Apr 2024 06:40:27 GMT  
		Size: 9.9 KB (9925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc195cb4c11d549ba519d2d8a9a5082a4c6d93ed648908c7e8d6e6ba2c56e9e7`  
		Last Modified: Thu, 11 Apr 2024 06:40:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad05448d1227587d90cd47c91072e635ddf05d5885a9a67f67fc689aa23c2846`  
		Last Modified: Thu, 11 Apr 2024 06:40:27 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2589cdee2dc3999180415a41cf0a83a465d195bdbdcb2e13eddc9a0509063e69`  
		Last Modified: Thu, 11 Apr 2024 06:40:28 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c994195c93d9895930e95dd8f092435dfbe35fa86cd2b65070c77598bd2c9a`  
		Last Modified: Thu, 11 Apr 2024 06:40:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:7ccc960ac32b348d29ed00971227d09305d8c6b0ff1d3039707a6126e8a812e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5791423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30ee9eb66d7bbbc4150e5fb73f5809a1823e3a847a62004c4c3995ff0c5ae67`

```dockerfile
```

-	Layers:
	-	`sha256:a1b2d72e177eac459c1214c271e5d3a14d6e6fe16401c5a3f3b18c08f98e2306`  
		Last Modified: Thu, 11 Apr 2024 06:40:24 GMT  
		Size: 5.7 MB (5736128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e42baec51eca075df09f058cb05d521d03918c9ae9d4b3d1ce24fe1e77f9f38`  
		Last Modified: Thu, 11 Apr 2024 06:40:24 GMT  
		Size: 55.3 KB (55295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:ee2b987772a7a37892cbf3c91cc73fed4246475cbc7a234fcfd0623b12402117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151554786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4ffc32b30ba1f80294a3aa127db06a7b3bbbd6024e338fc572bcaa94e8e5845`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg120+2
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b22633fce1bf38e3dc7d5a988447ae2a46b61593276c2d821ab42dc5026822`  
		Last Modified: Wed, 10 Apr 2024 20:27:44 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e6435e69040984f43b95489d1724e699355472fc4c827794c5d7257452772d`  
		Last Modified: Wed, 10 Apr 2024 20:27:44 GMT  
		Size: 4.5 MB (4498833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc195e1b2c0e99cd0ed0879417a5369713974b6a5a73cdcf8570e31a81a33fc`  
		Last Modified: Wed, 10 Apr 2024 20:27:44 GMT  
		Size: 1.4 MB (1378668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6833124bf59a019b5de378a677d1bec1d4a86a8bf5a427b289fb975cd2e8d5f`  
		Last Modified: Wed, 10 Apr 2024 20:27:45 GMT  
		Size: 8.1 MB (8066243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108e79d8080f3bcca1d29a67ce8154ddae602ddd6c15e9d7fda552a109f210b1`  
		Last Modified: Wed, 10 Apr 2024 20:27:45 GMT  
		Size: 1.1 MB (1108679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadbe0f8d7c2f37193b723a97b7e04edd3506fbf2bce5131a671d63006be117f`  
		Last Modified: Wed, 10 Apr 2024 20:27:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23378a7512e0ae79b913ba72ba2327740f5b9c255a844b89e2abd6f8e8c3bd52`  
		Last Modified: Wed, 10 Apr 2024 20:27:46 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ac056b6a86e253df97cc670e4c570ca948c86c7a10da01bcd18bf73e4c4fdc`  
		Last Modified: Wed, 10 Apr 2024 20:27:49 GMT  
		Size: 107.3 MB (107319962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28af548c1c147ec336a513ca896b401abfe21908d5376c19b867c398f0a00636`  
		Last Modified: Wed, 10 Apr 2024 20:27:47 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a111b6e3eb6fcaae892371635ca5db8f95e7e28f886379fa4c7b8d65cdab5d`  
		Last Modified: Wed, 10 Apr 2024 20:27:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae48f57758b6676c0b2c916442f5c222f34d6671e523eaa4885f337ef8c9f45`  
		Last Modified: Wed, 10 Apr 2024 20:27:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7770491d933335c8be0064e4e39b6f5e2d3d1103358ddc8399143b21d342262e`  
		Last Modified: Wed, 10 Apr 2024 20:27:48 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c76dea9dcaef6285d612151704b225dbe0e4a421f5725a2826b0ceab3f14082`  
		Last Modified: Wed, 10 Apr 2024 20:27:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5481594c3a2d0a2b7ad19e3c635cfc1cca293c21875846a286ec11aa546d9728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5780571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd056e66afbab0eb0915242cb82ec45e9575ef9465c967eafa3ac961728d4beb`

```dockerfile
```

-	Layers:
	-	`sha256:162ff711295c4806209dd6ee08c4afbb0c001347b7cf5b1a65aa983d34b4fefe`  
		Last Modified: Wed, 10 Apr 2024 20:27:44 GMT  
		Size: 5.7 MB (5725491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53be8dc580e652507e5bbfc27c118d8989f4bfff4e28e5568353c8a0297bf6a`  
		Last Modified: Wed, 10 Apr 2024 20:27:44 GMT  
		Size: 55.1 KB (55080 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:b2653f33e2b9a49dceb8f3444108222875e25d993c1ba03a89c116bbccc53be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161478425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880ae51bbcb3f097e64e6532460cc7edafe59130a2900a482d574d8929d01b4d`
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
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg120+2
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
	-	`sha256:90bc80421e8744705c780270f0d16bae38c6e5b4b75248fe4f28385c37ba217d`  
		Last Modified: Wed, 10 Apr 2024 02:11:42 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9b0e1e2caa12b5acea371e33987c0bf4d9034da32ecf60b90ce457c8008847`  
		Last Modified: Wed, 10 Apr 2024 02:11:42 GMT  
		Size: 5.0 MB (4964447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2031997a56fc0298a5c71941c0a94964ff4e19fbc933f49e08cf1f871202e1`  
		Last Modified: Wed, 10 Apr 2024 02:11:42 GMT  
		Size: 1.4 MB (1422102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0106ca3d71d894cfc3144f3662a6f1568d9db1c98dbe340148518dff185ffcdc`  
		Last Modified: Wed, 10 Apr 2024 02:11:43 GMT  
		Size: 8.1 MB (8066201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7529b4d382a05b0499898c238e57b3ed67bf7b2643b0cbd7b71455c9fea540df`  
		Last Modified: Wed, 10 Apr 2024 02:11:43 GMT  
		Size: 1.1 MB (1137154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fb363f79df209e897c2cf38bf9b430dfd9e5a3156c52fcb82969724bb5c632`  
		Last Modified: Wed, 10 Apr 2024 02:11:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdeb6421c5504427511ccb360c99bfb3d492951ccdd901b2c65628314921168`  
		Last Modified: Wed, 10 Apr 2024 02:11:44 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbbac54a944ecb34387afcf50acd7ca663334836b0490dffc9e2400327cddcd`  
		Last Modified: Wed, 10 Apr 2024 02:11:47 GMT  
		Size: 115.7 MB (115721752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d967d36c17d27c97d618a74f91fe9a1e7380fabebe11ca3e6010dc97c0c1b9`  
		Last Modified: Wed, 10 Apr 2024 02:11:44 GMT  
		Size: 9.9 KB (9927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11322ed8b62c362865928367b9cd72f9c3fc095536aac77a31f03dae50d4f988`  
		Last Modified: Wed, 10 Apr 2024 02:11:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2347c07a19797cf1b2f54901c09d97c9d692961a1ebb8308b92d0cc35ed8cc02`  
		Last Modified: Wed, 10 Apr 2024 02:11:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b198d8128a54f6f29af15c0f269cba66223daaac4ad669ae57f5ffa10526985f`  
		Last Modified: Wed, 10 Apr 2024 02:11:45 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e9a812fc16ff74b3d33744e946b5fdb8208a2fa77f88bd483600a3268b9ce8`  
		Last Modified: Wed, 10 Apr 2024 02:11:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:acfa3d95efa8bd72366d3ec656592e4856c11bbcd00e07b1095cd1be61c1f76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f51baba62aeda29d4a8701213d1520e998ccd89a8c05d0cdb9b945b8da158cb`

```dockerfile
```

-	Layers:
	-	`sha256:9564cf319657b7fc173e978c5157a642d7af188518ccb13eda3c9df5b1f4c2f0`  
		Last Modified: Wed, 10 Apr 2024 02:11:42 GMT  
		Size: 5.7 MB (5734343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4b8195ae0c24cc7cedae0aa91547d461b9f654c12141e17fc7697cbfce32aa`  
		Last Modified: Wed, 10 Apr 2024 02:11:42 GMT  
		Size: 55.2 KB (55172 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:41b83d94582b53a7495906df3be5aa73f194d6957a5362248dd2745bdaa3473b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148778126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f34bab321bcc21b9eefcdba1d404724e05fa533d56c79699257d40aef70ef5`
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
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg120+2
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
	-	`sha256:3c2c05a39f6994992e41ef823b7a402ac8ee18efd65ab85ec734bc0d24ddc77b`  
		Last Modified: Wed, 13 Mar 2024 17:13:25 GMT  
		Size: 104.6 MB (104581512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2038018cdeb2c1c1e485052e683e8b9263e844a1a6887550e1d51420570b382b`  
		Last Modified: Wed, 13 Mar 2024 17:13:16 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9251d44517d08aa6f40dc388a240dc341aa2f46903a72cbbed43020f5b384ae`  
		Last Modified: Wed, 13 Mar 2024 17:13:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42675a47f51d9ef5294fe8c78290fa095dea456fc0ecd04661952f7aad22bb9c`  
		Last Modified: Wed, 13 Mar 2024 17:13:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e94c0044bf1224ab0eedfa89dcccb6e48a62352867d2a2099f9b8a5a19e223`  
		Last Modified: Wed, 13 Mar 2024 17:13:17 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800be0304d2a3948164af5279cb716f8b00641e3561f62e99d98ba3e1d615cc8`  
		Last Modified: Wed, 13 Mar 2024 17:13:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8c2fac1601438bc53c7fc8c250eeace213c91844866b2086b99120156cf463a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 KB (54959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cb1354e443f534cb13645b9273c553e426e5a79195d5459722a3ed646a2aa8`

```dockerfile
```

-	Layers:
	-	`sha256:453b1f1db9d3b9947681be8fcd930ac0c4db799366025f895d67ee7c17420d63`  
		Last Modified: Wed, 13 Mar 2024 17:13:13 GMT  
		Size: 55.0 KB (54959 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:600ecf8dc4e686744e02b20238bee287204ad5710376c074ec9385b726312759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165545506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c4139e799faa91e2211a57b461c59080a650aa3c2e71d34396b0f273dfefd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Feb 2024 00:46:13 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg120+2
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2d6757733ece08f0ad67b561be0bb635b7d5c664205b7eaa65ef5ecd0d93f9`  
		Last Modified: Wed, 10 Apr 2024 21:27:24 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc217f41c2b6dfb2eca175e0a6c00ac70fa62c587a5f90905bb09294e93108e`  
		Last Modified: Wed, 10 Apr 2024 21:27:24 GMT  
		Size: 5.4 MB (5368102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84aae58b37f95dbb142fdaf2f362e44c0d866974a22e135cad393948d2f82609`  
		Last Modified: Wed, 10 Apr 2024 21:27:24 GMT  
		Size: 1.4 MB (1368653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bfb977fd9da81dcdd8627095c765814cfce1c9aaea5fcaee8c3f569bde7b5d`  
		Last Modified: Wed, 10 Apr 2024 21:27:25 GMT  
		Size: 8.1 MB (8066309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291e26df09f2553a165f5b70916a6ff5bec8a6cb508965c4c8c18016deced73d`  
		Last Modified: Wed, 10 Apr 2024 21:27:25 GMT  
		Size: 1.3 MB (1283553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355cfeed852a4fd7140633ac1c7c2d8053b452c5e389862d467edc5533474d5b`  
		Last Modified: Wed, 10 Apr 2024 21:27:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6266396b9eb524420134e6a5a23572296d1225b45ec587fdc3f0658a9c234e9`  
		Last Modified: Wed, 10 Apr 2024 21:27:26 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152d5d7d7e0433b630fb23ce95470d97dac9c79491c6cc360fb6abfcb19098cf`  
		Last Modified: Wed, 10 Apr 2024 21:27:29 GMT  
		Size: 116.3 MB (116313796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884451dbdad1c8abd96b0308449a2f5021af94e530bdd2fafbd0899d5ccd7d12`  
		Last Modified: Wed, 10 Apr 2024 21:27:26 GMT  
		Size: 9.9 KB (9927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da29883a40c84d2986ff39980a1caeab302e0912fd0f24610ea6b73ace9367ca`  
		Last Modified: Wed, 10 Apr 2024 21:27:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96666fecaf2cd0a8bb5ebb8fa39c239145a5264ede856c85a9cdb84d797cef6`  
		Last Modified: Wed, 10 Apr 2024 21:27:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b662cf445990cd0dda105900379941ee6d9c8a9d3d785b1d0f795765634290`  
		Last Modified: Wed, 10 Apr 2024 21:27:28 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8ec69cfb5de324006f7a04c3fc037aa74ab99cd36eb042c55e0eee22be8159`  
		Last Modified: Wed, 10 Apr 2024 21:27:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:21cd313bb30ebbac1ea6326832a79aea1911cd85e62e1a08abc164ff819d0520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d143177572dfc6f51437fedf729dc7e9c369e96e0de942e1a97f9ba684a19a9`

```dockerfile
```

-	Layers:
	-	`sha256:1666b2385973aad993a4826cc92c5815049e709e01e37e61dfc9f952be01dd28`  
		Last Modified: Wed, 10 Apr 2024 21:27:24 GMT  
		Size: 5.7 MB (5726432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0d9121c81abcb4a09e0b45a089d6b43bcfd555d79623221c37c98345000fc88`  
		Last Modified: Wed, 10 Apr 2024 21:27:24 GMT  
		Size: 55.1 KB (55138 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:f0e86442f1638f0d196ec620e6f6d195f981cd8622a22a9e4e3e3594ee623789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158879680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3798f07bc9dd50d7b14fb6b5dedd7061c74603cd16167bd9b6b489cdfe9b6b4`
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
ENV PG_MAJOR=16
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 21 Feb 2024 00:46:13 GMT
ENV PG_VERSION=16.2-1.pgdg120+2
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
	-	`sha256:59716c2616b642c2321de9f6862d7d8c2d1d87c3296613a87256d752af99cb8f`  
		Last Modified: Thu, 14 Mar 2024 04:09:37 GMT  
		Size: 116.4 MB (116350424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395e3366a0acf637ed1ced6b87e4f4a7d108c793c803d0cdf5a8a8b0ecdaddc3`  
		Last Modified: Thu, 14 Mar 2024 04:09:36 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d3691cb3229656044fbf9aad9bf9dbac54939c95be51b417b803dea19fba0a`  
		Last Modified: Thu, 14 Mar 2024 04:09:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05eb17f825138591f9a8acde85dce36bac3f07fe5d251d7d2c4b44eafbd64e4`  
		Last Modified: Thu, 14 Mar 2024 04:09:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58faa3853b5e1659ef75ca28ac493ed7479cef31ab4c52be69d89a056841cbba`  
		Last Modified: Thu, 14 Mar 2024 04:09:37 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03555530166158fd4beca4e3d5da1ecf91dba6a148fd3a5673f5233c6f34a23d`  
		Last Modified: Thu, 14 Mar 2024 04:09:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b017cb906ca4446cd975a94b1834a0de8421da6f573367eaaeebee7c7ab6aa43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5774935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230fbda1316d077f59ae0583f52c8ca47d94e6f19f76506cbd4e1d456e8a4a0b`

```dockerfile
```

-	Layers:
	-	`sha256:cf4140b52cd36970ab354e3c6f793e8cfb0095b0c70003da3c03eead4d150a75`  
		Last Modified: Thu, 14 Mar 2024 04:09:33 GMT  
		Size: 5.7 MB (5719869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60a51b7486c071ce5aa26e120b10d8304ac2bd4c5da3231b0c61475f741ef237`  
		Last Modified: Thu, 14 Mar 2024 04:09:33 GMT  
		Size: 55.1 KB (55066 bytes)  
		MIME: application/vnd.in-toto+json
