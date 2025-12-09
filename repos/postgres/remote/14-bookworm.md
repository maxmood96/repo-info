## `postgres:14-bookworm`

```console
$ docker pull postgres@sha256:e8bf6e7baad56d3c1e16800b6aa6fb351dc1fded7454c2b23efe51537f615ca7
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

### `postgres:14-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:1feb2e230ea8733ecdca18a071fe86ab8f6f07ec497fc4b94578325b715f7888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151837284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2da70b0f3485f43e7edac1788c06a02345a46cad5542439c2f2f1b8b3e31a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:03:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:04:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:04:10 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:04:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:04:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:04:14 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:04:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:04:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:04:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:04:18 GMT
ENV PG_MAJOR=14
# Mon, 08 Dec 2025 23:04:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 08 Dec 2025 23:04:18 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Mon, 08 Dec 2025 23:04:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Dec 2025 23:04:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Dec 2025 23:04:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:04:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:04:30 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:04:30 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:04:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175e35ad51485f2b0c0774d4abd1159c2651baf0e6f1f876fbf4fd9a8a7e2212`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e98491a8719ccd80a6b5e865988988f0d9a9bfce91eac413d1c5354ac865c2`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 4.5 MB (4534049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86883bb8eccb275152cc7a60601b91591a0cec73a694b9f601c931e734355775`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 1.2 MB (1249482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34da9dda593d159390ba9f021767582fee5642db385c1fd3557e7b15ac025d1c`  
		Last Modified: Mon, 08 Dec 2025 23:05:00 GMT  
		Size: 8.1 MB (8066432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2e42ce8f900b36a0b985dbef14ccfcfd3066f9a1c24cc05466d7aaeabfa127`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 1.2 MB (1196382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6675c1e8d7a229e25a90c6ee87a922b54a7f109ccd7a1c3f195c7ebc272b75`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f614d079acc26acfefd742eacdb828ad201904576ab027ea3ca605fca592a6`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3deb1843ae93ef6dc91cfab4036186b2365d2ba130b513c2365dc4dfcbebe513`  
		Last Modified: Mon, 08 Dec 2025 23:05:12 GMT  
		Size: 108.5 MB (108542256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e2c76da5f97fd49c5c7900e4f12604e397da4ee4ea6ec47882c5504cdc8f91`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3faf205ebeb0684f3429d4f11033652391aa934b46f5128d2a3c8d24d10b937d`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60122d9a8ed686e66474b3f90ace3cf8956279b83b5a514bdfcbafbe346c606`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ea23fd4804a5d1be39cc921b2afcf33747cdf3d752d10c800978109625c363`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcae598a180bdba0101885378df83b3ef920e96f9222c3e7b9a9d7c15875017`  
		Last Modified: Mon, 08 Dec 2025 23:04:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c08788b4a0d3686c7cec6747723bd76e7946502ecab9221cf5e99c06ac76be1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5846131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75a5b1162e658ce990c9861718568ad01f241b76acb7df3fead12329657b670`

```dockerfile
```

-	Layers:
	-	`sha256:09a5f50e164df035c5c942db15344a0f191f230495416d4f11a8bd91c4a70b75`  
		Last Modified: Tue, 09 Dec 2025 00:07:58 GMT  
		Size: 5.8 MB (5792835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feca3d485ae59d6f0f112d5b8b15f4b920a5935c66bbc25a6693c0c4531dbea`  
		Last Modified: Tue, 09 Dec 2025 00:07:59 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:54decf8e2074eefb391f56ef891f8932745fb7f5a33ee5d3efe241f7961154ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144795588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb3f6cfcbe537f1355d8a1c8c403708a13a7c5cba0d0abd41f6af64c6e47165`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:37:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:38:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:38:11 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:38:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:38:18 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:38:18 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:38:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:38:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:38:24 GMT
ENV PG_MAJOR=14
# Mon, 08 Dec 2025 23:38:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 08 Dec 2025 23:38:24 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Mon, 08 Dec 2025 23:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Dec 2025 23:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Dec 2025 23:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Dec 2025 23:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:52:20 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:20ca79728ab9e4eb574872cf271bd965c51cf4e8ac84660ef17b281a3aeb750e`  
		Last Modified: Mon, 08 Dec 2025 22:16:26 GMT  
		Size: 25.8 MB (25757588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f497f3e6f0b2f8dd6b03ba629018dccb0bec1a42842ef35f6e169e06f87e36`  
		Last Modified: Mon, 08 Dec 2025 23:52:49 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512ab84c681b8f107e56f0d1cfae97cfe3e05240ed8a25aa8540b185d8d5bf9d`  
		Last Modified: Mon, 08 Dec 2025 23:52:49 GMT  
		Size: 4.2 MB (4151206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698620e10d471dca055c3a6465260fb787ba601d808ed3c4732ec8298fae0b5d`  
		Last Modified: Mon, 08 Dec 2025 23:52:49 GMT  
		Size: 1.2 MB (1220048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d6cc3d77fc6c784751693901c70f80c3456a04eba6b1f78a619ae99e0e14b5`  
		Last Modified: Mon, 08 Dec 2025 23:52:51 GMT  
		Size: 8.1 MB (8066538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87bc52e446c93af57b9702e4a6c7ac59f4441f3ddce2e32bea03a570ac564a`  
		Last Modified: Mon, 08 Dec 2025 23:52:49 GMT  
		Size: 1.2 MB (1195008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f7b1521a914419dfd1788a61c18c9a23be8b604a755c778be55889c22f4dc5`  
		Last Modified: Mon, 08 Dec 2025 23:52:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa4bd8f364703f99327d94309aee47cec18bb93b92f0164f3179df6299d5aea`  
		Last Modified: Mon, 08 Dec 2025 23:52:49 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c62b2530b211bb5bfd79980503de1a1ca955a020fff3fa78f25ae1ab86a796`  
		Last Modified: Mon, 08 Dec 2025 23:52:58 GMT  
		Size: 104.4 MB (104384933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660dc6cdf385c5445c5e7de8da786bf2ec94525340235ba96bfcf71999156d47`  
		Last Modified: Mon, 08 Dec 2025 23:52:49 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82cdf1ae48f7b51e87006a4383163546ca92cd429c4c147247dac6574684afe`  
		Last Modified: Mon, 08 Dec 2025 23:52:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3788c95053e9dfc36ff0077726a80784b4bbdf37fdc79943a2281cdfda65745e`  
		Last Modified: Mon, 08 Dec 2025 23:52:50 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dd8d08f772239174622da3b95316b2311fa99ab4f912a5851dd6aa399f9605`  
		Last Modified: Mon, 08 Dec 2025 23:52:50 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93e5fa12fd0e6f57ffe32a8d1ab01c0ff2e71883a4c9b7e9d05637a954bd5f6`  
		Last Modified: Mon, 08 Dec 2025 23:52:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:91a47e30f25f849c06fd0e2fa3ca507692190e5a6e98d268bef6e90b7922b5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5862162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c36dfd209bd245526bfdfefb223e3a8ab1d9687f35fbcf557f684843ba85744`

```dockerfile
```

-	Layers:
	-	`sha256:30074c67134e47b61cc957c02fc82ae3d9d634bc0065aaeddc40b7896a5941d1`  
		Last Modified: Tue, 09 Dec 2025 03:08:18 GMT  
		Size: 5.8 MB (5808660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b52fe7f85bc8159821197c0569770b4a088c47bfb535117021d0b5e3e175fc8`  
		Last Modified: Tue, 09 Dec 2025 03:08:19 GMT  
		Size: 53.5 KB (53502 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:58dab8de4f548e7c8655935fef9a007ece36ee94f77d3a358715532fbd61eb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139891758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce66bff10ade906141c7c77cfea502c209ee67568e50d809660c9c60bb255c58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:37:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:37:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:37:43 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:37:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:37:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:37:49 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:37:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:37:53 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:37:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:37:53 GMT
ENV PG_MAJOR=14
# Mon, 08 Dec 2025 23:37:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 08 Dec 2025 23:37:53 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 09 Dec 2025 00:05:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 00:05:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 00:05:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 00:05:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 09 Dec 2025 00:05:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 09 Dec 2025 00:05:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 09 Dec 2025 00:05:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:05:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 00:05:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:05:05 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 00:05:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 00:05:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916e1e2b574d48fe4d17f2f55f051c3988982922f58e684856670a96f50b769`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75dab41cf845ddd0bd6e2c34218d17e76608688c0ced571bd269218c398e0ba`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 3.7 MB (3742630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa83cd5fe8e42a34ce0c73df78aec82f551ec252065b519337d9dd19215072fe`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 1.2 MB (1215981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef887ac3389d563e6a40761a6728cfb36b37817d3626e896ad4e10d8d112a7`  
		Last Modified: Mon, 08 Dec 2025 23:50:25 GMT  
		Size: 8.1 MB (8066389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2abc2551a12c2667538fc5875c67271ddcfe2dec7443e9900cf522541bea67`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 1.1 MB (1067258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4d39907f8def56f25bb21bb52ae2d36a8e01c66adf27ff82ee957671f18e9`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d205946325bda99bed307f89b84c0093bd90eea13899ba4707bc2716a4870634`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c4e4b59c575bac996b6ae56534f78597c0a2b046a0f99e3b51544c9a6e16cd`  
		Last Modified: Tue, 09 Dec 2025 00:05:46 GMT  
		Size: 101.8 MB (101845221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e0388c79b9cc41ead5f046e744ffe4c6bbd796df2467455b78686be7cd819d`  
		Last Modified: Tue, 09 Dec 2025 00:05:39 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e016684526bde09505b3ada3777cbbb270a652193e037110e74bf448d1fb799b`  
		Last Modified: Tue, 09 Dec 2025 00:05:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd1caf5892d7757ecef16083a0d98d6b8a9d503ebc370287b554fb9d163e73f`  
		Last Modified: Tue, 09 Dec 2025 00:05:37 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8519f246d6d2f813a258e5f7cbd7460d6e6a77d133ad8f54574b8250f8a059`  
		Last Modified: Tue, 09 Dec 2025 00:05:38 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1059c4821a96b3971808bb658f5a6d6618917ed844a74265651f94ee742c43c`  
		Last Modified: Tue, 09 Dec 2025 00:05:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:83420feaca775cb36cf22b7a8878ec67431e1f6e0ae01972addd4ab7c3cea5c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5861418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda2fd55f7c4a78e566d0745bfc099aea403396d49ad9a3d2a59e4162d84c76f`

```dockerfile
```

-	Layers:
	-	`sha256:d74be3ee743eecc33847383580bd0fda347ed118a1fbd52bdc92dba960855000`  
		Last Modified: Tue, 09 Dec 2025 03:08:24 GMT  
		Size: 5.8 MB (5807915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb5f591fe8c86ce68bda6c037cbd7df16ae8493754980f790f33f7cb24dccc3e`  
		Last Modified: Tue, 09 Dec 2025 03:08:25 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:bf4184d47a7bea40ba639f10c5ddd6a2b9b51f029fd16e4cd59018c9a8f5b3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149839334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d289368d48f962bb911ac423ccdf82c17bb5e9529f37ca7c549332f6c9618d60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:07:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:07:27 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:07:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:07:32 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:07:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:07:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:07:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:07:35 GMT
ENV PG_MAJOR=14
# Mon, 08 Dec 2025 23:07:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 08 Dec 2025 23:07:35 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Mon, 08 Dec 2025 23:07:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:07:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:07:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:07:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Dec 2025 23:07:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Dec 2025 23:07:47 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Dec 2025 23:07:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:07:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:07:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:07:47 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:07:47 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:07:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3b7e397dfd085c693484a5cfb8f826cf8101ac86ddfdcc24da9326e14e4fe0`  
		Last Modified: Mon, 08 Dec 2025 23:08:16 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4865fdb8e393708525b0540021a278c606b088b128ef6c1e090832a4c8dca33`  
		Last Modified: Mon, 08 Dec 2025 23:08:17 GMT  
		Size: 4.5 MB (4519894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9c73e45d4fe3ae191f93e3f0ccd7068d8045b4519ac4734000e821339de63d`  
		Last Modified: Mon, 08 Dec 2025 23:08:16 GMT  
		Size: 1.2 MB (1203297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb8177a125ce80425229cedd1053b05ff5094e2232353acc64e5f4da516432e`  
		Last Modified: Mon, 08 Dec 2025 23:08:17 GMT  
		Size: 8.1 MB (8066469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8380fb9f0b16943d8c8bb96dc6aa1707aa798e43f4e594d3b60b1fe4586fc0da`  
		Last Modified: Mon, 08 Dec 2025 23:08:16 GMT  
		Size: 1.1 MB (1108959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f938cde75f81daf673f233d495a8973cc33ade130b99ad71d6a95d69fd4e00c4`  
		Last Modified: Mon, 08 Dec 2025 23:08:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496c1edb598c67f2471bc59e0f60cd2ec83aef6911f60f6764a109096ca4309c`  
		Last Modified: Mon, 08 Dec 2025 23:08:16 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf614dea6db09d84372f4017e45a1624d777d51daccb67bed36f25b7663b2032`  
		Last Modified: Mon, 08 Dec 2025 23:08:26 GMT  
		Size: 106.8 MB (106818227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b326edc7e79c5e6a18e7d4f49c313d63e8c135979e2ba62fd233c080dca36`  
		Last Modified: Mon, 08 Dec 2025 23:08:16 GMT  
		Size: 9.5 KB (9523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200df20d44189de97693024f235db1c4114c95ad7f5062256cb0dedf1576764a`  
		Last Modified: Mon, 08 Dec 2025 23:08:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72a5f3611078dc6bac1549315b34d655e5cb7b349cc2120a2f6976af1a4bd99`  
		Last Modified: Mon, 08 Dec 2025 23:08:16 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3defef5e94a6b2c96b81da961d892a0ed5426312147f202b459facdc50f45319`  
		Last Modified: Mon, 08 Dec 2025 23:08:16 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6f58e3ba6a3a3084158373cf4b5c37c65f8fbfe32163ace1aca2a251a6bc1b`  
		Last Modified: Mon, 08 Dec 2025 23:08:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f4fdd1f35ca3fa4510f00217a4735b6b984b81a5148b026cff0629fa8f319d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5852687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b876040c488f86258825646a695f0949b5e7228d0c48c8834da95b587f9c97f9`

```dockerfile
```

-	Layers:
	-	`sha256:0271a8fc0fc98516dc4f238183399aed15c229caf400bac192f9a26caeba9c54`  
		Last Modified: Tue, 09 Dec 2025 00:08:13 GMT  
		Size: 5.8 MB (5799146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d2fa8306a029c476b183859fac5a520dd6a8148430c5c11119704272f71d4d`  
		Last Modified: Tue, 09 Dec 2025 00:08:14 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:1e90d9aab71aa16bd8912a8ff08068caff69279986677383c5c78c1dde644957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160518813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a158a1cf5317c2a4f42a1994ef3f5151f886cb05ace1adc411bf1f8486563a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:03:41 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:03:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:03:54 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:03:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:03:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:03:58 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:04:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:04:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:04:02 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:04:02 GMT
ENV PG_MAJOR=14
# Mon, 08 Dec 2025 23:04:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 08 Dec 2025 23:04:02 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Mon, 08 Dec 2025 23:14:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:14:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:14:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:14:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 08 Dec 2025 23:14:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Mon, 08 Dec 2025 23:14:25 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 08 Dec 2025 23:14:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:14:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:14:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:14:25 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:14:25 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:14:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc3fdf980f0bd0338b331f287ac0d6879024f83ba391de94e71d6fd6632fdf4`  
		Last Modified: Mon, 08 Dec 2025 23:14:55 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f8e28d67e27344e5685b8f25484ac815e184fa7a9571df8bcf4aa24da0b729`  
		Last Modified: Mon, 08 Dec 2025 23:14:55 GMT  
		Size: 5.0 MB (4965394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7eeb663ac3e315776fe4c4ad9ee443a11edf5e8f5859d7cd6e5854e299bb84`  
		Last Modified: Mon, 08 Dec 2025 23:14:55 GMT  
		Size: 1.2 MB (1218627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34277e6b7c5a6e3fd86b28c114f73a02b1c092ea6458c168460677a83491e041`  
		Last Modified: Mon, 08 Dec 2025 23:14:55 GMT  
		Size: 8.1 MB (8066428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4373a4b96382a1fa26013c0d943a1e1f051cbf20802c0b1ea4bcaf84e35d3585`  
		Last Modified: Mon, 08 Dec 2025 23:14:55 GMT  
		Size: 1.1 MB (1137437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f7394e26dde2b237f6805a6608efbd9aaeebbf3369af8820f6b932474573c9`  
		Last Modified: Mon, 08 Dec 2025 23:14:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cba849734cb768a1aa11a9071d5d9813aa0333413d85530759d5eda4ad4f076`  
		Last Modified: Mon, 08 Dec 2025 23:14:55 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2081b9799c3bdafce0ed15faf28a7b185e50591e617c0a74ee9e460caa0d33a0`  
		Last Modified: Mon, 08 Dec 2025 23:15:10 GMT  
		Size: 115.9 MB (115900928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c519e4c81aeb758098e5cd5d75501f5d294659138ed1e0c5642cedd42fa35c3`  
		Last Modified: Mon, 08 Dec 2025 23:14:55 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee7823278016756cbee0cba3039064cb68e5bf38cd6f97308ce1afd2b6e37f8`  
		Last Modified: Mon, 08 Dec 2025 23:14:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64620144e0ffcead110256a6467c0b6563684f9b4218b2f91a361ed5309f316`  
		Last Modified: Mon, 08 Dec 2025 23:14:56 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd1b4e99f55aa215d9a7ccf2ec9195cd1acd40601f7db26a8e9f1f4dc1fee9b`  
		Last Modified: Mon, 08 Dec 2025 23:14:56 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d61907eb86ff76476675cd9b0ec3bbf961ea32c8161c01df04ad257ca338ea6`  
		Last Modified: Mon, 08 Dec 2025 23:14:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:bb56ba379ef447c1885a4a491f7c088a934f5cdbe35c46819dd64fb70be25b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5860055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec328f220f10e33be9699ab661a2332eefdf9eb31de7874752c22c89933e0455`

```dockerfile
```

-	Layers:
	-	`sha256:6561551c443bc4dbf6cd4b94b9c0fe100dbfd489dabac47a8a3ce4799b4d3432`  
		Last Modified: Tue, 09 Dec 2025 03:08:33 GMT  
		Size: 5.8 MB (5806803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f354a89ce9846c47558308d63accb8225e3829f2c3a5eec2466001ffb63384f3`  
		Last Modified: Tue, 09 Dec 2025 03:08:34 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:680bfca39575273e8936b46a33b4f0d60de54e5b886d3f4385afbd05f28b2151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150644268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dc2c26997f48eb944aee3f1ef979e7c271901ccb1e6092ea0b667d99c4a0eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 08:35:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 09 Dec 2025 08:35:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 08:36:23 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 08:36:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 08:36:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 09 Dec 2025 08:36:48 GMT
ENV LANG=en_US.utf8
# Tue, 09 Dec 2025 08:37:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 08:37:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 09 Dec 2025 08:37:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 09 Dec 2025 08:37:09 GMT
ENV PG_MAJOR=14
# Tue, 09 Dec 2025 08:37:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 09 Dec 2025 08:37:09 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 09 Dec 2025 14:24:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 14:24:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 14:24:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 14:24:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 09 Dec 2025 14:24:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 09 Dec 2025 14:24:38 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 09 Dec 2025 14:24:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 14:24:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 14:24:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 14:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 14:24:42 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 14:24:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b2b054f3a77e8800c8f5fad5ed6594164acd9d6bbb1409af308aa485c7352cac`  
		Last Modified: Mon, 08 Dec 2025 22:15:08 GMT  
		Size: 28.5 MB (28513802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d47dc8acc85e561a2b57f777018cb1cea2c388e433fae54bb69a230e01e7bf6`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded2023525854da28133834b4d009a7b2461ff6da6a300aa50ca4e83bdc07201`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 4.5 MB (4475494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdccfe6df3d4b77476b8e6b837791063e36a5343f2741e514f74019e786b0da`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 1.2 MB (1159212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae81cada0dbdd36e2f3ce856568dd67817b9419e45715e907952c70b153112c2`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 8.1 MB (8066677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610dc6ee7fcf349dc925fcb88038f9c027d70deb2c0048dfcef02f4d0300fbe`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 1.2 MB (1182943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17a35b4a2a9c8c58153919fc2323fe2e2f2554ab27b544e125279494971f11d`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696281a9f2a21529623361fa823bf678235f4122aa4a80f78e7068017da7b04c`  
		Last Modified: Tue, 09 Dec 2025 09:50:43 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdb924c2c3cd6b2a67887fbac1cadd5b3729a1c34e397356f3490c1f08e5373`  
		Last Modified: Tue, 09 Dec 2025 14:27:04 GMT  
		Size: 107.2 MB (107225857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaf0d072b0f4bd7b36a7d0a2a71f89234dd58563eec534b210a8794f323751b`  
		Last Modified: Tue, 09 Dec 2025 14:26:56 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23774cea08ea5ebcb6a3a9d627eb2cfef80496753d968998929e1615451d0f97`  
		Last Modified: Tue, 09 Dec 2025 14:26:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3318cf5802e659de4b63479ecf700a59a7ff0d280c20ee2f91190a9106b94bbb`  
		Last Modified: Tue, 09 Dec 2025 14:26:56 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88839876e93caf7a09f6ba3094eb47e990c239cff15079705d446df28c3b7b6f`  
		Last Modified: Tue, 09 Dec 2025 14:26:56 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ecb465409cf95be8a043d85cf3ae05b543407bd38f011b98c3f95d7f254ee`  
		Last Modified: Tue, 09 Dec 2025 14:26:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e8c734884e97ff6901db41ca77ef7664577941cd45b8d481660f585b24c5eeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a622543fc4c7773ec2f65075a68ebcb678cf266f3492764f9b1ef00048c3f8c6`

```dockerfile
```

-	Layers:
	-	`sha256:8546cc124c12dfc55a7e0f425ac6d850b3428cc928683f0f4dfb53be6b2fda38`  
		Last Modified: Tue, 09 Dec 2025 18:07:54 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:eb9b17942fafb2c7b4feefd305edd65bfabc68e52f143a5d1b255d43a2a35edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164504973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d5fa925a415194ca9b4054a79e89f8c12bcec3d538cf74c8237132559887b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 14:06:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 09 Dec 2025 14:06:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:06:26 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 14:06:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 14:06:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 09 Dec 2025 14:06:35 GMT
ENV LANG=en_US.utf8
# Tue, 09 Dec 2025 14:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 14:06:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 09 Dec 2025 14:06:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 09 Dec 2025 14:06:42 GMT
ENV PG_MAJOR=14
# Tue, 09 Dec 2025 14:06:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 09 Dec 2025 14:06:42 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 09 Dec 2025 14:12:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 14:12:21 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 14:12:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 14:12:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 09 Dec 2025 14:12:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 09 Dec 2025 14:12:23 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 09 Dec 2025 14:12:23 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 14:12:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 14:12:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 14:12:24 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 14:12:24 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 14:12:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1242fbf5439ce7c9e3a77980c5b6e8bafeb45c33f149e270bb88cd9ec1f4c67e`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c53d034afcbdd6f654d9fe1aaeef703493ef065a5ae05bcada4329686328a6`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 5.4 MB (5368546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ed3cd8227300b056f550d1b12ae037f670a1985bdb9c38a6a073d9a0857a9`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 1.2 MB (1208196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ad4f65c6983b761b5dfcf5c82c2e08ea5816ce7aa74697b372208808f5d5ba`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 8.1 MB (8066521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abf9fe0835cfd8dd1de603db21ab5d44448a5232262d4dfd62b6a2e37ae0b81`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 1.3 MB (1283631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0185ec9f7edb70a06ffe3de0ec8b66fde15435a482585c9f9c2878586b3bf22f`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26d941e8b8881b4c06c365213698d3d5d5110a3d0a234b835f43b884d1b5b79`  
		Last Modified: Tue, 09 Dec 2025 14:08:34 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9640146cdffc00a79f24f6987e186c3511a96b4547003ad77afcd7b199c1245`  
		Last Modified: Tue, 09 Dec 2025 14:13:28 GMT  
		Size: 116.5 MB (116488963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a424b6c76e77e62fd7fbe22699fa67cf9c03ef52c3c75d3a72beaf948f43218`  
		Last Modified: Tue, 09 Dec 2025 14:13:20 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9672dddcf826930346f495d70ef9b3f18eadbc17245e7dd50a6f06898171547f`  
		Last Modified: Tue, 09 Dec 2025 14:13:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcdbdbf2073a5d499f1f283d054e6c9d628b060e3f4bc237ea0522bdf4a5dc`  
		Last Modified: Tue, 09 Dec 2025 14:13:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c776abd48f245d7bb49c4d245ff4c728a368ab34279e95c0cf96e9756be66dfd`  
		Last Modified: Tue, 09 Dec 2025 14:13:26 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eebce1db525efbefd196b06b96a34611d2ec36bca018b75f997d662b882f724`  
		Last Modified: Tue, 09 Dec 2025 14:13:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0bce3228824bf1e1e4a5f31ce3af107d1a5892433eb9621adb5f066409a8a15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5853546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b4008e10bf953fc7085bb0ce9ae373064516512a2d720df044a74facfc93ac`

```dockerfile
```

-	Layers:
	-	`sha256:fad21ec19fa5a666b0d2d6155e3f839b50c9299a1276c9ba26e87ce7213e44d3`  
		Last Modified: Tue, 09 Dec 2025 18:07:57 GMT  
		Size: 5.8 MB (5800196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab9db978f13fa457436bd6c51cc897050a5b2b92d00189db97291f0e8419ac5`  
		Last Modified: Tue, 09 Dec 2025 18:07:58 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:def32a17a6b3f84f455d639be5b6bf687cc747d81f776f2904027a28ca4e40e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160985576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb23dbe88056e31a02f234cbeb33b96c24c54dd9ef157007d8d8b0b259d14c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:37:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:37:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:38:00 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:38:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:38:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:38:04 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:38:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:38:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:38:08 GMT
ENV PG_MAJOR=14
# Mon, 08 Dec 2025 23:38:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Mon, 08 Dec 2025 23:38:08 GMT
ENV PG_VERSION=14.20-1.pgdg12+1
# Tue, 09 Dec 2025 00:14:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 00:14:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 00:14:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 00:14:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 09 Dec 2025 00:14:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 09 Dec 2025 00:14:09 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 09 Dec 2025 00:14:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 00:14:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 00:14:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 00:14:09 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 00:14:09 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 00:14:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725cf3e4bfa36eb2b8eddb47675bb249f0ca3eefe6068b41e37fa647a565ca78`  
		Last Modified: Mon, 08 Dec 2025 23:51:45 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899e4551cb8c25e22e5439deaa5f9a2bfebb42c27d9dfe13b32e42e03fa534a6`  
		Last Modified: Mon, 08 Dec 2025 23:51:46 GMT  
		Size: 4.4 MB (4391344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96440795729f516ea449176989238797f5d4bbd3ae8757a77a04ba941d036e72`  
		Last Modified: Mon, 08 Dec 2025 23:51:45 GMT  
		Size: 1.2 MB (1222829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11b91c535a77489ba0daa9b0dedc7794397bb2a6e2e99b524e50faab62e117d`  
		Last Modified: Mon, 08 Dec 2025 23:51:46 GMT  
		Size: 8.1 MB (8120716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e54f30d6e3687a8c5c94bb3d140fbff52ef5d03601cc11bc041fd6646b48d9`  
		Last Modified: Mon, 08 Dec 2025 23:51:46 GMT  
		Size: 1.1 MB (1097045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022fc848c95d0b9b39608c17b09d6af19633141f1d64c5be5afb6b0a2d5436b6`  
		Last Modified: Mon, 08 Dec 2025 23:51:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bec706c26a025fb818d05790ea0e361eabcad789c5b1a0fdb616a7e33d8f29`  
		Last Modified: Mon, 08 Dec 2025 23:51:46 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a587660f20abd5a439c28744a85a658f8bc433bc105334e97eebb52ae7162a`  
		Last Modified: Tue, 09 Dec 2025 00:14:58 GMT  
		Size: 119.2 MB (119248946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7150b9bff0cc068a5724579508948669521d7c6a2ac9e9c88e962fdc9f759ee0`  
		Last Modified: Tue, 09 Dec 2025 00:14:44 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39664947002cdbc0b9ff9139718741a6b49fb178b21e1bb85ac48175058fd4b8`  
		Last Modified: Tue, 09 Dec 2025 00:14:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db4fe3baef4fed5b71a153c2ad99c1a98098043809638e2c777bf26b6a995e9`  
		Last Modified: Tue, 09 Dec 2025 00:14:44 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316c55df4d700c6cdbd7f382ac86d958ef5e8e84571a866e0724e94df27dedb3`  
		Last Modified: Tue, 09 Dec 2025 00:14:44 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47622954bd0bd48b484b69c3ee3ebdd6f049d179da19b3621fc8164b1c74ded9`  
		Last Modified: Tue, 09 Dec 2025 00:14:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:576c77a2350d16adcdf00654d65e32fb9764bd77db7061d1c0a02a0a800bcff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5856575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573b6a849cf1cb330927101ae4341209841e4cebcff54abe96e43b5c58dd3e11`

```dockerfile
```

-	Layers:
	-	`sha256:a41d08b2c633034aaa16aa7a8b05c2fb264f50bb5d9360dca129e0f6918470d8`  
		Last Modified: Tue, 09 Dec 2025 03:08:44 GMT  
		Size: 5.8 MB (5803279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9785bef344eac2bdf1e9791d7eca763b314f3c34b41838a4210480f0ae5cef`  
		Last Modified: Tue, 09 Dec 2025 03:08:45 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
