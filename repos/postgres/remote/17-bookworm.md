## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:f57cfa8e5c1b89d07c9cee525849772027c1d05b6668b1ee2ce64a4890ecb1ef
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
$ docker pull postgres@sha256:d4eceb7552a57997fff2e9ceb1a624210e61b6432a2a1f7934a418c27bfe1406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156287572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a04d02adcf690e908ccaa1bfeceddbd1a7156107f2fca0534ad5c473b7ec59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed504ed4ebeade3e0145c8654490ec08e90f56163ae8585f440a8c1758486af`  
		Last Modified: Mon, 28 Apr 2025 21:52:08 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1012ab103c420d50bf5b3b2b9d9e566fc6d14cb27a1d13d072590891922553`  
		Last Modified: Mon, 28 Apr 2025 21:52:08 GMT  
		Size: 4.5 MB (4533757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688bd672efd5ea033d3921a58adb553c3aca7430b6459255392d1b1588db4bee`  
		Last Modified: Mon, 28 Apr 2025 21:52:08 GMT  
		Size: 1.4 MB (1446729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c4f6c1b1e70a2abd9fdb96878a5492469d59da28187a489bde55b0f9f11e8e`  
		Last Modified: Mon, 28 Apr 2025 21:52:08 GMT  
		Size: 8.1 MB (8066269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2c2f1196a6e1f46f1378bf60d9626a5b42ffbe5d22461b544de1f34320a284`  
		Last Modified: Mon, 28 Apr 2025 21:52:09 GMT  
		Size: 1.2 MB (1196117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451329d20b9fb14b0a2382c1478c7c3bc8a495c397307980907e1d080159baee`  
		Last Modified: Mon, 28 Apr 2025 21:52:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33518fbc18a9f0a776aad0209c0ace2410c9b9dbd0f3fff4d3e8981e80ae2ca0`  
		Last Modified: Mon, 28 Apr 2025 21:52:09 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7e820633f95788ae9a9191f107a6db5712bda8bc035bbd7b3d73f15517bb1`  
		Last Modified: Mon, 28 Apr 2025 21:52:11 GMT  
		Size: 112.8 MB (112796448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17c4120c78919e3c373e60563bb2b587caac2b7860ffa2fd6afcdc194dc75a0`  
		Last Modified: Mon, 28 Apr 2025 21:52:09 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8937a896f225a1d08cd6dc3eff31432d70487df8c4d531bede81c5a823f11cd8`  
		Last Modified: Mon, 28 Apr 2025 21:52:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a61d71ceb1b3e50ee67257bf1d6bcd5747d8afa9e8714dd33940232c4d543`  
		Last Modified: Mon, 28 Apr 2025 21:52:10 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b75ce6e0b44f73d96c1e63450d487c0ea92f7d550f9816ad9dfcf8fc957d4c`  
		Last Modified: Mon, 28 Apr 2025 21:52:10 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9034c7832ac61076bb7388c36c2a422e2c1525bc08bd9aaceb25028ce6f529`  
		Last Modified: Mon, 28 Apr 2025 21:52:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:110a3f6b5a06deed3e77309160358eb96487095156a581068132a9072a98a14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5873121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6873bbfa438fade8de5ff4d96913db945e8588c6419d7ec5129a0c4bc8688bd8`

```dockerfile
```

-	Layers:
	-	`sha256:faa96198709a203c1fbcadb8c7c9b6ed3e57794d4d86ce84f89c9860493b68b4`  
		Last Modified: Mon, 28 Apr 2025 21:52:08 GMT  
		Size: 5.8 MB (5818434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c76874153903e16f8a6899d76f98a817c34fe40a1c7c6094755ba0386a7a74`  
		Last Modified: Mon, 28 Apr 2025 21:52:08 GMT  
		Size: 54.7 KB (54687 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:29662333747b3d73efbdd63bd07c8dcf2cf0664f7853c0623b344429a3aa659e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149358087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12b08cbbaae6668812a8a861d1736d0e43685794e044844dbffb651e3c0946f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Mon, 28 Apr 2025 21:07:56 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7dbd13a5b1ee87638e8ff020b1d2afd3a00a7bc146f2dd322eff851e885678`  
		Last Modified: Tue, 29 Apr 2025 00:11:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddeed145392a589296f4def151c0cba38caa5ada19685adbdb91ba2a6a6b03f`  
		Last Modified: Tue, 29 Apr 2025 00:11:04 GMT  
		Size: 4.2 MB (4151014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df15ff5474dea0b8a303fcd9ca6d5caf5f5ade1fd5c898351501897de7d9f2`  
		Last Modified: Tue, 29 Apr 2025 00:11:04 GMT  
		Size: 1.4 MB (1423985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12dab1affb15219c1bbe269f8dba51a0b04a4393f6cc5b4ddc6b2dbd7e731e3`  
		Last Modified: Tue, 29 Apr 2025 00:11:05 GMT  
		Size: 8.1 MB (8066459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d53a8d7d21b72bc0336ce7f91d99cb2e76a3f5bb8e50f04848caeffcf3871d`  
		Last Modified: Tue, 29 Apr 2025 00:11:05 GMT  
		Size: 1.2 MB (1194889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550a864e050e101f225d9a0cc2bb1b9064f50226333ad9e131522c36a3921ac4`  
		Last Modified: Tue, 29 Apr 2025 00:11:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b669ee28183d02dee57a101cd1a31845cfd26fe615ab0a0b969ce916dfc59`  
		Last Modified: Tue, 29 Apr 2025 00:11:06 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb2a63e8dbc5626f22307ded5dc855ed49ff7322a43aa8b7b5e2dbbd4fdf409`  
		Last Modified: Tue, 29 Apr 2025 00:11:09 GMT  
		Size: 108.7 MB (108743287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5067717deab212501ee7b414f94988af7b576708f8c58be969ed68c83b2288bb`  
		Last Modified: Tue, 29 Apr 2025 00:11:06 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f359eac59746fd9fe9454ef5da8cecb439c7d5afc9061670798bca2e09e84c`  
		Last Modified: Tue, 29 Apr 2025 00:11:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a2d1dff26f0a34e3680f01673747ae564c7b8221dea9984d03a8c67ea6954a`  
		Last Modified: Tue, 29 Apr 2025 00:11:07 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc7290dd6a59af21960d95532845243d5eb4d5a291fbda767b7f202976020c2`  
		Last Modified: Tue, 29 Apr 2025 00:11:07 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741ba4865787274ef8074852f15d495cb672aa104d73961903a4a55bae16063e`  
		Last Modified: Tue, 29 Apr 2025 00:11:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1381081935010bc86baeca528e83cd97aecb5dbb0e2b50ebf9a30d2675a50237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66411f2ddd8c4b6051cca6f649237622c50e39b2b94d443ea42bf312a7ca1bc4`

```dockerfile
```

-	Layers:
	-	`sha256:710e63b74675c255f987e3b206714c1b0bbb936053a8ec389d7436b32c402677`  
		Last Modified: Tue, 29 Apr 2025 00:11:05 GMT  
		Size: 5.8 MB (5836107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90fc25fa1caeabe7bac7ba08afc24af59d34eae60bff8b907cc4128006bda404`  
		Last Modified: Tue, 29 Apr 2025 00:11:04 GMT  
		Size: 54.9 KB (54922 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7f1db312ef44843964b445af3bbdfe1bb500952b28074d94fc99710cec658b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144337267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fa7bb1891a748de4fbcee3fd3e16d98c275e01380be5ad3bbc50630152063e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a3677b10b3c2b17c251b045a96a5c5899810ee1ee2fa8982715ba998fd10e6ad`  
		Last Modified: Mon, 28 Apr 2025 21:15:45 GMT  
		Size: 23.9 MB (23938074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdb4fadcfae6c7f639bb005beb451a5d1442c02240a0d69d7265e913295df68`  
		Last Modified: Tue, 29 Apr 2025 01:02:43 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2efccad23750e2931d3ed57d24f2835f3b9ce8744beaa721d9437163c0cf9c`  
		Last Modified: Tue, 29 Apr 2025 01:02:44 GMT  
		Size: 3.7 MB (3742519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0f553df79e41f2f793d4828509d5e5323042ad46cd5cd5b31d6d14f8607643`  
		Last Modified: Tue, 29 Apr 2025 01:02:43 GMT  
		Size: 1.4 MB (1413684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad2964e1fa8d5744b87a0ed825b61807320e0a04d4889bb205fa941886b2e0f`  
		Last Modified: Tue, 29 Apr 2025 01:02:44 GMT  
		Size: 8.1 MB (8066255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f726aa2fe47cabbb56851a90a83ab6a9c48b967d6f4ea88827119d6b3120afb5`  
		Last Modified: Tue, 29 Apr 2025 01:02:44 GMT  
		Size: 1.1 MB (1066999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1938ce7122ffddb675c2743693e8ab090236dc16305e5d6d3c52d4d237fc06`  
		Last Modified: Tue, 29 Apr 2025 01:02:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f217542552436de76d587eaa73b78a8a5618772cbc566ca7272527155b615c2`  
		Last Modified: Tue, 29 Apr 2025 01:02:45 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964ae17d83757325c3cd1fb8fbf0b1b3c7bb6c57a596427a61f443eea92b1d56`  
		Last Modified: Tue, 29 Apr 2025 01:02:48 GMT  
		Size: 106.1 MB (106089110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb765c8303a7c0d06b92b62427a593ee9486864fd3a1073c545f7715f83f057`  
		Last Modified: Tue, 29 Apr 2025 01:02:46 GMT  
		Size: 10.2 KB (10243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5025657c78f4d6e559b913233e57deb15e2427b56e9efd130cc8c1848c82bd6b`  
		Last Modified: Tue, 29 Apr 2025 01:02:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1563dab3d5ccf219c9161a5b36560aa83a6a4b6cea3098a3c0c4a18a9da3ec12`  
		Last Modified: Tue, 29 Apr 2025 01:02:46 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9983ecce06edc3887e9c95fe6ec6e1d3b5025e834c28dce00dc945e2d67ec5f3`  
		Last Modified: Tue, 29 Apr 2025 01:02:47 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e591a6944dd600c0156e4e5582673852082afcc00c6bbe4d91f439b54527b336`  
		Last Modified: Tue, 29 Apr 2025 01:02:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fc4d50b37eae5e6de98b56c6986693735bbfb479a0904eb209f592bfab3a2f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5890600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ea29c159105a3134315a76dfb6ae869ec17245a6870ba95b6cd637a9ad186`

```dockerfile
```

-	Layers:
	-	`sha256:5c972671c704dd44786d0839ae00c52b5f19fd01af6787a9b638609bce1115c5`  
		Last Modified: Tue, 29 Apr 2025 01:02:44 GMT  
		Size: 5.8 MB (5835678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6480b36863ac51ad3c28ab69476dd48fee366b45fee5584fa6d8d5cf957ff63`  
		Last Modified: Tue, 29 Apr 2025 01:02:43 GMT  
		Size: 54.9 KB (54922 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:97a160118c773609ff236d79036fff8bfe23d446c984993042417f2fd2e699f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154121496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee23354db98232f14af587876b4a5a9f25466ca1676fa310bd75a12a19ebe08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da6d707817bfb1b7d78ba0d26b56f9e77a089c182450e8585dff3c4bb737890`  
		Last Modified: Tue, 08 Apr 2025 05:23:14 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b6ca7917a98f030679f2679bb9f16ae3c357180bf0162d38b8a6127cd1338c`  
		Last Modified: Tue, 08 Apr 2025 05:23:14 GMT  
		Size: 4.5 MB (4499187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72fc08ac26ee4bf3b1ba41a882c7deb450047726e21569041b46af65d71d9dd`  
		Last Modified: Tue, 08 Apr 2025 05:23:14 GMT  
		Size: 1.4 MB (1378751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bfa870fec3fbe5b18b0872be14f230c0819e8eded65b5a021636f62af7ae7b`  
		Last Modified: Tue, 08 Apr 2025 05:23:14 GMT  
		Size: 8.1 MB (8066376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65be87db509c304fda88f4943c5f7e6accf8f225c87438ecde1e6fdb18b4447`  
		Last Modified: Tue, 08 Apr 2025 05:23:15 GMT  
		Size: 1.1 MB (1108726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f778b98a8dbf4ee01d00566661b19de481c2f12cb0b20283848351349321c`  
		Last Modified: Tue, 08 Apr 2025 05:23:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a9cbd0b73694e10522b06b2e893785c793695d54bb181f976cc5be0305c46e`  
		Last Modified: Tue, 08 Apr 2025 05:23:15 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22592ebceca81ecefa415d82d834184b5cad6d1e51436b7fa0684fdbd8490725`  
		Last Modified: Tue, 08 Apr 2025 05:23:19 GMT  
		Size: 111.0 MB (110981519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3bacc76b0c1630c93b88647f57f77c1fb4e8a14037bc59325228e29621ce0f`  
		Last Modified: Tue, 08 Apr 2025 05:23:16 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f4e734adeea9d911244725ca933a2260a9e691564887289db21538a1581ca`  
		Last Modified: Tue, 08 Apr 2025 05:23:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53782aa5200437f73b94b3b8dbd099b4edcde2b219cabc341305922c19f832d`  
		Last Modified: Tue, 08 Apr 2025 05:23:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4397474b5e5f1d9d8de8472f0d579743398ea79bc9beb440881180f6b919948`  
		Last Modified: Tue, 08 Apr 2025 05:23:17 GMT  
		Size: 5.5 KB (5473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd80efa9c3a1d49fd8a79f330a9bf3db218a84a3acbab9fbab28d05df9efa607`  
		Last Modified: Tue, 08 Apr 2025 05:23:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:08e6d8a6d3de47829846db473ae205aaf384efd026dbe7fb8d58450aef1cfad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5880584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400c45c41806e63b8d9f3709381aed91d0eefdfc2d972baaa025cc3e11dec40d`

```dockerfile
```

-	Layers:
	-	`sha256:e27ec7a23655ccd6ca8bd796dae9d4d44cafc23cf3a4369669d5e102076741c6`  
		Last Modified: Tue, 08 Apr 2025 05:23:14 GMT  
		Size: 5.8 MB (5825604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58f9c13b07da1e88d508a7e34f03de97b5d30cf55ebfcdb85d01966af7cc25b`  
		Last Modified: Tue, 08 Apr 2025 05:23:14 GMT  
		Size: 55.0 KB (54980 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:2b8556f513d6cddecf5166f65fe5ee0c38bafc69eed2f8370744dad0443a0f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165195654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02817e2d6964502baf4cc5503d6d6232feb12abf6409dae28582c20319c9769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4def8745002c1f930b5ef9518cd492bd606ed517adc7f21a530483986c855b`  
		Last Modified: Mon, 28 Apr 2025 22:03:59 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8d90f052b72a814fccc8d5a9622b9bb959056cb736eb1ec659c83d8b7aa912`  
		Last Modified: Mon, 28 Apr 2025 22:03:59 GMT  
		Size: 5.0 MB (4965136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968c34b87f52057a91f2a7732af4e39979315e49103c74afd4fd43f4dcf3589`  
		Last Modified: Mon, 28 Apr 2025 22:03:59 GMT  
		Size: 1.4 MB (1422208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d37baf1a316256bdff4e20d46571f66050ed686ba95b4f6a194743bd79f35bf`  
		Last Modified: Mon, 28 Apr 2025 22:04:01 GMT  
		Size: 8.1 MB (8066280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8c16f194055f7efcca33bd765375e64cfbdddbd47d4b78c4957e72b77b7247`  
		Last Modified: Mon, 28 Apr 2025 22:04:00 GMT  
		Size: 1.1 MB (1137193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bef6e911bf33ff2484b248d98a12a060dbe4b1204b8fcd692b6edf68018bedb`  
		Last Modified: Mon, 28 Apr 2025 22:04:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeeadb6eda79d062d0cf67a82d8b86a45ad71acfeffb13e9c38d97afab616deb`  
		Last Modified: Mon, 28 Apr 2025 22:04:00 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74433ecc707ef67f316ce6e5dbaa9b73ba143426a03818ccac2ea0645be4980c`  
		Last Modified: Mon, 28 Apr 2025 22:04:04 GMT  
		Size: 120.4 MB (120373360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1236e20dd6c275a41f4119e899778c251f5a682d22be5a2869b1d6bdb2ae1987`  
		Last Modified: Mon, 28 Apr 2025 22:04:01 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbe78a8200b711863e68d2a40537d4870ca9b6d32715c5fb80a3925fb626fee`  
		Last Modified: Mon, 28 Apr 2025 22:04:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b1dc4fe1be3d89bc436b9f5f7c3ac56f156c2fbc89d172980a74b2c63dda9`  
		Last Modified: Mon, 28 Apr 2025 22:04:02 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf4675cea5c059d5dbc18d3e8857e5312b9d3b96e5f404367ca474801a61198`  
		Last Modified: Mon, 28 Apr 2025 22:04:02 GMT  
		Size: 5.5 KB (5470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0555740ccd257ed45253e05c53a811301a703c3727e4521ceaec8632691ef23e`  
		Last Modified: Mon, 28 Apr 2025 22:04:02 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:be9e3693bc7760e6c84c38125aae0fee764643be674a5ce73af4ec4c0a3f4671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e3abf9e5ed9a493c0c0b747a8160f5db00fff8cd05c0b25b91f96cafc05928`

```dockerfile
```

-	Layers:
	-	`sha256:8eafc451467dc21c2191551435633672189add493de66b5dc3c817d8617c6c30`  
		Last Modified: Mon, 28 Apr 2025 22:04:01 GMT  
		Size: 5.8 MB (5834119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f90f4ddc113e9084536def85c3c3200b7431bd9eaf52c54585beab98ae106260`  
		Last Modified: Mon, 28 Apr 2025 22:03:59 GMT  
		Size: 54.6 KB (54623 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:13ff3ce1c45d7cc954a0388dca2127761fb8b462aa7fb6a0d5b53a82913a210e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155158620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497bc77775f3b8f183c11565afea7d707fdc0ebf93dc77393c0920567a219dab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf86079eafad14c9e6dc2a7e8ffa4ec0ac0a330ed3d25e9d09c1888d58daf4dc`  
		Last Modified: Tue, 08 Apr 2025 11:31:07 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca852a9dc1f8245c1b91285c91f41838c8b29fe4694f7fadbd0b731136f90294`  
		Last Modified: Tue, 08 Apr 2025 11:31:08 GMT  
		Size: 4.5 MB (4475153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca35ee6858b9f76e8d819c0e6c3d7f84c852e6c49d6098dce782670797997147`  
		Last Modified: Tue, 08 Apr 2025 11:31:08 GMT  
		Size: 1.3 MB (1333924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b558be61e2efcfbd147d64c068b214943b4911f9d10d75c1ae39b006269f720c`  
		Last Modified: Tue, 08 Apr 2025 11:31:14 GMT  
		Size: 8.1 MB (8066603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662989c626a5de33ee3a63e5a7dfb85983edb4b08c4b3e45cd8595c2b630873f`  
		Last Modified: Tue, 08 Apr 2025 11:31:09 GMT  
		Size: 1.2 MB (1182666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e138e282415a57c8f82414779abeb380674d841f89c169963ce32dd9a4776c`  
		Last Modified: Tue, 08 Apr 2025 11:31:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2edbf1c77e98ebed72ee4b3fadd15e2dd652cdb0ac4bf845cb6517fdc061ee5`  
		Last Modified: Tue, 08 Apr 2025 11:31:09 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441b072e1681f4257283d75a9965de0732172d2d4e4b7570592ac21025e407d9`  
		Last Modified: Tue, 08 Apr 2025 11:31:36 GMT  
		Size: 111.6 MB (111565691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ee65f74436219358c465ec56714b56be69d26eb81bf5fd193d299cef9d2a57`  
		Last Modified: Tue, 08 Apr 2025 11:31:10 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e3287a98d2ca3a4b22f691a49d7cc7b328f37857aede9955a46e9f5809254`  
		Last Modified: Tue, 08 Apr 2025 11:31:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13758c11f8c0d7412cd975aebd7406b10ca15667fed75382b91163b584ec5adf`  
		Last Modified: Tue, 08 Apr 2025 11:31:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b18c22dd6935050108c46a1d022478c5f81474029ab5a5bdd8857cd960b5af`  
		Last Modified: Tue, 08 Apr 2025 11:31:11 GMT  
		Size: 5.5 KB (5477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d538696a9cf8491a06395b7a50f770bda61533a712d8933cd7c7b61414f1f7`  
		Last Modified: Tue, 08 Apr 2025 11:31:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:00aedbd6a25053059335292cd0c72e781b45e755eff0562abbd08c0da286b329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 KB (54589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6f7c431ccda1799b130303184da1b8418d8b71753e6d88fdf116fd8e9e9e5b`

```dockerfile
```

-	Layers:
	-	`sha256:044f3c0c0cf8d005241bfeff8e5cd7a49ece44d1f835a4b79078cebc4d093862`  
		Last Modified: Tue, 08 Apr 2025 11:31:07 GMT  
		Size: 54.6 KB (54589 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:77cdf06c3bb3cd77a1fcf77fe7046375abab740c066687e11910835aa0be71a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.0 MB (169048118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac06db087082ff91d9af0838304e76e4cc1301b53b293759b71362299ae3b259`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aecccb244efc7d4bda38a6b1f15f48923a3f326f79d43c1ad1cf4972ec41a14`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba53104c6d323a45d3a84ab8de62bc99e5e7a0d7b2eb8759e4c10448e308ff16`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 5.4 MB (5368229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b610c510be8c81b2b587ef9f554ba60a0d35d758c721a405fe8b0f08a40fed62`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 1.4 MB (1368760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a9faa9d682ef30681c416a68d3205a50af33989daff8bfd12bfa92a39d8dc0`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 8.1 MB (8066429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2815faea99c9050a34ab7555c1428e5cbc69a6f768e9aeb499bf83f6e9c3d6ba`  
		Last Modified: Tue, 29 Apr 2025 00:04:49 GMT  
		Size: 1.3 MB (1283539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4e76c309677517e1c0da65c16f2876b6442c1628abbb49014fad1aa0c1f1ce`  
		Last Modified: Tue, 29 Apr 2025 00:04:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2511b3704ad26efd3bd6b6ee52c75a8a420e7a54dbfd81fe256830b3b3d2b6`  
		Last Modified: Tue, 29 Apr 2025 00:04:49 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b3ca8f32e859f2238071ab98c7b2c2ec5e0917457ae84aad89764d0c65cf32`  
		Last Modified: Tue, 29 Apr 2025 00:04:53 GMT  
		Size: 120.9 MB (120872105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d77ddc02848034c3aaedf332b93d8f86a00185f6ae35e23a6bee8f6cb63e35`  
		Last Modified: Tue, 29 Apr 2025 00:04:50 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb8291030a388cc2cfbb9eeecb2777ec55cfd5cdb26418c9c3eb583eea80636`  
		Last Modified: Tue, 29 Apr 2025 00:04:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79869bccdfef9d65dec4099c0fd9c9165aecc70dc62e4ad1b485edc9b598d53e`  
		Last Modified: Tue, 29 Apr 2025 00:04:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3cf3a2618d7f54b247b71745e7536256b771f3cc4e0b78025f57cc339c2a56`  
		Last Modified: Tue, 29 Apr 2025 00:04:51 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486f2f33e3dc9cdad2d709653efa45310c8110867965a603224718f3ed4c7a04`  
		Last Modified: Tue, 29 Apr 2025 00:04:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:68fcd7a1987704bd87e398f0f44144d08c4dae18c0a94309d8c8fcd2da6f09b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5880460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b857e12198cd3f5b48fc619aa05d6ce728713ab0afbaae5f68467a61064689`

```dockerfile
```

-	Layers:
	-	`sha256:c6e55b270860464f7d3e1f3f0acf817ee84addf87fb058df42181f9835e75ad2`  
		Last Modified: Tue, 29 Apr 2025 00:04:48 GMT  
		Size: 5.8 MB (5825695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fe17686030b42dcec8d68dda6f1164f57fbd70b1700be1c038e7050fbe84346`  
		Last Modified: Tue, 29 Apr 2025 00:04:47 GMT  
		Size: 54.8 KB (54765 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:9114c05d04653fd14c3ca18591e4be9111aae9eb99d9a1115a456bae6308ff81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165428509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b26edf22e9a2a51cbe44405eb7f2f7e4a90d9185d20bde94de455a465a0b969`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Feb 2025 00:53:12 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV LANG=en_US.utf8
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_MAJOR=17
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PG_VERSION=17.4-1.pgdg120+2
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 27 Feb 2025 00:53:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 27 Feb 2025 00:53:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 27 Feb 2025 00:53:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Feb 2025 00:53:12 GMT
STOPSIGNAL SIGINT
# Thu, 27 Feb 2025 00:53:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 27 Feb 2025 00:53:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6ceea3e93e14f792750d1766a5ebfd761d9dc9254b37e35fd53660754cc4ce`  
		Last Modified: Mon, 28 Apr 2025 23:41:37 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5553e636c58f261b388fd0065e409a44d059a465f0cee0608aed0359e82ec5`  
		Last Modified: Mon, 28 Apr 2025 23:41:37 GMT  
		Size: 4.4 MB (4391070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a22915eed3e01edb79952f0f75976828fc526a800b1b57a3dc32c6cefb45e3`  
		Last Modified: Mon, 28 Apr 2025 23:41:37 GMT  
		Size: 1.4 MB (1412763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde711414fba469d3c89853f125b128e0539d38681fedf651614c085eea945f5`  
		Last Modified: Mon, 28 Apr 2025 23:41:38 GMT  
		Size: 8.1 MB (8120469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d68dcaff298a7890e49ccb808912ee20a05bf83ae37cb98d8f189d4545767a`  
		Last Modified: Mon, 28 Apr 2025 23:41:38 GMT  
		Size: 1.1 MB (1096772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cbbcff035b7b09d2b04777b2daf46d1d8e72cdd589567c438ea06be3e6dca6`  
		Last Modified: Mon, 28 Apr 2025 23:41:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab5b1948c8b21b9ae8e9badd557e339ef86e99a596ca8e385e03a03d003491a`  
		Last Modified: Mon, 28 Apr 2025 23:41:38 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98a86c311c3d55c46b63e2114b73897fb48506110d933d7e06af9224e9f4aab`  
		Last Modified: Mon, 28 Apr 2025 23:41:41 GMT  
		Size: 123.5 MB (123501950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4a0c6398002303af6d085522bf24db689498dee1cd88f4a4b964bb46daf735`  
		Last Modified: Mon, 28 Apr 2025 23:41:39 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99c1ef43491254f7af07ee844f5de389f825fe7c35599a46f0ca34957ba3e99`  
		Last Modified: Mon, 28 Apr 2025 23:41:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15432e3c410955083abedd7f76761568dac47716d5e64f59120f062780916c42`  
		Last Modified: Mon, 28 Apr 2025 23:41:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e61dfe6db58653ea8483e3616a6be876d59232b17b88bd57a2ec428d1674686`  
		Last Modified: Mon, 28 Apr 2025 23:41:40 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1bd830c99491765537e52244af4f57d481088cc9dd277aab73ef5ce9281b83`  
		Last Modified: Mon, 28 Apr 2025 23:41:40 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:47760f7c7e29431a6e6393e6e0d3a5721a7780a2842403c1d7300a05ffc3bc07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5872404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9a62012b63525fea3252377e15265712c19a9386f6feb6a58ef36c7a3f96a6`

```dockerfile
```

-	Layers:
	-	`sha256:0513b70e89510b7028bd9d8739897e46697130cd26c1dddc654d53d953b5c813`  
		Last Modified: Mon, 28 Apr 2025 23:41:37 GMT  
		Size: 5.8 MB (5817717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9a6a942bd422f4e4cb1cd6b9057babb9e131421da7879e80b7ddb0deb69a24`  
		Last Modified: Mon, 28 Apr 2025 23:41:37 GMT  
		Size: 54.7 KB (54687 bytes)  
		MIME: application/vnd.in-toto+json
