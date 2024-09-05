## `postgres:17beta3-bullseye`

```console
$ docker pull postgres@sha256:7c52005c1ffab33db2b72378dcf6b70d5d6c6b55ab713e4e4f21071f93f2f990
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

### `postgres:17beta3-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:aac1e4a49473ede112842a41e93ddb26f7753ad3e1bd9239ae87583c5222d3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146095897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc47d3861e9ec8ecd99b6821070b52af4d62a1182cac2eb6f568663a9e1a868`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:1b8ac8ec2b2cbdfc9682f076e7e579579d6df6235ed23b2e63f8eec671c52e92 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg110+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6533c3eba3f3cd4c840877f9245b26929fc8c22a39f42c872aa314c32c6d654b`  
		Last Modified: Wed, 04 Sep 2024 22:34:54 GMT  
		Size: 31.4 MB (31428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01632e99f866712395dca873f7002a0c02e6579f44736bf3bbb35372a1911e77`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05b99b41bf0909c9b5bbd18ec1de5e276c063a14de58fee8061cb206ecabb5`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 4.3 MB (4308193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ffbc6ba3d13d9bf95b07e593378ac41176592d74a782b58379148285bb0998`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 1.5 MB (1472202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b1e319f9cc5806be14653d6599172023927685a374c1705549fd6ae3adfd9f`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 8.0 MB (8044407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740f8178593f1737d0fb3285b7148988baf47dbc1c9c22bfe096cbad7f72f721`  
		Last Modified: Wed, 04 Sep 2024 23:08:59 GMT  
		Size: 1.0 MB (1038342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e514eb5f2809929597c3421e0650529ddc8c0d474b27bdc516b5d08d69c30c83`  
		Last Modified: Wed, 04 Sep 2024 23:08:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ffb6d44547d224a3bdd500006664b2f1c46f326458d450668e3279e89b3f24`  
		Last Modified: Wed, 04 Sep 2024 23:08:59 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9977e4d7b6bdacf716988af5b35a2c280d535e5379f52466aa94b9d8e45aaf53`  
		Last Modified: Wed, 04 Sep 2024 23:09:01 GMT  
		Size: 99.8 MB (99782999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c654b8268ae38d7ca7b59650772a1a36e542119672d65975b1dd255d8b2f4a`  
		Last Modified: Wed, 04 Sep 2024 23:09:00 GMT  
		Size: 10.2 KB (10247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31157d7b08254be2ba81bc279b667012a5c8ee4397bd8c61260fb8c0d23a028`  
		Last Modified: Wed, 04 Sep 2024 23:09:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd62b303ba343b08578f772c4c345626111a01c86775b80f506f1627d56f91b3`  
		Last Modified: Wed, 04 Sep 2024 23:09:00 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f9550915d594efc976da214e2932ed76acbb3314c8a5e3e8f303ce4bc214ac`  
		Last Modified: Wed, 04 Sep 2024 23:09:00 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbe2e050ef5bda95b9a6836719046f7377bf9017f98eae8c2a3651fbae5b3b6`  
		Last Modified: Wed, 04 Sep 2024 23:09:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c09c1b9e9ed9b2bf86e7da646ec8316e3274eaad922bd898415f43a4b00b7972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6062016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef023d0a3c37f471369489fdccd6c5de39afc01746fcd0c3c70e504dacc5e23`

```dockerfile
```

-	Layers:
	-	`sha256:7aab3d9416f95482361e4c5e0ddd2fd107151f5b1f06b2b2848d8294a8f9a59d`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 6.0 MB (6008459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5071e1943d29252fc72fbb32a23e60b9d2c1c9364ed15ea451fee103b19a586a`  
		Last Modified: Wed, 04 Sep 2024 23:08:58 GMT  
		Size: 53.6 KB (53557 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:e0a51fdb6f1adc24455ebfccb1a2665152b12981072265d85e9f506bd15c6ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139030759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094907f08fc6c45e2774cbe609b27c384c0b1417a743119a8b1d4725c3077bf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:b6f3f19f4bd2bf78068380b3cd10d72519ced99a2b5abe830b4729df341dcfdf in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg110+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c8ed7888c72e20491bc1a05ae8b473757ca4d400de33029eab69bacfb9dd933b`  
		Last Modified: Wed, 04 Sep 2024 21:52:15 GMT  
		Size: 28.9 MB (28924911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff08d14835d2a8416c4df6e3dd9e317c595ade6582b069f140f08286cdbad6e`  
		Last Modified: Thu, 05 Sep 2024 06:06:12 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f652cee625fb7c902694dfb64a4dcbd644862142e4dfc68893dd60dd62f5c5`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 4.0 MB (3991654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d02501ed234a0a5d8e7cbd6a3b78af584bd0c2c5a2559d08ee15ba7e5f06830`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 1.4 MB (1449215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9160d82cccd2166396d8525cd76bfc39ac2c6a06230e6c5b4fb2a4b6e736dd`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 8.0 MB (8044317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5cb92b5411bcffbc1c9ab1ecc57e17994310a00f9727277ec63f3e3cca4bf2`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 1.0 MB (1034881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52386f3c03837e7199651cb1044a0ed933f4fae098f20975ad8db2eb6262efd`  
		Last Modified: Thu, 05 Sep 2024 06:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d037fe4403f7b5c213daecbfb442898d0fca3592426a40bf38cd34bacc6ae7ce`  
		Last Modified: Thu, 05 Sep 2024 06:06:14 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc0482665e2a3cea99745b708cb34fce2dc452061f181084fd8b4ffab709ae0`  
		Last Modified: Thu, 05 Sep 2024 06:06:17 GMT  
		Size: 95.6 MB (95564698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadcdb84ef8fe9b7002b29c17f7d20a01c620d209a6e1b961b5cccc66d8bb290`  
		Last Modified: Thu, 05 Sep 2024 06:06:14 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e637201b2f3e331cf9757c03446a0db1dd4eacf55241e53a710b7e468b579a`  
		Last Modified: Thu, 05 Sep 2024 06:06:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b92c81fe1194fc3ba36c3558b9317d872a4656e7bfe626e96f0bbcc22cb6db`  
		Last Modified: Thu, 05 Sep 2024 06:06:15 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d9bacd00d368b0e303aa4bb20fd430929b4af0e5c2e3547f5185c35a75359`  
		Last Modified: Thu, 05 Sep 2024 06:06:15 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b126953102a902926677c5965fc14af385bd25181d9425f0542f23e034b16218`  
		Last Modified: Thu, 05 Sep 2024 06:06:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:85380f3a4c9062b609a7904dd8acdbcb89bbb8d19ba60f6af5eb30accf8caa92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6079583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c731b9461e0b7e7c51f374c58866809d742ae6c7ab79a7492416e5c683d2e6b`

```dockerfile
```

-	Layers:
	-	`sha256:783e0c8b73083727e4427419d8bf44926662700b861da9dd2cced48d3480b8e0`  
		Last Modified: Thu, 05 Sep 2024 06:06:13 GMT  
		Size: 6.0 MB (6025837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aa4d2cd2d907035795e83ae2dd8710125d570c1ffc84504dd9c2a8a4528c137`  
		Last Modified: Thu, 05 Sep 2024 06:06:12 GMT  
		Size: 53.7 KB (53746 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:22421c64d607a78343a41ebf7ec46582e3a9d210b4cd0344df9e647e6e5350d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134084369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cefdf8e3d3b1e226d236d51ba52d46d5cd2bea0851b7ee59ff94188c65e11f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:c451ece1244c14bce110ffbe6906867ce12f8e88234988b0edba91009a9dbbf8 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg110+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f572303598915f7fb61cc4b47f7207c9ee64d52b9db5fc03ee133ec2dd679347`  
		Last Modified: Wed, 04 Sep 2024 22:02:25 GMT  
		Size: 26.6 MB (26589615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5e9c606d8528311a46a30cb82519938c43b33c4e1f31162ab88efcc0dd0f15`  
		Last Modified: Thu, 05 Sep 2024 07:11:28 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2970a29d8de911f08d48442531c9307bf0ae742938b71d029a754342b919a541`  
		Last Modified: Thu, 05 Sep 2024 07:11:29 GMT  
		Size: 3.6 MB (3601649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66db6d98ea73837923d726df3338ff4973e9c5bd1b7514f22394af905dd9b4`  
		Last Modified: Thu, 05 Sep 2024 07:11:29 GMT  
		Size: 1.4 MB (1439215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770e958c632b7100f93874e6d8edcf6a0e7bfebd2df344b16f5d3ec2a0f0f714`  
		Last Modified: Thu, 05 Sep 2024 07:11:29 GMT  
		Size: 8.0 MB (8044293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c42f090ffe7dc7637ee220b14061287b2fc4c983da82a663fcd24defc85954`  
		Last Modified: Thu, 05 Sep 2024 07:11:30 GMT  
		Size: 908.6 KB (908647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9846d37a8dad8e0ac73680041abcd9790c9deee18bc1d3cdc6986e340820abf`  
		Last Modified: Thu, 05 Sep 2024 07:11:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b909d375e13dbdd2a339a93e951b8c697bb1f0a9622446bdac7ce891a6eba51`  
		Last Modified: Thu, 05 Sep 2024 07:11:30 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69edf4e7b47047fc29db03c6820a20c6d8b477f7ab7f52b6d39922a37bc6da8b`  
		Last Modified: Thu, 05 Sep 2024 07:11:33 GMT  
		Size: 93.5 MB (93479873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79399f440b473552f96fb00d3c208e124e086165e78960ced352aded3c80c194`  
		Last Modified: Thu, 05 Sep 2024 07:11:31 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9ae2f81d139b3e33d75a68bd8d122917e26118a47632977f4cb7daa168d7de`  
		Last Modified: Thu, 05 Sep 2024 07:11:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb3e451c679c83954ab6044cfb73a239568595d2475104d9d47e764c049b512`  
		Last Modified: Thu, 05 Sep 2024 07:11:31 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5ce77cb9d9bf1cfb61d4850061c1b46e9bca12ee2e92a25ac30b379135ec99`  
		Last Modified: Thu, 05 Sep 2024 07:11:32 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c8246a095695cb577804671fcf3055b1b0ec27def3bb82064dbe3c155e4393`  
		Last Modified: Thu, 05 Sep 2024 07:11:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:eab9bc5708b0701b6b747822eb107a58002197d1cd4d63950f11f43a863dcd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6079203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e5e33663030a739dc88f84ce462b552a08b88e4b3f413e9d43ca0ac7d8bbb0`

```dockerfile
```

-	Layers:
	-	`sha256:b7871c282c711658cb3d4c6d197ce9cdd4692e498cd6bb2cba503f082deffafc`  
		Last Modified: Thu, 05 Sep 2024 07:11:29 GMT  
		Size: 6.0 MB (6025466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a726b0d38459c10ae9d07793b3141c0421d5c6eff5ce8ea2aed9ca7799e131`  
		Last Modified: Thu, 05 Sep 2024 07:11:28 GMT  
		Size: 53.7 KB (53737 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:4189849c8c00461c892a6aebfcb7c00500ee4b78ef993b389c53e1d6cf333af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142481265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68e5f49279ae669277e11255c7c6b0edf962a2aa98353e9de6a37515e3c7b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg110+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b5d412b788418a26c749ece91b8e7ac6ff9bcda7946ac505000020ce874ee4`  
		Last Modified: Tue, 13 Aug 2024 09:31:49 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df90a302ac3f2158eaeea4cc0d7c1af8d1460928f53720a4e94bf1f96c04329`  
		Last Modified: Tue, 13 Aug 2024 09:31:49 GMT  
		Size: 4.3 MB (4312699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719ce726d4b261e8b67a342dcdc873a3ff082d9d484a6cb6a78a41c493efdc20`  
		Last Modified: Tue, 13 Aug 2024 09:31:49 GMT  
		Size: 1.4 MB (1404075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de0a6ac2622147d99a288c1020d29ac9efba186ed374e3e3ccf225f0f260024`  
		Last Modified: Tue, 13 Aug 2024 09:31:50 GMT  
		Size: 8.0 MB (8044582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda4efc98a15c9556da46f3cbac14434688d0acb36734583809081bac67f435c`  
		Last Modified: Tue, 13 Aug 2024 09:31:50 GMT  
		Size: 1.0 MB (1026602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8835b2e7973ef5b2667407cd3420695492a7c1f9c80d56279f31d3ae89c566`  
		Last Modified: Tue, 13 Aug 2024 09:31:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148b60d389b32772b626b63199e1c7bf4d46939e7423f4adaa73d2c7de9d526a`  
		Last Modified: Tue, 13 Aug 2024 09:31:50 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21697ddf5bb32aa9e72a80ddaef750ebc734350bd287f5c4e174980e6c0ecf5`  
		Last Modified: Tue, 13 Aug 2024 09:31:54 GMT  
		Size: 97.6 MB (97596142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babcff0d4dd0da2eb43025d53e6044aeff6bb7a1c000c914e4a24ba346501705`  
		Last Modified: Tue, 13 Aug 2024 09:31:51 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b7ad6fc0de56b313829c4b1f031c054f62d592b3ac715f69cd2dffb423070b`  
		Last Modified: Tue, 13 Aug 2024 09:31:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083f05145fa0688d8d4c07113ac0800c706f3170709db7fcf605c52f9bf16801`  
		Last Modified: Tue, 13 Aug 2024 09:31:51 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad8be46cec6f1084d02b126e931c5de20d6c6c0852f20c4efac997ca585f4a9`  
		Last Modified: Tue, 13 Aug 2024 09:31:52 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df78787fcb6902b4d7aa942f115faa7e66e21933debd25c92e52022f89f5fa6b`  
		Last Modified: Tue, 13 Aug 2024 09:31:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:fb2bc5c153a94d75dbc56f5b5217a41a015d2232ef58445ceefc64d32c888dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6068567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029468a69fdeaa25c4d584effba8fff9be4a0a401825078c0148f491c2d40499`

```dockerfile
```

-	Layers:
	-	`sha256:4161fcd588c118e69997ac06ccd4ec9df16e07fa5a615f7df5378c6cda9139fa`  
		Last Modified: Tue, 13 Aug 2024 09:31:50 GMT  
		Size: 6.0 MB (6014737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aaf7c5462d0c8130034ca3cd9bb4938691c6e3ed438f90e4e19e9f4eb80fc23`  
		Last Modified: Tue, 13 Aug 2024 09:31:49 GMT  
		Size: 53.8 KB (53830 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:7104a9aab891138af71c233b26a79d9cc5fb591cb11ce728a07699b6c84f1c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.9 MB (148875453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a719fcd775dbc1436d452c6d6133da7272f16b67be75bc9d0560db2b48e15796`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:9177ff00c3abd0afc64f577295a060d88f4daed1042f024f7cfcfcd8cb1da9b8 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg110+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2e34c6adf259f6e5265d64b5a01b92c3cc93548f22be8c1ccc578b7e9babb30c`  
		Last Modified: Wed, 04 Sep 2024 22:48:51 GMT  
		Size: 32.4 MB (32413314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc40cd00afc6ee6f5bf0816240de4800ab5e9efa834f3b660ce0489b6173de`  
		Last Modified: Thu, 05 Sep 2024 00:21:15 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597d7b1e8ac2a00758820158f2c6fc2c9839aa052b49898253568a92939b39f8`  
		Last Modified: Thu, 05 Sep 2024 00:21:16 GMT  
		Size: 4.7 MB (4719567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fcd32d87e4695c1e5f9f7afc9870fe1253d5181a5eccef160c11c8b2a6cf15`  
		Last Modified: Thu, 05 Sep 2024 00:21:15 GMT  
		Size: 1.4 MB (1447770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0df096b8d516b5998db2613198e637e65ef1c6bc6ab9c9d5d3b3c621e30391`  
		Last Modified: Thu, 05 Sep 2024 00:21:16 GMT  
		Size: 8.0 MB (8044289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc1eb662f71da1d4f5f789851d0d6fcda5cd4cdc6a3b95530842fbe965b598`  
		Last Modified: Thu, 05 Sep 2024 00:21:16 GMT  
		Size: 1.0 MB (1028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca037820180c50747624b9d208a750047b4856f0753d9fbac2016a814b313b3`  
		Last Modified: Thu, 05 Sep 2024 00:21:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a849b91059246828a930ac5f34fdf31ddcfe06f42d02869ce968578c0aa3072`  
		Last Modified: Thu, 05 Sep 2024 00:21:16 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73137d9d033126f174e9a6f9afa82bcc9daa5a32c4d23eaf3b85d66a3cc90cbc`  
		Last Modified: Thu, 05 Sep 2024 00:21:20 GMT  
		Size: 101.2 MB (101200530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0b3c9490e72d3d453abc66573c596d24515bd33481ba46ba5667f759f70ce8`  
		Last Modified: Thu, 05 Sep 2024 00:21:17 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6783ae8e33792fa65da96431c0883f61968ac453c9c9d82c1bb67c1e2a208ff`  
		Last Modified: Thu, 05 Sep 2024 00:20:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f067dc43cdae548e7a86025d5c4fe15aaebf787bc5899a99c9959f6b43d3c296`  
		Last Modified: Thu, 05 Sep 2024 00:21:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba5cd35637378b65fab33ea1b80921364fc81c9bf8d79fc800d015119600ea1`  
		Last Modified: Thu, 05 Sep 2024 00:21:17 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0cab91c8d54274bd06cc3e105bcefd86d61a9a26a7e8fec34e548d198caac5`  
		Last Modified: Thu, 05 Sep 2024 00:21:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b7a7b74660b917ba38b893668c8c583ca1b4726941a47aa51158be3d58d18956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9163705af9c03bcdffb267cd9c64c0c3ef5e6bb7664c9e8a34c6bcd0d5c2be`

```dockerfile
```

-	Layers:
	-	`sha256:6423e86ea137aa7a1758bfb08416b52bba791e0c2b153291814fd97cbf48b16f`  
		Last Modified: Thu, 05 Sep 2024 00:21:16 GMT  
		Size: 6.0 MB (6023170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9e14e12b3fb26b77df16e94896d204c89bf50d3238717cce6fe5d473702ea8`  
		Last Modified: Thu, 05 Sep 2024 00:21:15 GMT  
		Size: 53.5 KB (53526 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:dd9bf3fdd5f4ee3df4df69a71e8a3655b23d231f69d6ce8d57c12fc40d9a1288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140429939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9b0f15e2e5fb1d222acdea8218876e080994c319927bddd8fcdf839eb7a21a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:d4b92daa2701c7af077c4c89b2b1f5a97cfc6389c09e049b3bdaa36454653bbd in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg110+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:15b8bd5d9ec350cbe23bbccddd5284b3cc9139e037500a63a02025354518d5c8`  
		Last Modified: Tue, 13 Aug 2024 00:23:52 GMT  
		Size: 29.6 MB (29646095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8756e4bf324c450320a08e19331208ae564f36a011174c89af8cb49a53f60c21`  
		Last Modified: Wed, 14 Aug 2024 06:08:12 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80efd2830b090c4732a7cdc9cc81ab571e02a44d3d1437948c71657571e9925a`  
		Last Modified: Wed, 14 Aug 2024 06:08:12 GMT  
		Size: 4.3 MB (4308324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc775a138ac985753fc78bfa32a171a019ed026a41738516b80442dcb0bf0b18`  
		Last Modified: Wed, 14 Aug 2024 06:08:12 GMT  
		Size: 1.4 MB (1359373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd6a47bae0895d43a00e4068c39d18d5630c457b64a3370f0f96284bb42423d`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 8.0 MB (8044717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aae077fa3abd7258a46d4e7c2e634a6f65e59687ca05718c7c1736b0a65ce9`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 1.1 MB (1090275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb13c1ba77f878e041e12823e8b6dc6ea9d93bd7ecab70a97d379b65f470109`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a98d98bab3c64f344d2e50547954cbd619d9e47596137358497a0ae3457d01`  
		Last Modified: Wed, 14 Aug 2024 06:08:13 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246808e6e9a018524542dbddb4a999dc20049671394b76a9a3accc1ba410be82`  
		Last Modified: Wed, 14 Aug 2024 06:08:23 GMT  
		Size: 96.0 MB (95960065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294dce5b5e0c2f1832eff074a08591cb466cbbd3c38fea63847deea82d545624`  
		Last Modified: Wed, 14 Aug 2024 06:08:14 GMT  
		Size: 10.2 KB (10246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb981bc0055e0181702690b80e8c718352bdd913b5a47ea11ebe9a67c3546d7`  
		Last Modified: Wed, 14 Aug 2024 06:08:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c0d4261045d5309393a1847625289c1ba745cc90be09918eeee1089ed09a63`  
		Last Modified: Wed, 14 Aug 2024 06:08:15 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97203f089f9b09ab04810d6c5da5f8e223e82d96193d4291fc93657158bd0e04`  
		Last Modified: Wed, 14 Aug 2024 06:08:15 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fde02cceea08d8eea672ca9913a597ec015c5b2ea3aef3eb5a2aaa5b9bf665`  
		Last Modified: Wed, 14 Aug 2024 06:08:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:4ce31181bd13d2ecb550e60f2123dac51145bd8cab45f315ce4cd1938fcc6bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 KB (53401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b24f1bed986f6d7e624577f174b64760a4d7119b944c6c1261af77baec2eb1`

```dockerfile
```

-	Layers:
	-	`sha256:57a5da0d311de984a5f6881afd67dc380b690c71c78d0d5508c79680dea165ec`  
		Last Modified: Wed, 14 Aug 2024 06:08:12 GMT  
		Size: 53.4 KB (53401 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:989a59878ed174d3a236b5b90d3742ce9266d0340cdd8c60182ffbd250538a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157131296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ad0d9401560df3c181f9918d7f5c949348c47ccabf5c28c13f5af15befd3c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:1dd1fe717176cf8c20fe5b4fd39ce7f79d39d2aec08c436f3ade914e61d5d17b in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg110+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:713e780b10a0e4075bf4372f97f67566ba30b5cc32dd0bf565177796f5503d7b`  
		Last Modified: Wed, 04 Sep 2024 22:30:58 GMT  
		Size: 35.3 MB (35299274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb03920874bebaac0313c066da6e1292d051b9bdbd1123d8de0e41a668ccb72e`  
		Last Modified: Thu, 05 Sep 2024 03:12:11 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac3e8856a34a137abae04f17f55e1b3d6a2886709cab091647f4fef7897631a`  
		Last Modified: Thu, 05 Sep 2024 03:12:12 GMT  
		Size: 5.1 MB (5137806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadd44eafb3401af71118033b6cb1bb2e472a4eab258f5ebe20b1b035cbf2d4b`  
		Last Modified: Thu, 05 Sep 2024 03:12:12 GMT  
		Size: 1.4 MB (1393635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae1bc84e0e01888ba16e6babb838cd471e00ecaf928ea1e7beef6406a4b936f`  
		Last Modified: Thu, 05 Sep 2024 03:12:12 GMT  
		Size: 8.0 MB (8044494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db835f9f21dfc6fca2b1aa1d9ed5199d68a03bf4a8742ffe7bc912bee54c791`  
		Last Modified: Thu, 05 Sep 2024 03:12:13 GMT  
		Size: 1.2 MB (1197541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8cb26e1532c0e800af9f9dd22391dda36b40c2d8934633184af9cea8decbe`  
		Last Modified: Thu, 05 Sep 2024 03:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a67336446e997e452360d45b8b18e766a00beff49071b72280c2101482cb427`  
		Last Modified: Thu, 05 Sep 2024 03:12:13 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1171852e9a3a48dfa0af8c1dd0279bedf9c7a5b916c5649daafe44c10f125949`  
		Last Modified: Thu, 05 Sep 2024 03:12:16 GMT  
		Size: 106.0 MB (106037461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa2a893af942ba5e1077e63053d9dac3fd6ee3fdc15ac600b4988eacbcc451d`  
		Last Modified: Thu, 05 Sep 2024 03:12:14 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa77be38d6c90c6d13014b582e2cd54beb86817abca0c1654eab89b08043d95`  
		Last Modified: Thu, 05 Sep 2024 03:12:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a00a763ca308dd9f3f2b834de9c72d4ae610555c29178cd48230989eb29db8`  
		Last Modified: Thu, 05 Sep 2024 03:12:14 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c11d705ce97410d12efd11eea8611b7ea9ac826329c5fcdff38ce97fba6630`  
		Last Modified: Thu, 05 Sep 2024 03:12:15 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e9eda37b4a472e3e897efa3f3e6cb9b0e8a58ff23f1bcb77e95d35c36e65bf`  
		Last Modified: Thu, 05 Sep 2024 03:12:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:0448ab81eb7a6bb22f6dd1ad5cc49f8fb380afe2f57fefbfc68b083573ccdc01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6069190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa258ba560b0a2da42e589de8781b2635643d13c1b7e6624814d738277505937`

```dockerfile
```

-	Layers:
	-	`sha256:28602d29e18d895ade6a942038390554f416c9b1ce49d63be4f6f61179c43358`  
		Last Modified: Thu, 05 Sep 2024 03:12:12 GMT  
		Size: 6.0 MB (6015585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9584845f5bf9316d73ca62fd3c8a4887b49cc3fba25e6d84c48adf67607ddcdc`  
		Last Modified: Thu, 05 Sep 2024 03:12:11 GMT  
		Size: 53.6 KB (53605 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta3-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:addb78d56d34d0227e3f6da992e7dad1b822fa3c07eeef3567680b8d91bc6b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150485606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b40a307fe071113f3eaadf615a71b9caeba4e9cf376c5cc8a91040616224fc2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:34:59 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_MAJOR=17
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PG_VERSION=17~beta3-1.pgdg110+1
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:34:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:34:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:34:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:34:59 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:34:59 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:34:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa74617b6306779ebd9fe52758d2400e81a4c82d80b8c0dd2d87dc02c9187ef`  
		Last Modified: Thu, 05 Sep 2024 05:05:36 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95d1b5d7b1f1d66b6dcf47f49733f151a45df9fc346b7fb40c378aebc629f4a`  
		Last Modified: Thu, 05 Sep 2024 05:05:36 GMT  
		Size: 4.2 MB (4200347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69982ab84b3d7a587c8efaadc9f9082799de1c9183067e379dfb94e9a77af86`  
		Last Modified: Thu, 05 Sep 2024 05:05:36 GMT  
		Size: 1.4 MB (1437973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0ab37ef9cd03d0f26514d5b7d51f3ff5b8c87dd84895233863040b15a688dc`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 8.1 MB (8098858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29c31483b2b4e9ac50de84964c4b8c92a50c4939ac41224cd8fbde23826d786`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 1.0 MB (1015252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41e8be03ee08a804c131ea8a9344f92b2d99929f458b23e9745b939edcb267a`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddf8031b775ba82af170e0d5e20c4cf9b27c8e7e983ce8e74a142542dffa1a7`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d539fd081148cad27975478d7ebccf77a0d9f906bb0e66d797f9861a186eab`  
		Last Modified: Thu, 05 Sep 2024 05:05:39 GMT  
		Size: 106.0 MB (106048638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98accda239e01d49ddd7e8c36eb3a2175bd905bc3830d665cc496989f4afca7d`  
		Last Modified: Thu, 05 Sep 2024 05:05:38 GMT  
		Size: 10.2 KB (10250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b87305afbc47f089e689404998ad30ae9fc1ab727e97f4f3608a12feccbe3e`  
		Last Modified: Thu, 05 Sep 2024 05:05:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8e866eefaa5d125365972fb7387e7343f6b817a76d9e75e720fc8cd5c5c52b`  
		Last Modified: Thu, 05 Sep 2024 05:05:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1419cdb21250fd2181c335ccaeb1bdb2db6a4b918426d6e6680c1a0f99b42a`  
		Last Modified: Thu, 05 Sep 2024 05:05:39 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939eb53ed4bb4046427f0f6a5b152005524ef2961085f2adbbceac14afe8e634`  
		Last Modified: Thu, 05 Sep 2024 05:05:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta3-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e9434d7df279f9a93d235b23ecd7e8fd8906d957682b41ccb0455ede600324cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5252cf325f28be3ec31e201c9c82f6d5f49c1c3c088ec5b868a9b7126041b2`

```dockerfile
```

-	Layers:
	-	`sha256:6f31650eccbc0406fff96257f65483b690393fa42a84cc73be89abca465d3ddd`  
		Last Modified: Thu, 05 Sep 2024 05:05:37 GMT  
		Size: 6.0 MB (6007436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65a377fd4696380148dfaf44f9023eaaed79395ab00cc93a0e45d4da777d98fe`  
		Last Modified: Thu, 05 Sep 2024 05:05:36 GMT  
		Size: 53.6 KB (53563 bytes)  
		MIME: application/vnd.in-toto+json
