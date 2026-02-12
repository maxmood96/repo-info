## `postgres:16-trixie`

```console
$ docker pull postgres@sha256:d7486e4259a835fad05999c895620c0213f05e7cd6f0221d7f5471bbf32184ab
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
$ docker pull postgres@sha256:671edd2067af03a22235546817d0367bc5c4cc834efdebed50d0f445ad9e7bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160132459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c80b87c813a2ee26748ce49686844942f297bcc19b6cca3d49cd2fe0a87808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:04:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:04:32 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:04:36 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:04:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 12 Feb 2026 21:04:36 GMT
ENV PG_VERSION=16.12-1.pgdg13+1
# Thu, 12 Feb 2026 21:04:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:04:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:04:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:04:47 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:04:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:04:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e4628b174b7e518d5182f21cd9dd5f6e3e52156a4c4cc2f4146dbf432744e`  
		Last Modified: Thu, 12 Feb 2026 21:05:06 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672b38b519e3ed6af935d1db4b73e576d3fc0be7aa3538d79d32472396819429`  
		Last Modified: Thu, 12 Feb 2026 21:05:08 GMT  
		Size: 6.4 MB (6437906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9da9a39d3860c2dc168afb55c2b256f79836355eef04ca539bf11093a7337e`  
		Last Modified: Thu, 12 Feb 2026 21:05:07 GMT  
		Size: 1.3 MB (1256732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c7e7ae7017975eac5daaf712f764699c8b89e48432dc32d4e83354704409e2`  
		Last Modified: Thu, 12 Feb 2026 21:05:08 GMT  
		Size: 8.2 MB (8203791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023a0ad09ee980f600604c40aee9546b5a6bb896077c86c646a5cd9ab438cec4`  
		Last Modified: Thu, 12 Feb 2026 21:05:08 GMT  
		Size: 1.3 MB (1311607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8196d5fac2e7bff98484dd951ad017dd5a6c6991cef1b93b5e345033d14ed`  
		Last Modified: Thu, 12 Feb 2026 21:05:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453125fb72413add1127741c540136a56949a37d2839a34ec0901e3e53fea40f`  
		Last Modified: Thu, 12 Feb 2026 21:05:09 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05469d57f58755bba8f8a9e969422cd676c4ab6e1a0a1866fc8737d74346e308`  
		Last Modified: Thu, 12 Feb 2026 21:05:20 GMT  
		Size: 113.1 MB (113123006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ec76c49bc3cd991715a19c598d2ade970c257bb94ad0e74051886145a65a7`  
		Last Modified: Thu, 12 Feb 2026 21:05:10 GMT  
		Size: 10.1 KB (10065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293fe20c06d4202628aeda634757db68868893421e7ae9b416fd603bcfeeda9c`  
		Last Modified: Thu, 12 Feb 2026 21:05:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce80fc5ff389ae8ec9731a00b9f3ae99b797d323e249f3d0fe76493ec7b87ec8`  
		Last Modified: Thu, 12 Feb 2026 21:05:11 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646fe7da0dff47548f76673b0b09249fe16756f7ba33ae92fa172e44c2fcdca8`  
		Last Modified: Thu, 12 Feb 2026 21:05:12 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4ffd5284ad51e8dc4d342beb7624e6877e99d52b09eaa0e021dc18b3d0486b`  
		Last Modified: Thu, 12 Feb 2026 21:05:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b7ea3d43530d4391991d77e7b4a53eae882361811584d309b135629374566aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a855480b70dd4598625048884b5a43634ab6bb57f02385e27a95af2f6c69a12`

```dockerfile
```

-	Layers:
	-	`sha256:6b07fc76fde188d412e1650dc5e2883916dc45dba88d21b1729888b3640c5a39`  
		Last Modified: Thu, 12 Feb 2026 21:05:07 GMT  
		Size: 5.7 MB (5708724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d272ffb22f04a7bd667cd6634783d457a02d0b4caa55c4d9072db5bc9fdf3c7e`  
		Last Modified: Thu, 12 Feb 2026 21:05:06 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:2746e78f2f501e10148f73106653ceebf6ff443e8be4dc4d182cd32734162a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154141012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d180a1e4fead96140e57599a187736e7bc2242e58d5b638b84f1f2e4597818d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:54:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:55:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:55:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:55:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:55:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:55:23 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:55:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:55:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:55:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:55:30 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 02:55:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 02:55:30 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 03 Feb 2026 03:11:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:11:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:11:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:11:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:11:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:11:48 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:11:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:11:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:11:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:11:48 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:11:48 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:11:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5db6ada44344198b0bddd0f57487d5a098666df54bfbcc49e0a42837fd9b2c`  
		Last Modified: Tue, 03 Feb 2026 03:12:07 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f2da2ebee65e172eda5151b79850d3514b53d002e09bf84088d6ca91ff18d0`  
		Last Modified: Tue, 03 Feb 2026 03:12:07 GMT  
		Size: 5.9 MB (5930386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6174bd06c4769fb0af7e1578e3b146993498726ba0b7102a94b4810d8771f06`  
		Last Modified: Tue, 03 Feb 2026 03:12:07 GMT  
		Size: 1.2 MB (1227513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3e0b7946ef018e9646a15c6626c61f6c5f00e39ddb1dcb590dad86606dee6c`  
		Last Modified: Tue, 03 Feb 2026 03:12:07 GMT  
		Size: 8.2 MB (8204244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6021531c86e961758a7a5c7a20fb34fb93e353feeb56bd7723d2e61b4c6ee1a6`  
		Last Modified: Tue, 03 Feb 2026 03:12:08 GMT  
		Size: 1.3 MB (1317299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f420e199893d2f8c22d05a975dd3678f21919bf41f5e2a7e730ae0434b987909`  
		Last Modified: Tue, 03 Feb 2026 03:12:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96b43966c7669a6873238d374f95df95114cbb8f011dd45ea4e0db9f3a501ec`  
		Last Modified: Tue, 03 Feb 2026 03:12:09 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f957f7274469e867bda23de4bea1952805505caf6976fbb97bfc0caa3da231f`  
		Last Modified: Tue, 03 Feb 2026 03:12:11 GMT  
		Size: 109.5 MB (109493249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281635e191631f30c24dd50340423461de0a8857712847c7feeb4b91d0fc0030`  
		Last Modified: Tue, 03 Feb 2026 03:12:09 GMT  
		Size: 10.0 KB (10013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b89e7c14b017aa5582cfa81e67824caf22c0f7588cbd0d4876687b39e5efe53`  
		Last Modified: Tue, 03 Feb 2026 03:12:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0179a4b49514410bf2e6e7a54f704d44543bac17270697ca37868da1714f83`  
		Last Modified: Tue, 03 Feb 2026 03:12:10 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515a1a6000a979b4e2563a72acd0e8790d4e06ec48ab924c10d2e2f5edcb595d`  
		Last Modified: Tue, 03 Feb 2026 03:12:10 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e6e9b276be0ea6b12ba781bc5ccc8402c8452c112136bcdd036817df3577b1`  
		Last Modified: Tue, 03 Feb 2026 03:12:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:9a0b612817ee446a25c1c63782be76ecea7129a0a5ce9ea023256de2803ef69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3de7d6a4732c69456b6ed60bd1722839a382e5686642ca177e709be16391d4`

```dockerfile
```

-	Layers:
	-	`sha256:ecbdf89073f128c090939fb88aacc51540e7cf6e093174769b006304f3537088`  
		Last Modified: Tue, 03 Feb 2026 03:12:07 GMT  
		Size: 5.7 MB (5725362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610dd8012f823b65df3fbe035f91084f18a9b3d1b2b5adcbaf5cf2c8269b590c`  
		Last Modified: Tue, 03 Feb 2026 03:12:07 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:93ef5c72e22573da553436046cde42fe49ceca1d959382c7ecbe3bd01decf57b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149200915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c544e935ca68d0f6ad76bfe78667667209b151f3f08fd8c21c564f9d405ce1fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:11:56 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 03:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:12:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:12:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:12:19 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 03:12:19 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 03:12:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:12:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 03:12:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 03:12:24 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 03:12:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 03:12:24 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 03 Feb 2026 03:26:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:26:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:26:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:26:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:26:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:26:55 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:26:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:26:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:26:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:26:56 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:26:56 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:26:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170063cfef7abbab39f7dd80a21e9736dbf207136c85be27c9c1784394044b0b`  
		Last Modified: Tue, 03 Feb 2026 03:27:14 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12728b4f8f23f541776fcb2bc70b9bd384ec137f8ba7f1264e1f5675014a96`  
		Last Modified: Tue, 03 Feb 2026 03:27:14 GMT  
		Size: 5.5 MB (5496499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a638076b95c11f29a15888725afedf4aa7503d8bff06d752c8d8096d3dac22`  
		Last Modified: Tue, 03 Feb 2026 03:27:14 GMT  
		Size: 1.2 MB (1222410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36556cd6cc7cd2e06ab695768f7cef7f50c3fb4c8c729d31e85abe0e24654fac`  
		Last Modified: Tue, 03 Feb 2026 03:27:14 GMT  
		Size: 8.2 MB (8204007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74e38a2a76cfa65ab90c17d1eed72abd3b67aa037816c2f4dc544a5499f96fb`  
		Last Modified: Tue, 03 Feb 2026 03:27:15 GMT  
		Size: 1.2 MB (1172595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c4e1d75e1253702d1a405208e9a2811a1314900a61d5c5ba5729bde62d1bf1`  
		Last Modified: Tue, 03 Feb 2026 03:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60aa282791ed13a6163ba225a4f5fc83f5880414ac8194b0ae40d86235de7caf`  
		Last Modified: Tue, 03 Feb 2026 03:27:15 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20cc590089f86827d2b5df431425bb86c5ba03518c4ce11ea802082383369c4`  
		Last Modified: Tue, 03 Feb 2026 03:27:18 GMT  
		Size: 106.9 MB (106870874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e24b44f85e6be137ad6f973e2cae5d599ad342e6d59773446e9f6fde3349ff`  
		Last Modified: Tue, 03 Feb 2026 03:27:16 GMT  
		Size: 10.0 KB (10028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2646b945ff9e22547ca72fd947bad10c301c3a3d92260b89bdef114690303bd6`  
		Last Modified: Tue, 03 Feb 2026 03:27:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626d6bad2757390bd715a7d59fed11affad442e9ab6c3d903dcdcaee974e2369`  
		Last Modified: Tue, 03 Feb 2026 03:27:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc13d8317c6a6da134ed2c47caa77d7dd66c00dd223998145f3263acd82688a`  
		Last Modified: Tue, 03 Feb 2026 03:27:17 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d98acfdc32eea91ed100b50d87680754b004b67ebcfe305ac9a89a3ef593a3d`  
		Last Modified: Tue, 03 Feb 2026 03:27:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:0806afcb2652a61cbfe992641dcb52513c224ee2f8e82a68ba8723a2caae1ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9f53b7cf821a32ad1b394a16ce5a9bde673fbcbbf3fd763a97f9cfbedbbc9a`

```dockerfile
```

-	Layers:
	-	`sha256:785d27c46caefcfa211eb03df832ce10393d46692e74c9b42f67e4e8677242d2`  
		Last Modified: Tue, 03 Feb 2026 03:27:14 GMT  
		Size: 5.7 MB (5724667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b73acc0672d5893cfd0060d33df8a163a622faf61e97104a4f5461202f3941f4`  
		Last Modified: Tue, 03 Feb 2026 03:27:14 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:288939e49fc9c58111908a852a1ce96e431ef223e2ba7bd63ff77a3cfb7b6c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158751471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa01b97f2f0d3af4241d251d8cdc6cce2cf8f95809f0e9d32088620d02606ab9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:04:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:38 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:04:43 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:04:47 GMT
ENV PG_MAJOR=16
# Thu, 12 Feb 2026 21:04:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 12 Feb 2026 21:04:47 GMT
ENV PG_VERSION=16.12-1.pgdg13+1
# Thu, 12 Feb 2026 21:05:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:05:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:05:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:05:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:05:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:05:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:05:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:05:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:05:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:05:01 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:05:01 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:05:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159d36e850b33c3d4351cff190fced1c01d2fb60cf486826ce84d8cde616bdce`  
		Last Modified: Thu, 12 Feb 2026 21:05:20 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f72f2469f7a83590031d747a1f13cc8123b67646396f8f77b985de66d5c765`  
		Last Modified: Thu, 12 Feb 2026 21:05:20 GMT  
		Size: 6.2 MB (6231080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb4ddf8b2687900480c04dc4b6f8a0ac597c69e98409333083ca84802aff8fb`  
		Last Modified: Thu, 12 Feb 2026 21:05:20 GMT  
		Size: 1.2 MB (1209549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa75330dc5c35118107bf074936607ac008c24dab1fca02d51017ef50435cdac`  
		Last Modified: Thu, 12 Feb 2026 21:05:21 GMT  
		Size: 8.2 MB (8203947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6e9e133ab370822b1c0dc7a3517df91fb45dd65e4812829ab3dd8eccf9b314`  
		Last Modified: Thu, 12 Feb 2026 21:05:21 GMT  
		Size: 1.2 MB (1220561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7d8ae723c7e120eaecb63f9e608a15ca720f8a16c010e6b5182a7596ed10cf`  
		Last Modified: Thu, 12 Feb 2026 21:05:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc2c34c39df6733bd45a687dd21c22a0c9f3930187177d465483299a4fbbbe9`  
		Last Modified: Thu, 12 Feb 2026 21:05:22 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6555bc89c213e5d89df9f7732637b3034b22dc3dc2951ab98d59d17cdb82bb45`  
		Last Modified: Thu, 12 Feb 2026 21:05:25 GMT  
		Size: 111.7 MB (111725454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63e511144f4c14fd372dbc2676104e46a6d453b56dcd57b02b8018dc5c5dfd7`  
		Last Modified: Thu, 12 Feb 2026 21:05:23 GMT  
		Size: 10.1 KB (10069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff13f785d6eb448e968590d16fad76b91216777fe6c8a46ef91782d541a0670a`  
		Last Modified: Thu, 12 Feb 2026 21:05:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca09dc26af4d95c27614dd94a4751d2fde363bf8744520e3c3fbb92e50ba8984`  
		Last Modified: Thu, 12 Feb 2026 21:05:23 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b5ed65c63436abe923e27ca88ef7797dec1617db94da4cb6249eca6a45b417`  
		Last Modified: Thu, 12 Feb 2026 21:05:24 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d6cd55c82264e134ab6e011dd856c1a0760c795ee66c9ff15e9dc9fbbf79dd`  
		Last Modified: Thu, 12 Feb 2026 21:05:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:44f341aa90e612273b7e7dfa14f4ea47b8611c7bf5e775a829e47a537fefa6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fae53cf3098afa870f64db62642c8eb6527373cdb9a5a383e2abf1a9f392b7d`

```dockerfile
```

-	Layers:
	-	`sha256:2bfe745dd88d6bfc2cadf8a9067a5df94a429b5e04ec30d2dc9fe6e5bfd7c15d`  
		Last Modified: Thu, 12 Feb 2026 21:05:21 GMT  
		Size: 5.7 MB (5715070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:466c449fdd538f74e3db6b25aac8262a33698f33d81635c931876f3d7827becc`  
		Last Modified: Thu, 12 Feb 2026 21:05:20 GMT  
		Size: 54.1 KB (54136 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; 386

```console
$ docker pull postgres@sha256:33a23880cda5c639b52b95ce44ba9107bdc02789ad66bfc1e92525fac86ba8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.2 MB (169218995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f640de29de8437c0fee46a7b5766188009962d1adf1394cd3f2fcbf0f1f677`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:37:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 02:37:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:37:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:37:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:37:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 02:37:45 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 02:37:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:37:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:37:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:37:49 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 02:37:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 02:37:49 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 03 Feb 2026 02:49:15 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 02:49:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 02:49:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 02:49:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 02:49:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 02:49:16 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 02:49:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:49:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 02:49:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:49:16 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 02:49:16 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 02:49:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a421359866f260cfbca54b55a928f88a37ba1d6deaf08c7ba6b50067eace0ba6`  
		Last Modified: Tue, 03 Feb 2026 02:49:35 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f759f4d817e4a1b04fde66561869977cb0e1ab1b49f37112c69657523bdaaf19`  
		Last Modified: Tue, 03 Feb 2026 02:49:36 GMT  
		Size: 6.6 MB (6630563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172969f49fa65a97b187cb71ceccade530ec6faf87ed4c0d63f605f4795a7e11`  
		Last Modified: Tue, 03 Feb 2026 02:49:36 GMT  
		Size: 1.2 MB (1225831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbccc11d6b6e423a07496580e69c3d321d0e77308a509b6280b45fd1e94e21a`  
		Last Modified: Tue, 03 Feb 2026 02:49:36 GMT  
		Size: 8.2 MB (8204013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392005215375a83ea63ca680cfa667dc1f3f2c4cc26109d2899be9eafae5f817`  
		Last Modified: Tue, 03 Feb 2026 02:49:36 GMT  
		Size: 1.3 MB (1308243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b91157b0962d5a8c844b989b909b5f9e0e605d78a9c3c3193f639cbe88ac15`  
		Last Modified: Tue, 03 Feb 2026 02:49:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef22bce6182ba8dbaead04cffd01028568c6b115c1f8159fdf92672af5d852be`  
		Last Modified: Tue, 03 Feb 2026 02:49:37 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d7db0f1202a5133435e6ba36711b8ea0aa4237aede24f5d588da809b7fdae8`  
		Last Modified: Tue, 03 Feb 2026 02:49:40 GMT  
		Size: 120.5 MB (120535718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d3846fcee2688797828b8f216cb59ed4b923daff95678013c258c17d077ca`  
		Last Modified: Tue, 03 Feb 2026 02:49:38 GMT  
		Size: 10.0 KB (10023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830668d38e4256e469d67f032d27c0b6b1a0846c8555aefeee3b4ef259734b53`  
		Last Modified: Tue, 03 Feb 2026 02:49:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5d80d2a554a4b33c837f4a955093375995807db435c80ec00a210f530c019c`  
		Last Modified: Tue, 03 Feb 2026 02:49:38 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28158e2c0832c13b10d0b2a706d9ba2cb45242a6fa40d18d08e45370b700b1`  
		Last Modified: Tue, 03 Feb 2026 02:49:39 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f849b257293e3bb10285b11e1b22b48ab72733786ad61122c6b08a84dd06097d`  
		Last Modified: Tue, 03 Feb 2026 02:49:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ed3f8f5221ed040755d130d6804e8181650ea1917f65d4124bf539f42717709e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50945f8fbbece369055d61095b3dac1bfe2d59169edf956e7939f9d39e7b1b36`

```dockerfile
```

-	Layers:
	-	`sha256:14abf9800bd7eacaa2f0e4b9b104b5b169cd23c9f5de5a37e7b229ab821801bf`  
		Last Modified: Tue, 03 Feb 2026 02:49:36 GMT  
		Size: 5.7 MB (5724255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34517bb3db5266818d939e64606b82f441ad81946cd7b0631b90dd250fbf5870`  
		Last Modified: Tue, 03 Feb 2026 02:49:36 GMT  
		Size: 53.8 KB (53815 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:38f0379d35a126c00b7d65f23fcbd6608e2f48c83807d1f8217a4602b8a6d7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172375352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa95d21801b4036b3f416a904fb313034fcb7670ac18091f45ebb560449d197`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:59:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 04:59:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:00:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 05:00:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 05:00:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 05:00:24 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 05:00:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:00:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 05:00:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 05:00:35 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 05:00:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 05:00:35 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 03 Feb 2026 05:06:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 05:06:33 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 05:06:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 05:06:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 05:06:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 05:06:34 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 05:06:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 05:06:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 05:06:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 05:06:35 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 05:06:35 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 05:06:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2067247c50ee586cbb200d8226f05fcdcd2f42e6334ae4c7a1237e4974f27da8`  
		Last Modified: Tue, 03 Feb 2026 05:02:11 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94ddbdeb362dc9b15e871349cea403b2d5b0c947796b89ef6c02f249af0304b`  
		Last Modified: Tue, 03 Feb 2026 05:02:11 GMT  
		Size: 7.1 MB (7076665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df226ec6ab28e05688aa44ea38117e503dfb939c29a93e4feb3cf3c6fb6bba0`  
		Last Modified: Tue, 03 Feb 2026 05:02:11 GMT  
		Size: 1.2 MB (1214788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09f5a8b4cbb1a257798fe9778fb752789b44196d95d970fda697a9912746221`  
		Last Modified: Tue, 03 Feb 2026 05:02:11 GMT  
		Size: 8.2 MB (8203993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0a009047e8b1d6fea0f3cb745c3d08e69cc73279dfb9977fddb9ba8c1f7fdf`  
		Last Modified: Tue, 03 Feb 2026 05:02:12 GMT  
		Size: 1.4 MB (1394928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bb216edc5ca1912e97faf441f5114c5659586b5b912b049ce97837c3e05d2a`  
		Last Modified: Tue, 03 Feb 2026 05:02:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f9f462009a8a9f8be02cbb3eca10364467ff555fa297b06b769cc2f087a66e`  
		Last Modified: Tue, 03 Feb 2026 05:02:12 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd7e7a1a3c44d5acc9245a8e231da76483d65eb0d07c83ed23a6478175fa5a`  
		Last Modified: Tue, 03 Feb 2026 05:07:23 GMT  
		Size: 120.9 MB (120864033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7331f454c391bc97a74b1ec509e17346b025f4fde195600fc39a6a582a47b162`  
		Last Modified: Tue, 03 Feb 2026 05:07:20 GMT  
		Size: 10.0 KB (10010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e2a40e180c29861f33cb59e9e50a7f3fb1bba3667a1be03cc09ff1f3167f0d`  
		Last Modified: Tue, 03 Feb 2026 05:07:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ae6e91319d1a0a0c3874663b43748e18572844f6749d39d1f8c11248df8128`  
		Last Modified: Tue, 03 Feb 2026 05:07:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a5b1cbc68d2fc505838d174dffdc72e85d881709372ff54226d88f6bac434d`  
		Last Modified: Tue, 03 Feb 2026 05:07:21 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92288ce1867cbe6971e73c8d828145942080d33cb27cbc32a3954ece1c994d61`  
		Last Modified: Tue, 03 Feb 2026 05:07:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:7de7d8459534a6e321e29254155897bd02f0e905acec7f82675b1bb24a805e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00b46a6f7c8c3c04bc15df87952012afcb2c8bc23275726e2c809de57d6e9aa`

```dockerfile
```

-	Layers:
	-	`sha256:e4a69c24c8f38bf2da6802ae8e5deea754a9920b5d9fef998d3ef7f97f3fd717`  
		Last Modified: Tue, 03 Feb 2026 05:07:20 GMT  
		Size: 5.7 MB (5715337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09a61bd5a49b3bcbd44d00d206e0ddbc539e6879ca0192171f00bf12cbf125cc`  
		Last Modified: Tue, 03 Feb 2026 05:07:20 GMT  
		Size: 53.9 KB (53935 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:7d65f04b3fe25ca7273661adc90f290afa9133c7dfbd7399bd1192d5b4d11abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91561334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bce947f2025993666cbe76bd4c728299ea1df5e236800de3b55ee65b999f2fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 04 Feb 2026 16:13:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 04 Feb 2026 16:14:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 16:15:14 GMT
ENV GOSU_VERSION=1.19
# Wed, 04 Feb 2026 16:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 04 Feb 2026 16:16:15 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 04 Feb 2026 16:16:15 GMT
ENV LANG=en_US.utf8
# Wed, 04 Feb 2026 16:16:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 16:16:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 04 Feb 2026 16:16:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 04 Feb 2026 16:16:58 GMT
ENV PG_MAJOR=16
# Wed, 04 Feb 2026 16:16:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 04 Feb 2026 16:16:58 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Wed, 04 Feb 2026 22:40:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 04 Feb 2026 22:40:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 04 Feb 2026 22:40:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 04 Feb 2026 22:40:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 04 Feb 2026 22:40:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 04 Feb 2026 22:40:10 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 04 Feb 2026 22:40:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 04 Feb 2026 22:40:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 04 Feb 2026 22:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 Feb 2026 22:40:10 GMT
STOPSIGNAL SIGINT
# Wed, 04 Feb 2026 22:40:10 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 04 Feb 2026 22:40:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80995be55917dc7fd201d347bc9226e2f5ac4bf648270056077ffdd82365b78c`  
		Last Modified: Wed, 04 Feb 2026 18:24:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1f5c6b2d99f755313f7c8a99b0dc4359c317ad0b8bf85fa05a15235111d7c2`  
		Last Modified: Wed, 04 Feb 2026 18:24:11 GMT  
		Size: 6.3 MB (6292229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3419a5cae79de9fcd3de7a8c5585cda9f74e580063c21f2ba132beaaf144525a`  
		Last Modified: Wed, 04 Feb 2026 18:24:09 GMT  
		Size: 1.2 MB (1202087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1011f782d19ba43309db24778d82c70cb389a070476ff5dae98b8b45210498d`  
		Last Modified: Wed, 04 Feb 2026 18:24:12 GMT  
		Size: 8.2 MB (8203651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0485b03c21170701329d20fbb35c7b9ca2b9d9a7d4437c48576a357aed50c301`  
		Last Modified: Wed, 04 Feb 2026 18:24:11 GMT  
		Size: 1.4 MB (1402345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055b637555d4df19ff25f1e2fbb73523accc9fa0389284938730df0384953bb`  
		Last Modified: Wed, 04 Feb 2026 18:24:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d5fd337755cc5ee8443095f73c397172e5f877bb14a60fe985381ee14c8dd5`  
		Last Modified: Wed, 04 Feb 2026 18:24:12 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f20f619468b2119ff49a7b0883150405bbbe95a5dacad9bbef9f0ba05b69e`  
		Last Modified: Wed, 04 Feb 2026 22:42:48 GMT  
		Size: 46.2 MB (46163857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ce60d94481e742345138f3b32017136dafcf04dde6b783d3fe992712b7e968`  
		Last Modified: Wed, 04 Feb 2026 22:42:37 GMT  
		Size: 10.0 KB (10024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ecfa3d196785d047c06c4d5e92f88e09a682989045233348a54dc808ad790e`  
		Last Modified: Wed, 04 Feb 2026 22:42:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fd11676bdfc3d8cc0413ed4d3411e62626e69602430be78f25556d4db38ac8`  
		Last Modified: Wed, 04 Feb 2026 22:42:38 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577ea2525e3a30975647a1f887e6bbfb35869cc310bca631b6b9ca843b287380`  
		Last Modified: Wed, 04 Feb 2026 22:42:40 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaeb490264b859eae56e985cc17ad187e42aaa1ed14ba2098d530c4f93f2a0d1`  
		Last Modified: Wed, 04 Feb 2026 22:42:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:bba582ae99b42ba8916e8fee74c6a8f7d6f0b15c11ae8dc0997deefb51549e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5128932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164ff637574f81628bbca10c8248f9ffa3cdbbd95a38f76be93ae73e07c76549`

```dockerfile
```

-	Layers:
	-	`sha256:88a556799de052ab921a00983f0e492c9d9b5924ee8b547a0421540d5439abf6`  
		Last Modified: Wed, 04 Feb 2026 22:42:40 GMT  
		Size: 5.1 MB (5075003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29895acfdc1ba50b416b774a7ea5ac8f8b50a828ec5ae748e0244a12a76476c7`  
		Last Modified: Wed, 04 Feb 2026 22:42:34 GMT  
		Size: 53.9 KB (53929 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:6c4baa6377579e0c1cab85a3a5effc3c69899d05e1ae0aea28a01050a0b92080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174614630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de85226e23661034edfd812218e35564170faed83eaa2893309be78d27e5e6ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:10:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 03 Feb 2026 03:10:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:10:59 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 03:10:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 03:11:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 03 Feb 2026 03:11:04 GMT
ENV LANG=en_US.utf8
# Tue, 03 Feb 2026 03:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:11:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 03:11:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 03:11:08 GMT
ENV PG_MAJOR=16
# Tue, 03 Feb 2026 03:11:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 03 Feb 2026 03:11:08 GMT
ENV PG_VERSION=16.11-1.pgdg13+1
# Tue, 03 Feb 2026 03:35:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 03 Feb 2026 03:35:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 03 Feb 2026 03:35:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 03 Feb 2026 03:35:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 03 Feb 2026 03:35:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 03 Feb 2026 03:35:53 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 03 Feb 2026 03:35:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 03:35:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 03 Feb 2026 03:35:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 03:35:53 GMT
STOPSIGNAL SIGINT
# Tue, 03 Feb 2026 03:35:53 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 03 Feb 2026 03:35:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8077f2bbcfce1aaedf1a064a0e8fd51aebe94ad0ef24c0ff2ddca619fbd173fa`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79287514408b6ef0a85b7d3a863a699fc7122c0b12b45844a562c3208221510`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 6.4 MB (6408759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe5e8fb73d9a4ab10b09d8fd286ff36deb8d8ae34e6f2013352136f379a40f4`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 1.2 MB (1230203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c866b9c8124101d8c7209f17cfd7d182230fddc5fb91850fe69a2dd12caee377`  
		Last Modified: Tue, 03 Feb 2026 03:23:56 GMT  
		Size: 8.3 MB (8258952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b55952f5e10fc188cd69ff85002b0f1dbd437076f36a273875c03c1562589f`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 1.4 MB (1398202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a2d60021e150d93707586195a33ecb491529c20516756048816be04ff66b72`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e42b977764bd402a1c842afa683e87e58284f47b463bdba118c8bd7fa04f0cc`  
		Last Modified: Tue, 03 Feb 2026 03:23:57 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c75ea44c00d1b44e53ea5c3d2304f961173c303a94185d947f5900eef533d8`  
		Last Modified: Tue, 03 Feb 2026 03:36:28 GMT  
		Size: 127.5 MB (127459603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b68b6bd1a7d4db9ba3caaea5f8c4daa9617a4ceae2afd7276ed25c05510aada`  
		Last Modified: Tue, 03 Feb 2026 03:36:25 GMT  
		Size: 10.0 KB (10012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9ff3ecfe2d6c675bcf7414c900f54dfa7aa379b3f8e86dbed1fb56893ee22`  
		Last Modified: Tue, 03 Feb 2026 03:36:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2427cb573e6080be79e5104bdc0c5e8a932a7a6c102f6ec5b338544ebcd730fb`  
		Last Modified: Tue, 03 Feb 2026 03:36:25 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31295c0bbb37b563aa0f3a8e025535e020d1255555528b8a051d31ddc51d133`  
		Last Modified: Tue, 03 Feb 2026 03:36:26 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefe8460638007410445462509c359238131ccc1f055cdc8ef0c54f2f4c138ea`  
		Last Modified: Tue, 03 Feb 2026 03:36:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:80ee84ebfec187883ab99034ac4bd890e990766e7d14101481b5dc36352f49d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76489aef2a77791fe7fd16b40de42232cd500ecac552067e70a0b618fc9b5b72`

```dockerfile
```

-	Layers:
	-	`sha256:240308a8d407e0c0392258b12089bfc07cb0c4492c60a26fbb109b20ff91c6cf`  
		Last Modified: Tue, 03 Feb 2026 03:36:25 GMT  
		Size: 5.7 MB (5725393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f37ef924b1f22a860871e5a0182dff52c686e848f0d92c3d2d7326264c45f49a`  
		Last Modified: Tue, 03 Feb 2026 03:36:25 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json
