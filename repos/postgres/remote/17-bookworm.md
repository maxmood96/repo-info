## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:843ed200ecf366172737a800294fba2405abc80590c79f75af16f9a1ed54b167
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
$ docker pull postgres@sha256:dc92145efc675e474af72c5d8cb4522d70271f409a5347d51cf6dd75b833f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156018507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9c77a7728a3ea8ecf3dbaf1dcd1219c297d4791d37c7a29889c58416780c1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:51:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 13 Jan 2026 01:51:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:51:16 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 01:51:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 01:51:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 13 Jan 2026 01:51:20 GMT
ENV LANG=en_US.utf8
# Tue, 13 Jan 2026 01:51:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:51:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 01:51:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 01:51:24 GMT
ENV PG_MAJOR=17
# Tue, 13 Jan 2026 01:51:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 13 Jan 2026 01:51:24 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 13 Jan 2026 01:51:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 13 Jan 2026 01:51:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 13 Jan 2026 01:51:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 13 Jan 2026 01:51:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Jan 2026 01:51:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 13 Jan 2026 01:51:35 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Jan 2026 01:51:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:51:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 13 Jan 2026 01:51:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:51:35 GMT
STOPSIGNAL SIGINT
# Tue, 13 Jan 2026 01:51:35 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 13 Jan 2026 01:51:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae319c955d01efcb523a9992ba82823c1a4eea15f3f2fe4ba011eed0ccc0a6ad`  
		Last Modified: Tue, 13 Jan 2026 01:51:54 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f47e179aebad1eb7ac66518e840fb762ee56293cbb0bd16c01eb9312e97226`  
		Last Modified: Tue, 13 Jan 2026 01:52:05 GMT  
		Size: 4.5 MB (4534280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1352abe9469198d6b331f2cee126ec4f7c9eec884e0618a13652c4950dc10b`  
		Last Modified: Tue, 13 Jan 2026 01:52:05 GMT  
		Size: 1.2 MB (1249548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906c3e6a56756473200dff156e2fe443e8b64ebf7d5bf7f55ae2d15e0b3eb2c7`  
		Last Modified: Tue, 13 Jan 2026 01:51:54 GMT  
		Size: 8.1 MB (8066504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad6d9831a37f3b5f24c591104ab5644797aa938d0a165ff92a396e613b6e5fd`  
		Last Modified: Tue, 13 Jan 2026 01:52:05 GMT  
		Size: 1.2 MB (1196417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37062b4a6b30067ac25e94c0c90b6756c051366c0a9574fb389b0b2d808737e6`  
		Last Modified: Tue, 13 Jan 2026 01:52:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d295fd06e33ee0425f2d62cea06bfef17ec1c94b49bec58b15db314cc8495d`  
		Last Modified: Tue, 13 Jan 2026 01:52:05 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05576011220075350874324ce56ca5f3cd04e8a487486ea3eb32f4027f6897b7`  
		Last Modified: Tue, 13 Jan 2026 01:52:12 GMT  
		Size: 112.7 MB (112722211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae48a22e155beac935511780169a0ed72d2c01e356de857ee852fa7eb919b7b4`  
		Last Modified: Tue, 13 Jan 2026 01:51:56 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefc97776c9dedf7243bf46e52b6d6f0ce1717c8e68457780dfe66ea3b59b03c`  
		Last Modified: Tue, 13 Jan 2026 01:52:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49955792ca012f504f0b5eabbc0eb746b17f6f82e757d7d01a148832053016e8`  
		Last Modified: Tue, 13 Jan 2026 01:51:57 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472d8dde329daffd45cc55638a8813717fe3f3253996d8d699989e78a09de8ae`  
		Last Modified: Tue, 13 Jan 2026 01:52:05 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e817eaa94eb6438938854c116145a3f579840762af7090dc1bc7ca287fe36ae1`  
		Last Modified: Tue, 13 Jan 2026 01:52:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a193ab98ccb60cafdbbc4fb8b8cecf3f5df234fa57a0fb5453ec213b40b1e240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f8689061a0f5d0078713c7d3472c841726e7b21595b89c6b3a80725f47392a`

```dockerfile
```

-	Layers:
	-	`sha256:be840f775f7724c74a6083626dd72918ef7907389129995362d6f61869aeaaad`  
		Last Modified: Tue, 13 Jan 2026 01:51:54 GMT  
		Size: 5.9 MB (5927466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3293b76263fd0131c1aaf43b840ae91eff729188b04fa7f50aff9c4f20ad43c9`  
		Last Modified: Tue, 13 Jan 2026 01:51:54 GMT  
		Size: 53.3 KB (53290 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:067abf495410e8f5844bfd64827d3f86104a3c48570ee6367950e995699e68fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149053746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cdd1e49aaab5004a180b886686877f60de5d2495d5bb6397e495b3da5c4be6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:07:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 13 Jan 2026 02:07:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:07:46 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 02:07:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:07:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 13 Jan 2026 02:07:53 GMT
ENV LANG=en_US.utf8
# Tue, 13 Jan 2026 02:07:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:07:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 02:07:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:07:59 GMT
ENV PG_MAJOR=17
# Tue, 13 Jan 2026 02:07:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 13 Jan 2026 02:07:59 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 13 Jan 2026 02:24:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 13 Jan 2026 02:24:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 13 Jan 2026 02:24:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 13 Jan 2026 02:24:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Jan 2026 02:24:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 13 Jan 2026 02:24:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Jan 2026 02:24:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:24:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 13 Jan 2026 02:24:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:24:02 GMT
STOPSIGNAL SIGINT
# Tue, 13 Jan 2026 02:24:02 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 13 Jan 2026 02:24:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:43595593b17008d0147d9ea53c9ed04f4ec8fde216c1d359e2de9daa9e0665f6`  
		Last Modified: Tue, 13 Jan 2026 00:41:45 GMT  
		Size: 25.8 MB (25757697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa0931a44c9aa0d67fdb317b58163540a2add315c6f07ea29e6ce5373ca0bd9`  
		Last Modified: Tue, 13 Jan 2026 02:24:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7508660611f2925d04657de2695d183c63211ee0a8a335d817dce31dbeaae9`  
		Last Modified: Tue, 13 Jan 2026 02:24:22 GMT  
		Size: 4.2 MB (4151296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20810556eaf08c9cf4144a4abd31f5e8ad1113d0e746125b9a36681b965f8cc4`  
		Last Modified: Tue, 13 Jan 2026 02:24:22 GMT  
		Size: 1.2 MB (1220120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ba103137091ca080f18a8acba035096b640779e00635bad38739e6d2af3063`  
		Last Modified: Tue, 13 Jan 2026 02:24:22 GMT  
		Size: 8.1 MB (8066637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102ebcdaec4a59be809008b5d4fdb05b13da5824ba27ea7149fbd7692501014b`  
		Last Modified: Tue, 13 Jan 2026 02:24:23 GMT  
		Size: 1.2 MB (1195078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184697d50b9a41e6688f9edcc81aab34b2389161109e72c2be5ecd24472d1582`  
		Last Modified: Tue, 13 Jan 2026 02:24:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6df8dacf56447de19587c4be6facc0d81cb1dea0f197f7bfc01d6a8c6058a5`  
		Last Modified: Tue, 13 Jan 2026 02:24:32 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3f4746fb6ccb9d03c4de67c94c84cdb1c332af0ca966efb4d36994d1a9ae61`  
		Last Modified: Tue, 13 Jan 2026 02:24:37 GMT  
		Size: 108.6 MB (108641942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c241fc12a14ffc1b8cbcbd9857cf968c5f0c17288fe43622fbb065df5668e0fb`  
		Last Modified: Tue, 13 Jan 2026 02:24:24 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c0c93c3349a845d99b13bc20f9bbc79c63d93aa15e5560979a818621ae5859`  
		Last Modified: Tue, 13 Jan 2026 02:24:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce04309e07155a405b51952efd9a968e61bcfd05afdd9ab5b873b9e8ebd277d`  
		Last Modified: Tue, 13 Jan 2026 02:24:24 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b632d141ded96f159745b2bba5e55410b16e52eee6a12fb3ecbea649900d5de4`  
		Last Modified: Tue, 13 Jan 2026 02:24:25 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2d6e0397efba50d37bbb9c794fc291780019a26b99677a6b9738e1fde80055`  
		Last Modified: Tue, 13 Jan 2026 02:24:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:944d9da7d0ee9d7f433542321b54ab89667fb6db539305754f8ee6c656a9efe1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d54dacb030e6d78fad20c718280dd14089f3409df0e0bfe3cba46f69575fa5`

```dockerfile
```

-	Layers:
	-	`sha256:defaaebb9f17209d6fe1c2b849a66151cc3b18112c2a9e4976b9fd213c7bda8d`  
		Last Modified: Tue, 13 Jan 2026 06:12:19 GMT  
		Size: 5.9 MB (5945781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62c1450d87c2330f77290c92419e351ed3b8fa3a4de5fa70435a1354404bda7`  
		Last Modified: Tue, 13 Jan 2026 06:12:20 GMT  
		Size: 53.5 KB (53497 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:819181ae89923eafe02eadbc90df3fc4b8495ff0751064c680ef1872d71764e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144057423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413332a49d5bcb98263c587123d9494fc6d623aedd6fed8efadcf7202a2a2531`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:29:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 13 Jan 2026 02:29:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 02:29:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 02:29:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 13 Jan 2026 02:29:45 GMT
ENV LANG=en_US.utf8
# Tue, 13 Jan 2026 02:29:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 02:29:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:29:50 GMT
ENV PG_MAJOR=17
# Tue, 13 Jan 2026 02:29:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 13 Jan 2026 02:29:50 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 13 Jan 2026 02:45:04 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 13 Jan 2026 02:45:04 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 13 Jan 2026 02:45:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 13 Jan 2026 02:45:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Jan 2026 02:45:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 13 Jan 2026 02:45:04 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Jan 2026 02:45:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:45:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 13 Jan 2026 02:45:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:45:04 GMT
STOPSIGNAL SIGINT
# Tue, 13 Jan 2026 02:45:04 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 13 Jan 2026 02:45:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc2afc22aaaaca4fb17aec9f06268ecf8df18459bf42052c575b2f1456fe761`  
		Last Modified: Tue, 13 Jan 2026 02:45:22 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78751eb17a3ba3479ffde3d41d35a4e7b93bcabb34365233ad741f8ef5d60f4`  
		Last Modified: Tue, 13 Jan 2026 02:45:33 GMT  
		Size: 3.7 MB (3742674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ab4c49f660649fd34d4b60e24a17b447cd6d57628d2f4e8d075a9409a6bcd0`  
		Last Modified: Tue, 13 Jan 2026 02:45:33 GMT  
		Size: 1.2 MB (1215978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7b4246a95a8a7c201e671f7288ae44af23c6666727181f5d04c314de634189`  
		Last Modified: Tue, 13 Jan 2026 02:45:33 GMT  
		Size: 8.1 MB (8066431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06fb14daa3661e8835cb386f2185db4feb5bd4dbaf1d5aee9ea31b61ffddb6c`  
		Last Modified: Tue, 13 Jan 2026 02:45:23 GMT  
		Size: 1.1 MB (1067288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962bd3af5e017df481deba9e037501d443c120e619983cd27c04ce02b060d3b1`  
		Last Modified: Tue, 13 Jan 2026 02:45:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fc1e09be7c03b0029f12e30b0a225ccc891ac3cf5ce5db0d1f665aae0acacb`  
		Last Modified: Tue, 13 Jan 2026 02:45:33 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23812dd28fea02796d703a01d420c985b1ee7b3be5a06029489219a0a91a8416`  
		Last Modified: Tue, 13 Jan 2026 02:45:43 GMT  
		Size: 106.0 MB (106009952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8153ff58427498a1d78a3bbea9a4b9be942de0781eb835e76284ec9ee9cb40c`  
		Last Modified: Tue, 13 Jan 2026 02:45:25 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e306269b96fbb8dc2416aa924aed1cd9698ab734d779b2b2db822c2b8fe77031`  
		Last Modified: Tue, 13 Jan 2026 02:45:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f060b4a9414d38dcf8087a4b94fc058bb587b94f624b6f179f9b38e540e6d8`  
		Last Modified: Tue, 13 Jan 2026 02:45:25 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c331f507d7f2d176c4836a1f8c92ba665328d269ccc9e3c0be1d96c5453732`  
		Last Modified: Tue, 13 Jan 2026 02:45:33 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd20d3f7bac29a7f1490195ebc2f7a3b297451e89732f6dc546751ddc8f3c364`  
		Last Modified: Tue, 13 Jan 2026 02:45:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e48b44057b8127e43f85843bd54523cd901d8cb0fd6cad581b814124478a78e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8e3cd24cfc213f86a211b7b3025d6f857b1b083afb65aa962224d3916a4956`

```dockerfile
```

-	Layers:
	-	`sha256:1cf7f4a1b06e0f1ab52c060089d2b469d25b3a29ee1fdf9b05313b5e229fa144`  
		Last Modified: Tue, 13 Jan 2026 02:45:23 GMT  
		Size: 5.9 MB (5945036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53e4b042d5fd9625bb41e731c1dcd87527aa6101cdce68e5352043947f6e415`  
		Last Modified: Tue, 13 Jan 2026 06:12:31 GMT  
		Size: 53.5 KB (53495 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:ea44ee86a6b5abe60eeb75e4158392b3ba26eb2904b525ba651d803ecf0a8325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154019849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864f67d49f274ea31e03631674668f7fd6a99c2a96fc57622a33dbbb66b54a00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:53:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 13 Jan 2026 01:54:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:54:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 01:54:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 01:54:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 13 Jan 2026 01:54:11 GMT
ENV LANG=en_US.utf8
# Tue, 13 Jan 2026 01:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:54:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 01:54:15 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 01:54:15 GMT
ENV PG_MAJOR=17
# Tue, 13 Jan 2026 01:54:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 13 Jan 2026 01:54:15 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 13 Jan 2026 01:54:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 13 Jan 2026 01:54:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 13 Jan 2026 01:54:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 13 Jan 2026 01:54:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Jan 2026 01:54:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 13 Jan 2026 01:54:29 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Jan 2026 01:54:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:54:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 13 Jan 2026 01:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:54:29 GMT
STOPSIGNAL SIGINT
# Tue, 13 Jan 2026 01:54:29 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 13 Jan 2026 01:54:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac696c4e44591c5c7027410ce7481735ae55dd4f0f69b69d8c260bb55e415eb9`  
		Last Modified: Tue, 13 Jan 2026 01:55:00 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee54852a293cdf114097284d9cc5758561ff6bcf9b58686f34548fb22091206e`  
		Last Modified: Tue, 13 Jan 2026 01:54:48 GMT  
		Size: 4.5 MB (4519584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0509cab8ab34a6e78e4808356de50e4425c2c1fa83e71829160f187004434aa`  
		Last Modified: Tue, 13 Jan 2026 01:54:48 GMT  
		Size: 1.2 MB (1203333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed25ff2c567dd6dd4e4478a274a79a0f2226adebf8e4345ceabef24d6b352b8`  
		Last Modified: Tue, 13 Jan 2026 01:54:49 GMT  
		Size: 8.1 MB (8066590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e59764b509eb9269609bbbf1a9e244e3139195e4b9aee4e9a45939f451a475`  
		Last Modified: Tue, 13 Jan 2026 01:54:50 GMT  
		Size: 1.1 MB (1109032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3148207f49bf32831ce766f109ab7f4341d972f230c0ef23eac13add57049f36`  
		Last Modified: Tue, 13 Jan 2026 01:54:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f519daf18accdbadef462d0d3bf7590139bc544dabb1af210ed759b89dc614e`  
		Last Modified: Tue, 13 Jan 2026 01:54:50 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa92534c12a06d1548db427a5f5b3c8285ba0ebf574d988779c6a6c6a55343ee`  
		Last Modified: Tue, 13 Jan 2026 01:55:13 GMT  
		Size: 111.0 MB (110992441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be03f1f0ebeff6b9a43d3d0581d374e78cc19dc31076b28e68a3a6f93d10190`  
		Last Modified: Tue, 13 Jan 2026 01:54:51 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176c9a5795324463e6ca2ef968b4e52a33d59fe49ed8cb8d8d664c51b9e70127`  
		Last Modified: Tue, 13 Jan 2026 01:54:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a67a9a8c4a841dddace8b322782c16805729491e7ec8d1495156e9ced8524f0`  
		Last Modified: Tue, 13 Jan 2026 01:54:51 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b95df3e3785edb02e5a2100d1820d1483237a04742a88af22fe33cb94504c9`  
		Last Modified: Tue, 13 Jan 2026 01:54:52 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419986e2877f0a67ce44055687a9481454d72a567b0855d8931458e9663047f2`  
		Last Modified: Tue, 13 Jan 2026 01:54:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6dd02c686d20c97977328ed32984ff43ab596dcad4dbb4a6dad19c487b8d75b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5987312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefec99e42443551ba91b9aeb6b3297c28a831c44db8de593f1610ba24d83411`

```dockerfile
```

-	Layers:
	-	`sha256:78e29c750bedd0dc80cdafaf95aa8c193ba3845ebc4b890aacec62320089a63e`  
		Last Modified: Tue, 13 Jan 2026 01:54:49 GMT  
		Size: 5.9 MB (5933777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0e7182b8d781f13a2c7f56afa30753fdb766abb11982ac83e1e909dc27d5fc`  
		Last Modified: Tue, 13 Jan 2026 03:12:09 GMT  
		Size: 53.5 KB (53535 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:7138048b5a37ebb1a7413041da61a658166761a65e8bbe9280db70238d8a8180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164892289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86045f5f7deda7cb0621348fcdca592343edb93fbb5999683874b31821a50a34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:48:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 13 Jan 2026 01:48:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:48:40 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 01:48:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 01:48:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 13 Jan 2026 01:48:45 GMT
ENV LANG=en_US.utf8
# Tue, 13 Jan 2026 01:48:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:48:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 01:48:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 01:48:49 GMT
ENV PG_MAJOR=17
# Tue, 13 Jan 2026 01:48:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 13 Jan 2026 01:48:49 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 13 Jan 2026 02:00:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 13 Jan 2026 02:00:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 13 Jan 2026 02:00:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 13 Jan 2026 02:00:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Jan 2026 02:00:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 13 Jan 2026 02:00:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Jan 2026 02:00:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:00:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 13 Jan 2026 02:00:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:00:06 GMT
STOPSIGNAL SIGINT
# Tue, 13 Jan 2026 02:00:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 13 Jan 2026 02:00:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:45 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993d15b49e42a4c25b67416cba90369ea4fce560edd4d7d1ef5ce7b2b3c7c451`  
		Last Modified: Tue, 13 Jan 2026 02:00:40 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b28d1a0c49f2930d24010c6ffcb9f37deb24b14637cbf2f3bd68c8805dbdac8`  
		Last Modified: Tue, 13 Jan 2026 02:00:41 GMT  
		Size: 5.0 MB (4966105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22c3588b82308b1a0f46f042f6dacb2165fb945921cfe76a08db67846ddf449`  
		Last Modified: Tue, 13 Jan 2026 02:00:26 GMT  
		Size: 1.2 MB (1218653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f31ff61a06db978a5eac59405f091435435440ac3c61b2410ea065a83b00f77`  
		Last Modified: Tue, 13 Jan 2026 02:00:41 GMT  
		Size: 8.1 MB (8066485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6053f6d7d5e81ed53b3982984ec115e4a9470a174226bc9f784fdd22f9e734da`  
		Last Modified: Tue, 13 Jan 2026 02:00:40 GMT  
		Size: 1.1 MB (1137461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eab2353363f4843edf61d772b75ff0ece2f1350e2d40d4972b332efc170835`  
		Last Modified: Tue, 13 Jan 2026 02:00:40 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa4c840220cc2f6642c9c8939af208336d5ea8a1be2b594cc9390da7ec5c8b6`  
		Last Modified: Tue, 13 Jan 2026 02:00:40 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaf12c5d7ee9aadccc03c0c11ae2a81f459dbe30cce0f96c032ff2cd026d99d`  
		Last Modified: Tue, 13 Jan 2026 02:00:33 GMT  
		Size: 120.3 MB (120272542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c3e9c0301f1832e8d95495eb8f26a430a2589b2147911e6ba5674f9f89ac97`  
		Last Modified: Tue, 13 Jan 2026 02:00:29 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442f29d87394fb6978358bd76d4220be0cedef556c9d4f6dc271bc22c8ec4272`  
		Last Modified: Tue, 13 Jan 2026 02:00:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d02d4480a1cef40e2a86b12f04be1510c1a7ab2a92f4fc0c4f50fd71861f29d`  
		Last Modified: Tue, 13 Jan 2026 02:00:30 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a528ce8f4946ae4747cd351ef504c9cb9a62b2b873868d1d55fe88bad09d644a`  
		Last Modified: Tue, 13 Jan 2026 02:00:40 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04db7e65685817d3451260a4f0096669bc3f4b7e433cbec6bbe6f37fb64e2e2`  
		Last Modified: Tue, 13 Jan 2026 02:00:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ca18d618d87e006fe166964b40dc3aa1068f89b0a792377f12e7afe4cc7510c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5997169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b571e2081364edb70afe28a6c3660053f207c06dce82403f4c8a7724e036478`

```dockerfile
```

-	Layers:
	-	`sha256:826c4f74dd412b317286a6ceb772641a46a61e7a359932bc28946e3a66186686`  
		Last Modified: Tue, 13 Jan 2026 02:00:27 GMT  
		Size: 5.9 MB (5943924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7458e1c7e02f9fb0dd5de29deaac1a29cb9d9e5bc475a1971659a4428dc8ddeb`  
		Last Modified: Tue, 13 Jan 2026 03:12:17 GMT  
		Size: 53.2 KB (53245 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:aad68369c959c0ebe50528c02354eae6be626ae560a51683102eb99bfeee8500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154912311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83582ff6662cb500ac1eb206242197499f82a98f73b9740074cec76e53da84ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 09:47:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 13 Jan 2026 09:48:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 09:48:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 09:48:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 09:48:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 13 Jan 2026 09:48:58 GMT
ENV LANG=en_US.utf8
# Tue, 13 Jan 2026 09:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 09:49:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 09:49:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 09:49:18 GMT
ENV PG_MAJOR=17
# Tue, 13 Jan 2026 09:49:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 13 Jan 2026 09:49:18 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 13 Jan 2026 12:11:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 13 Jan 2026 12:11:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 13 Jan 2026 12:11:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 13 Jan 2026 12:11:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Jan 2026 12:11:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 13 Jan 2026 12:11:48 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Jan 2026 12:11:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 12:11:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 13 Jan 2026 12:11:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 12:11:52 GMT
STOPSIGNAL SIGINT
# Tue, 13 Jan 2026 12:11:52 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 13 Jan 2026 12:11:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c063a3c188d3088513ac303ee5a03a6c0ddff0d68a1e46804a822134a25bf8e8`  
		Last Modified: Tue, 13 Jan 2026 00:41:02 GMT  
		Size: 28.5 MB (28513755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339e9ab3af1db9f40e903a13293484c6639ecac659abd88fe7f0c37da730bfe0`  
		Last Modified: Tue, 13 Jan 2026 11:02:11 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ecd690564db6ac2314f3c383d0a9172576668537ac867fa57cd8ca6034f87b`  
		Last Modified: Tue, 13 Jan 2026 11:02:11 GMT  
		Size: 4.5 MB (4475215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e08ceec408c61d1be72d62dfdcec7a5ad643b65981db3c69ed60a9836063bc4`  
		Last Modified: Tue, 13 Jan 2026 11:02:11 GMT  
		Size: 1.2 MB (1159209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e4282ae4fbe52f50f855a92fcec567b8f0027dd7070ad1df9fd4b50e99fa39`  
		Last Modified: Tue, 13 Jan 2026 11:02:12 GMT  
		Size: 8.1 MB (8066557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c93c193d98815f669c859c5d9b63986a5ede4d9bfa4a10cbad1a0f5c55909be`  
		Last Modified: Tue, 13 Jan 2026 11:01:49 GMT  
		Size: 1.2 MB (1182917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401bebc4528724511f617e5220c40e53ee83b546a03000d42761b9d3a05de32f`  
		Last Modified: Tue, 13 Jan 2026 11:02:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67553a0ece38a82852308297cb7b292c9273c4aa43d5ed1a2a1eb30764848a70`  
		Last Modified: Tue, 13 Jan 2026 11:01:50 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1aef28a6f0a08c89249b6031a6c962c6eef3e110d6df568952ea6130261b85`  
		Last Modified: Tue, 13 Jan 2026 12:14:19 GMT  
		Size: 111.5 MB (111493669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914b2e5a81e06e9ba1337594297cefd9763984d37e863aab07dce0e47a3ab0af`  
		Last Modified: Tue, 13 Jan 2026 12:14:07 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3507f4d879a9d3f0f2034d016e25cbd4fcb6aa420db38ee8da96512e8524e42`  
		Last Modified: Tue, 13 Jan 2026 12:14:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d340f0f896ceac70f2178e7d4dd217460538d580fc84cf58026384c895cf3573`  
		Last Modified: Tue, 13 Jan 2026 12:13:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc0d4e103156ab07d2e6cbc07ac833a386a7699b6a00af64e441676b19f6ec5`  
		Last Modified: Tue, 13 Jan 2026 12:14:07 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9929027c5b1aa9ad4beb196d356b92a27c26ced7567366645488a687a7683e`  
		Last Modified: Tue, 13 Jan 2026 12:14:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9a72f516bfc1f4a101b8164a7477471e0195d0c3495ce4358cd02d45ae1a481e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c4f4d03ff59e8d8c757ee8ae419a5ef4553fc3206b49d2b7b507c3300a3e8a`

```dockerfile
```

-	Layers:
	-	`sha256:1a3ff2e2616a77ae3d70b1b3baa7de786fd9adb265ea16eeee47b5844827c009`  
		Last Modified: Tue, 13 Jan 2026 15:09:34 GMT  
		Size: 53.2 KB (53156 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:4aac5154890888e5cafafedaed87c2a21c0a0df90f74c1e4c7d426337f94fc1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168835054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9013f79e9d06df00739c02db79ed5da59ba63da4a7bdcb1cc01ddbad0b2e99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 00:41:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 14 Jan 2026 00:42:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 00:42:19 GMT
ENV GOSU_VERSION=1.19
# Wed, 14 Jan 2026 00:42:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 14 Jan 2026 00:42:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 14 Jan 2026 00:42:29 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jan 2026 00:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 00:42:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 14 Jan 2026 00:42:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 14 Jan 2026 00:42:39 GMT
ENV PG_MAJOR=17
# Wed, 14 Jan 2026 00:42:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 14 Jan 2026 00:42:39 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Wed, 14 Jan 2026 00:45:45 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 14 Jan 2026 00:45:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 14 Jan 2026 00:45:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 14 Jan 2026 00:45:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jan 2026 00:45:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 14 Jan 2026 00:45:49 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jan 2026 00:45:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 14 Jan 2026 00:45:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 14 Jan 2026 00:45:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jan 2026 00:45:51 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jan 2026 00:45:51 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 14 Jan 2026 00:45:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95be2544d79a8e44ff8538c0428b9fd57b633940c66d25d6d9b3f983d77ec165`  
		Last Modified: Wed, 14 Jan 2026 00:44:37 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f47bf5565ad24082ccc467e9e8159080547146057ee8b1d081ee4635a57bce`  
		Last Modified: Wed, 14 Jan 2026 00:44:38 GMT  
		Size: 5.4 MB (5368611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d52dc6bc72ab97943feef2561be8618c157bccde1ea17c9c86650c524d51ed3`  
		Last Modified: Wed, 14 Jan 2026 00:44:37 GMT  
		Size: 1.2 MB (1208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fa1c4fc4697a8e38e765f8b710fe1b3236aabf5eb17abebddd9586e4a62ca5`  
		Last Modified: Wed, 14 Jan 2026 00:44:38 GMT  
		Size: 8.1 MB (8066604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac945fdaeb3a636296cb5c3d42f50d9023ab06d12d36d00b5e5968166d0ced34`  
		Last Modified: Wed, 14 Jan 2026 00:44:27 GMT  
		Size: 1.3 MB (1283666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c8ddcb62ef12ef971c1a41b5951787457878f9d55b67cde3454c615e0378e6`  
		Last Modified: Wed, 14 Jan 2026 00:44:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1318b0bd3bb31f0194757280dcb9291b40bf225d0483f136d97919489bf1032d`  
		Last Modified: Wed, 14 Jan 2026 00:44:27 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1d0aefcb4555c3e2f5ba26e7feb6cff262425f4595d37e0e0954eb983c4eed`  
		Last Modified: Wed, 14 Jan 2026 00:46:51 GMT  
		Size: 120.8 MB (120818269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f05f60ef8a4bfcc92c6853bf346803326346631badf9af792fd01fb8deb8d`  
		Last Modified: Wed, 14 Jan 2026 00:46:47 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa3a5881edbbc8762a5108012a2b0de9abe07107751650fa0c672810efb123d`  
		Last Modified: Wed, 14 Jan 2026 00:46:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21907de1c98c10ce4eff8316cbeb976ed5eaf3e193f8401081907fa99ff8488`  
		Last Modified: Wed, 14 Jan 2026 00:46:56 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980cf78c6cb98c843b9fd2e92d802f59a5913dfa90a9282ee4652ff707a5b154`  
		Last Modified: Wed, 14 Jan 2026 00:46:56 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4afc37d186dacb97c4ea890c863bc00eca3be744bbb0f8914749da1b0e16404`  
		Last Modified: Wed, 14 Jan 2026 00:46:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:53a89d00ac1d18b1a7c1eb436b17df8f5130258e66302599a17b6ee0622574be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae07fd4518c70befaaebbcceeb861331926f085d360bbd3091d14680da3b65`

```dockerfile
```

-	Layers:
	-	`sha256:f1b0f7a26a773121417ecf46a2a726a6166306868a0bc6e648319259a77457ef`  
		Last Modified: Wed, 14 Jan 2026 00:46:47 GMT  
		Size: 5.9 MB (5934827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e93f727a2adc666c9d4443f5aded1cd1b987c5f9774539d0e636f5f180b7c911`  
		Last Modified: Wed, 14 Jan 2026 03:21:02 GMT  
		Size: 53.3 KB (53343 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:397b1a0c1fcdc47be3ee0eff1be8242d31c0fb611d7fa2f9f33c207c80a28488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165302073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5172b6e293412c21ab4db1b9f3a21cd5fb0440d37e08a36b865a8817c3624a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:48:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 13 Jan 2026 01:48:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:48:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 13 Jan 2026 01:48:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 13 Jan 2026 01:48:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 13 Jan 2026 01:48:25 GMT
ENV LANG=en_US.utf8
# Tue, 13 Jan 2026 01:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:48:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 13 Jan 2026 01:48:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 01:48:29 GMT
ENV PG_MAJOR=17
# Tue, 13 Jan 2026 01:48:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 13 Jan 2026 01:48:29 GMT
ENV PG_VERSION=17.7-3.pgdg12+1
# Tue, 13 Jan 2026 02:00:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 13 Jan 2026 02:00:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 13 Jan 2026 02:00:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 13 Jan 2026 02:00:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Jan 2026 02:00:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 13 Jan 2026 02:00:55 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Jan 2026 02:00:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 02:00:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 13 Jan 2026 02:00:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 02:00:56 GMT
STOPSIGNAL SIGINT
# Tue, 13 Jan 2026 02:00:56 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 13 Jan 2026 02:00:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:08 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d528ca50261fee4732a99b00e2a67ba63fcba29300c334653475287b4c0df321`  
		Last Modified: Tue, 13 Jan 2026 02:01:25 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8442bfeeb52d76050426cb8b293ec4fc73cc65f57b9ad050689c5ae18900f6`  
		Last Modified: Tue, 13 Jan 2026 02:01:25 GMT  
		Size: 4.4 MB (4391236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b035b11bca4f27c82922f2b1ec10790ce54ceafe6a56c32ab2c7c58834b5562`  
		Last Modified: Tue, 13 Jan 2026 02:01:13 GMT  
		Size: 1.2 MB (1222841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394d1a7a296b44de2b21f7b58081096eb128cd2411089d2cb8134135b9eee9c0`  
		Last Modified: Tue, 13 Jan 2026 02:01:14 GMT  
		Size: 8.1 MB (8120735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ab514eadde31c65abc84e6e25b1eac20a2a534cfb0f0d11ba30436ab0e9c61`  
		Last Modified: Tue, 13 Jan 2026 02:01:14 GMT  
		Size: 1.1 MB (1097063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142b1bd4fd5c8756ea4b639ad152e9fdf4b022661670452e9add0cfcac9f3c80`  
		Last Modified: Tue, 13 Jan 2026 02:01:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5393134c3189d4180b8a4e294c89e6467533e33e10fa0ed97b0d2e8f2d01d0e`  
		Last Modified: Tue, 13 Jan 2026 02:01:25 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072881081370cfe1400bfcfd3bc2dbfee9cb7e5c748f62799679cf366da25bed`  
		Last Modified: Tue, 13 Jan 2026 02:01:47 GMT  
		Size: 123.6 MB (123564793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3242bc14a5fac97eca5a509fa76aa3d7ee6c2dcdea63862ab3fb377861413f`  
		Last Modified: Tue, 13 Jan 2026 02:01:25 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fec5e1696db70774918c8ed5eda3bc3303f30c7780abbf82f03aaa0c9e3ed7`  
		Last Modified: Tue, 13 Jan 2026 02:01:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e8da98e6071df15754d925f1efdc9ebb3ccdab1d280a5dbe24f95af4f67e6c`  
		Last Modified: Tue, 13 Jan 2026 02:01:25 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd356c17e7c4c149c13727c813b4f3a2fb384a2af390a955fc1e0baedf3dcc56`  
		Last Modified: Tue, 13 Jan 2026 02:01:26 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efc9076a377e1b2fbb0a6a7a6a34e62dcb82f19af7bdd162679b4e12351508c`  
		Last Modified: Tue, 13 Jan 2026 02:01:26 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9e3e03338049e29744c6009d45fdc36e8510b7ed1a0bae53faeed15f42c000dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5993689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06060907d19d90217a68f7d878f251f41d48c9c139a7c0c7e170fa0dfa247025`

```dockerfile
```

-	Layers:
	-	`sha256:34ecde195595fb293c583f36d6e8d8648375df2a6ad76f3808296243e2b424dc`  
		Last Modified: Tue, 13 Jan 2026 02:01:25 GMT  
		Size: 5.9 MB (5940400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d2996666aa04c525b1bb2d9bcf9ee57a9a0ddb70167cf12121619f7486649ca`  
		Last Modified: Tue, 13 Jan 2026 02:01:25 GMT  
		Size: 53.3 KB (53289 bytes)  
		MIME: application/vnd.in-toto+json
