## `postgres:18-bookworm`

```console
$ docker pull postgres@sha256:38959036803bc33fe5236916199d441d16e29bf3134ae1c9b99c623f15b2ec5c
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
$ docker pull postgres@sha256:e3929b193fbe15a68a756e5417612351da743babeea56c6044ff68719ce595ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157012678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ee61064788a2033ba77445855ec4ebfe78b1a19f626ae58862522ceefd92ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV LANG=en_US.utf8
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_MAJOR=18
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=18.0-1.pgdg12+3
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 15 Oct 2025 18:23:03 GMT
VOLUME [/var/lib/postgresql]
# Wed, 15 Oct 2025 18:23:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Oct 2025 18:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Oct 2025 18:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e38e7a012f264407f9b9c29ea886e2fe59f9a6c3571cb64c232643725d50e40`  
		Last Modified: Wed, 22 Oct 2025 17:39:51 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa302e29182e5729df23295af8cab6cc84560d09e0f4b50c51ccaaf4a10c8ad`  
		Last Modified: Wed, 22 Oct 2025 17:39:52 GMT  
		Size: 4.5 MB (4534085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11f61ba5cebc56e43471c1bec22fb4a27be14147cf5ceb5bcb49d99ddfb6f39`  
		Last Modified: Wed, 22 Oct 2025 17:39:52 GMT  
		Size: 1.2 MB (1249503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1832cbd0d61c3effb337d86e23120358b289e89b1de4fec8ae0064624541ab77`  
		Last Modified: Wed, 22 Oct 2025 17:39:53 GMT  
		Size: 8.1 MB (8066470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6104b07a1cdcd5ed334ad0c0bb49785477df2013c9e2cc7fdbb617a03dbb080f`  
		Last Modified: Wed, 22 Oct 2025 17:39:51 GMT  
		Size: 1.2 MB (1196393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574f78662f16e45cc178b8d33c5de91789fe37b8452c24a6dafabd7461930d96`  
		Last Modified: Wed, 22 Oct 2025 17:39:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c435b8ccaa5b4445c4c1999c68738e49d1ae83af5b152da53c876df01fb067`  
		Last Modified: Wed, 22 Oct 2025 17:39:51 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ccb5ab51d74c7327c3a7cb1c77b0dbd6b77e31a15f9e1d925461bc8ebc9f1f`  
		Last Modified: Wed, 22 Oct 2025 17:40:00 GMT  
		Size: 113.7 MB (113708004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813c19840b842310e255df4687191117139efc3015779520ce48c236c03827e2`  
		Last Modified: Wed, 22 Oct 2025 17:39:52 GMT  
		Size: 19.1 KB (19083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c767c4650658ed1ddf1b2480a2adeccf533c6d2d0f6e6e7e36fcbba9caaa5a`  
		Last Modified: Wed, 22 Oct 2025 17:39:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eaef10e78de98ae11393c7856338f9f1b952e78d973f2dccde2f6e414c79004`  
		Last Modified: Wed, 22 Oct 2025 17:39:51 GMT  
		Size: 6.1 KB (6078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbe879751ce497cf9c747a948ffc95b1fb7d7c58399f40d0734829e2747977e`  
		Last Modified: Wed, 22 Oct 2025 17:39:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6ce75ac2b7d9d97e31b96c1843fc0a1545446720ce8730b17b787affc704adee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9bb5bf4e1d6333cebd9bcf492584d11361e8306707d0b22989e7b05bd05d3d4`

```dockerfile
```

-	Layers:
	-	`sha256:2a4fd37a896abf3efa1f56a38be57c566f11437a9bab146303ec725f664556d8`  
		Last Modified: Wed, 22 Oct 2025 20:20:11 GMT  
		Size: 6.2 MB (6156487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:745d0f0fa0bb7c9178bb8e352cedb13a599909e15ddd3bc00bcd2ff401517c51`  
		Last Modified: Wed, 22 Oct 2025 20:20:12 GMT  
		Size: 51.6 KB (51633 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:24e182c39f827582b3fec7f67982ecb9aa6b0f16d0f04863f2cd40f1aa5deea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87145699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f04b8fa17903c5d79d7a83448e772ec5de92bfaa9a37ead4fa27661945f72c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 02:04:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 02:04:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:04:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 02:04:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 02:04:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 02:04:36 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 02:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 02:04:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 02:04:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 02:04:43 GMT
ENV PG_MAJOR=18
# Tue, 04 Nov 2025 02:04:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 04 Nov 2025 02:04:43 GMT
ENV PG_VERSION=18.0-1.pgdg12+3
# Tue, 04 Nov 2025 02:17:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Nov 2025 02:17:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Nov 2025 02:17:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Nov 2025 02:17:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 04 Nov 2025 02:17:06 GMT
VOLUME [/var/lib/postgresql]
# Tue, 04 Nov 2025 02:17:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:17:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Nov 2025 02:17:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:17:06 GMT
STOPSIGNAL SIGINT
# Tue, 04 Nov 2025 02:17:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Nov 2025 02:17:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:def4b77141116a067c72a4f39eb9fa70634fe918be6e3df3cf0bc46323be22c7`  
		Last Modified: Tue, 04 Nov 2025 00:12:34 GMT  
		Size: 25.8 MB (25757661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adb3b96121d4ad5852ed7c245b7914087f7dbb449087b8aaaef28c33b3112ec`  
		Last Modified: Tue, 04 Nov 2025 02:17:28 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032cb885d7973944ec3afed56181b73edf2a875cda258cae26fa36d9edb95e8b`  
		Last Modified: Tue, 04 Nov 2025 02:17:29 GMT  
		Size: 4.2 MB (4151220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d618c098aa769184b793664dbeb9aa4f581f9796b9b98edc6b4ad5a6a07971b1`  
		Last Modified: Tue, 04 Nov 2025 02:17:28 GMT  
		Size: 1.2 MB (1220046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5422f3371032a96b752f656ad0b8eccd42a24c03b0bf3a11b12a8a855da38a60`  
		Last Modified: Tue, 04 Nov 2025 02:17:29 GMT  
		Size: 8.1 MB (8066547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d186947f9ffaec863520e6bb8d151a3b09471d01bddb4790fa8f6e24672f4e`  
		Last Modified: Tue, 04 Nov 2025 02:17:28 GMT  
		Size: 1.2 MB (1195042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad6dc2184ae1b8a7ec52bba6eeee659056105ebd15c54b7ffac726572d4b75b`  
		Last Modified: Tue, 04 Nov 2025 02:17:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f5c686f2a1c255e267b74242955517f3d34b51f2f6cac5d70cd81803a68ad9`  
		Last Modified: Tue, 04 Nov 2025 02:17:28 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b59de377737e3e31575638b6f548d1d578b281702146198ac2660024ea2829`  
		Last Modified: Tue, 04 Nov 2025 02:17:35 GMT  
		Size: 46.7 MB (46725284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57f6963e43353d9917fb3121b0f151affbe5f7922a4e14bb18bfcb4e47a6235`  
		Last Modified: Tue, 04 Nov 2025 02:17:28 GMT  
		Size: 19.1 KB (19087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd35056399a98aea5f10e51239ac2a9536d052b97c5a8e6693c7fde5e36323ba`  
		Last Modified: Tue, 04 Nov 2025 02:17:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f7a3c37e3956fae4b454631e7cc311f239f64573a2433ee1a5de677cdb0cac`  
		Last Modified: Tue, 04 Nov 2025 02:17:27 GMT  
		Size: 6.1 KB (6076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8e644a90c5e8faf29b0da43b108b7b425514c29b3a795ceaf6efb7e5abbfa3`  
		Last Modified: Tue, 04 Nov 2025 02:17:27 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:cb4c38732c6dc32e1a4c87a2d457147f1989a454b522d85363859345e61fe9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e27a1bdcbcecb011b1f0fd27e86bab38c46a16aa63090c64cc95f50106b821`

```dockerfile
```

-	Layers:
	-	`sha256:4dad1b9fc68d381e77720b07d93582be8c445ace465849c17544b48769018291`  
		Last Modified: Tue, 04 Nov 2025 09:12:13 GMT  
		Size: 5.3 MB (5317006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:963b81724a4dfa3c3ed1ff50241ac9e49374a7a7908f41365bcccffbd87d506b`  
		Last Modified: Tue, 04 Nov 2025 09:12:14 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:da1e423944bb1a1ad32674bf400e79db2b37591333a9f0164a371d392c35f9c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83273341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef0195ad16d9ed462a19be938c5cf17fc5ff403f7f729590e85f43380ffd107`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV LANG=en_US.utf8
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_MAJOR=18
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=18.0-1.pgdg12+3
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 15 Oct 2025 18:23:03 GMT
VOLUME [/var/lib/postgresql]
# Wed, 15 Oct 2025 18:23:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Oct 2025 18:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Oct 2025 18:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d787bcdb7d36a82dcda1acf3e2eaf80700eb2e7e19aa01f1d569a953603d7caa`  
		Last Modified: Wed, 22 Oct 2025 17:50:34 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860344b00e8c537af2312fd40c862e9402f6bd2204bfa0a10d5e50815adeeb92`  
		Last Modified: Wed, 22 Oct 2025 17:50:34 GMT  
		Size: 3.7 MB (3742681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cf88f8b33c174bcf14c79c0e68e04d146f6bb064fecc7c091c6f461e0430a6`  
		Last Modified: Wed, 22 Oct 2025 17:50:34 GMT  
		Size: 1.2 MB (1215986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368ba5273df42ed0c80330f3beedb99f8b3a4c883bc10383769851975322f3cd`  
		Last Modified: Wed, 22 Oct 2025 17:50:35 GMT  
		Size: 8.1 MB (8066477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6950a3c4a98bded5a9f4627dddef8acfb559883cf3ec0a31936cc25bae699f4`  
		Last Modified: Wed, 22 Oct 2025 17:50:34 GMT  
		Size: 1.1 MB (1067243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f2fe2b1ddbd0afbec65a993cd76f433ef3eb69b00eb7cdb47bd6b0f1250369`  
		Last Modified: Wed, 22 Oct 2025 17:50:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fddc993da473cedf0b1ac48ca8b848e1611019cdbe2d2f672850670730db26`  
		Last Modified: Wed, 22 Oct 2025 17:50:36 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c63b3f437ba685f0609bddcf6f70c9ae3444b1117a638274166f87aca6aa200`  
		Last Modified: Wed, 22 Oct 2025 17:50:39 GMT  
		Size: 45.2 MB (45217021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75dd3aff7e57755e7e3f02d78929c00cc78dabd3e8ead4cafe1b920b6744971c`  
		Last Modified: Wed, 22 Oct 2025 17:50:36 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b873003ed72d06e416744e250eb5adb3911a5b11352dff8cb169bab71a43da6c`  
		Last Modified: Wed, 22 Oct 2025 17:50:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21df5a7b7fdfc59574a5fd7a1461437b66c1845917b44b1fe70bbec9bd900012`  
		Last Modified: Wed, 22 Oct 2025 17:50:31 GMT  
		Size: 6.1 KB (6077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edde0defdd975f1f72cc0d77205aa0c13a8c2f347af92eb236474699fdeb0d2`  
		Last Modified: Wed, 22 Oct 2025 17:50:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6986de8b5f927934b8bba7baac22c78bbc17ca545615920498384056abd6e522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6d0590a1ba845458f79d60b831f7f24e5141bba74d30a0eba083237236fc59`

```dockerfile
```

-	Layers:
	-	`sha256:23c183f63222ec61febd1a16c9c6bd1aa4d82de11823e799d1ad5ff8c1450552`  
		Last Modified: Wed, 22 Oct 2025 20:20:24 GMT  
		Size: 5.3 MB (5316257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6538d0508280dd4ecb6358888494549903d09b09742ed0e15d9fd37e2b84acba`  
		Last Modified: Wed, 22 Oct 2025 20:20:24 GMT  
		Size: 51.8 KB (51830 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6c8a97e850370105ab96a778135b054f4b5814e32e74464c86d8b525ed86c6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155012425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e163c2549a00f7cbe06bbf1d3a6d8e7925542ffe46e29cecfae52cf30b06e2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV LANG=en_US.utf8
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_MAJOR=18
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=18.0-1.pgdg12+3
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 15 Oct 2025 18:23:03 GMT
VOLUME [/var/lib/postgresql]
# Wed, 15 Oct 2025 18:23:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Oct 2025 18:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Oct 2025 18:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674140c23ad8ec937c8e6459c397f754fe6134519faeecdedb101af453ccdd07`  
		Last Modified: Wed, 22 Oct 2025 17:39:56 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9219eded49009df38d7f69d7a246e935adca0295789e2fd56551c61ad06ee49d`  
		Last Modified: Wed, 22 Oct 2025 17:39:58 GMT  
		Size: 4.5 MB (4519811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abc851f9592c1413c96445dd4040a713423bf04e50b6ca46f6428a770f1e52e`  
		Last Modified: Wed, 22 Oct 2025 17:39:56 GMT  
		Size: 1.2 MB (1203247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9043aa9beef170c23e03387c210bac60fc609635affd8c1f6283aff39a678ef5`  
		Last Modified: Wed, 22 Oct 2025 17:39:57 GMT  
		Size: 8.1 MB (8066535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000bb6033639fc400e7784a6b3b984afa289e8c6cce1669e203300e9d4d9ceed`  
		Last Modified: Wed, 22 Oct 2025 17:39:56 GMT  
		Size: 1.1 MB (1108976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6742cfcc36fbd348d0d296f620a1c5dc1bae0d686b0712ca4dcd61d739630cd`  
		Last Modified: Wed, 22 Oct 2025 17:39:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c26dfc1013e833e954a13e5328aef3aef25b18cccd9cbae9522d7a4dea7ebe2`  
		Last Modified: Wed, 22 Oct 2025 17:39:56 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5fec9ae9aa96b2cad48d1686887067356e052c4fb2fd3d49827a2eed92f011`  
		Last Modified: Wed, 22 Oct 2025 17:40:05 GMT  
		Size: 112.0 MB (111981763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8d4a9398c1214f4d18c4a76df201a09f1d81b89fd6a6a58fbc9b6cf65a308`  
		Last Modified: Wed, 22 Oct 2025 17:39:56 GMT  
		Size: 19.1 KB (19087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52d0d6c7266b972cf51ba37d1db1550e2fee2f2d4715bf7dc7cdc5879baa47b`  
		Last Modified: Wed, 22 Oct 2025 17:39:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a731ecc66de7b7a0c07ffe6275598f088987139e42f2977dc63e789190bc6ce9`  
		Last Modified: Wed, 22 Oct 2025 17:39:56 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6378292fd274197f6a8b34726cbe00cafccc0cd6613fa14555e52b52898ace5`  
		Last Modified: Wed, 22 Oct 2025 17:39:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:90bddad526abb42a9c6c37856fb7003eadc5d759a24b4d65f736e8f2c4a1cad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfc6bfc90e812fcd7790434f301339488882cf44b66991da8995b43021c4115`

```dockerfile
```

-	Layers:
	-	`sha256:41e758029bcecd9b54d079885dc1205fba9a495abfe3f07b7f26c3200b966242`  
		Last Modified: Wed, 22 Oct 2025 20:20:30 GMT  
		Size: 6.2 MB (6162812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874a14399a104f61ddce104681ee91bd5e5c29769ede7a7ea57f419d282e2aaf`  
		Last Modified: Wed, 22 Oct 2025 20:20:30 GMT  
		Size: 51.9 KB (51875 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:2e4bd6bbd77ec662f160f896c351b970fa58d7358abb7d2941c0027614fe069e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93928467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771efc00cc9ae4f790775583e7bdf03a9742b9bdb5ca2dec7188456deecd12d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 15 Oct 2025 18:23:03 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV LANG=en_US.utf8
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_MAJOR=18
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PG_VERSION=18.0-1.pgdg12+3
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 15 Oct 2025 18:23:03 GMT
VOLUME [/var/lib/postgresql]
# Wed, 15 Oct 2025 18:23:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 15 Oct 2025 18:23:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Oct 2025 18:23:03 GMT
STOPSIGNAL SIGINT
# Wed, 15 Oct 2025 18:23:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 15 Oct 2025 18:23:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2675127b228fe24730a8ccdff4c483ee78be7fe4aaf8cf20c5744b2afddbc7`  
		Last Modified: Wed, 22 Oct 2025 17:48:15 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ea9f6c0ee8ba2c8b1d906b38f900fbb4cd11b009aa7956992b65156eaaf4bf`  
		Last Modified: Wed, 22 Oct 2025 17:48:16 GMT  
		Size: 5.0 MB (4965312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0508f49fd661ae21d9eb1551ac7fdf29ebda22c441e50aef3bb69c0a264b78`  
		Last Modified: Wed, 22 Oct 2025 17:48:15 GMT  
		Size: 1.2 MB (1218622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32af634f8b0065639493d9469b5068769584a56bec5dc62d4fa52b905ad2b8a4`  
		Last Modified: Wed, 22 Oct 2025 17:48:17 GMT  
		Size: 8.1 MB (8066477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1198759727bafa1b98b886cb4f69b1bb23842fd272a12be1cff80bbf107e8756`  
		Last Modified: Wed, 22 Oct 2025 17:48:15 GMT  
		Size: 1.1 MB (1137422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492cb3837a90fd40253a06376231abeabdc304c68b87770bf2429be58aca2729`  
		Last Modified: Wed, 22 Oct 2025 17:48:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59701cd2c707c32967ad1c6d0e0de229b83a668edc5d9743481052ed47cadf3`  
		Last Modified: Wed, 22 Oct 2025 17:48:16 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71d85ee18b1e19385c5656984081dd158143c4cbb1b88516f99c9b5980cf67c`  
		Last Modified: Wed, 22 Oct 2025 17:48:22 GMT  
		Size: 49.3 MB (49301044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b9502cd4ec4e0f5d2216e8c1f39206e05987ff14c0e6c10a43bec662c8bf02`  
		Last Modified: Wed, 22 Oct 2025 17:48:15 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab15b7a960ebda9c07eecbd4bb68fb26e6ab2d6fc941cdeb5230a0b85b87756`  
		Last Modified: Wed, 22 Oct 2025 17:48:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4764cac71e5143c216942b53c0ebd3e54b6c879bfbe5f7898275b16fa2ea9df`  
		Last Modified: Wed, 22 Oct 2025 17:48:15 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122c68c97c023d6dce4df95bfb0acb51b1996ae58d4d9d51d3a9110d1586fcff`  
		Last Modified: Wed, 22 Oct 2025 17:48:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c0110915b49bab0f0f3ad3fedfa641be06ff95b98b7e5e49c917801f80976264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc0de3eccd45b8c50ee917fedddf7d24c7f945687ee4afc5edfcb9c19f9ee93`

```dockerfile
```

-	Layers:
	-	`sha256:615080cb34a91f9daa3003f0fc8844d2050af46d83ea44287f0e3c0e082d214b`  
		Last Modified: Wed, 22 Oct 2025 20:20:36 GMT  
		Size: 5.3 MB (5311572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f04a740b74c0728497934792a52507efb0564d013c547dc3a34e4ff2896682a`  
		Last Modified: Wed, 22 Oct 2025 20:20:36 GMT  
		Size: 51.6 KB (51581 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:5f2364735336201a61bbbb926eb3c8b5f05898ab7fcbe54589fcae0bda0ad075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155897716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4ba36ae594c010aae9b08a38b696230fa76bb67e6bf3bf3009b34dae4b4662`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:38:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 06:38:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:39:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 06:39:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 06:39:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 06:39:43 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 06:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 06:40:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 06:40:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 06:40:03 GMT
ENV PG_MAJOR=18
# Tue, 04 Nov 2025 06:40:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 04 Nov 2025 06:40:03 GMT
ENV PG_VERSION=18.0-1.pgdg12+3
# Tue, 04 Nov 2025 07:50:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Nov 2025 07:50:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Nov 2025 07:50:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Nov 2025 07:50:49 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 04 Nov 2025 07:50:49 GMT
VOLUME [/var/lib/postgresql]
# Tue, 04 Nov 2025 07:50:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:50:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Nov 2025 07:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:50:52 GMT
STOPSIGNAL SIGINT
# Tue, 04 Nov 2025 07:50:52 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Nov 2025 07:50:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:86a398000765b1c4b7c071dc9cc165bf6a4cd12fe05016be099c4927b331abf2`  
		Last Modified: Tue, 04 Nov 2025 00:11:46 GMT  
		Size: 28.5 MB (28513928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c59277c56f373b2490221991067b5f8b28540eebec34850b2dc7bb36c43a972`  
		Last Modified: Tue, 04 Nov 2025 07:53:14 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d2200f65ed238eeb58b7835a4b23a11a90411de928803160205556ba1cc6f1`  
		Last Modified: Tue, 04 Nov 2025 07:53:15 GMT  
		Size: 4.5 MB (4475450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e1ddbe88942af174735c1845b8315e78eedf7d54d0d1442510a47d6e5bb428`  
		Last Modified: Tue, 04 Nov 2025 07:53:20 GMT  
		Size: 1.2 MB (1159178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65374a123fac46a8fad45e6a31ee16ac4ba79b49c50b4ee3e3b4898f86ad6aff`  
		Last Modified: Tue, 04 Nov 2025 07:53:15 GMT  
		Size: 8.1 MB (8066506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e11f2542a868baeb70ec0b078ba780b29888faa148328ee465d722b4f30aa64`  
		Last Modified: Tue, 04 Nov 2025 07:53:14 GMT  
		Size: 1.2 MB (1182883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52865a864447f0a892467e48e5830e078706835e5fb9bdd28a416c9f7f620249`  
		Last Modified: Tue, 04 Nov 2025 07:53:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1382e5350be307b5b3b5a61477c5f2e6ddec9e012d8fbe4c7d6067e8368d874e`  
		Last Modified: Tue, 04 Nov 2025 07:53:14 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759af2a4cfb76b3a4b91207db969771b20d146f7a05035f1c91479de82f0ee8d`  
		Last Modified: Tue, 04 Nov 2025 07:53:19 GMT  
		Size: 112.5 MB (112469863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f273ede0a8e3e6ec461b687c9979e1941b59c6322f9a81a56cc858ae28ac7e41`  
		Last Modified: Tue, 04 Nov 2025 07:53:14 GMT  
		Size: 19.1 KB (19095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c345bc8504f536025901d17803aae7f27d747613cd1adb4cb03dba0c05cef6c8`  
		Last Modified: Tue, 04 Nov 2025 07:53:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b7b0efc56fd6450b4b025e866c3f302d4e0c825ec3d5fe735832b34ab3ff7`  
		Last Modified: Tue, 04 Nov 2025 07:53:17 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53d2cf5e10f3f68eedffdbddeaf36a7160ea25131f2a9403e9e76315f43784d`  
		Last Modified: Tue, 04 Nov 2025 07:53:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ab4c281e00b19e9a5c3298f3e68e80eddea33e1167a5557416b1914e92d515bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 KB (51462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bd00f6b02a07db56f7044c014285d851296550783096ad8344b39af948aac8`

```dockerfile
```

-	Layers:
	-	`sha256:4a521107f0bb4de8a701361b31741e5f2641dc35da5790bb3c37ba7b8b46597b`  
		Last Modified: Tue, 04 Nov 2025 09:12:30 GMT  
		Size: 51.5 KB (51462 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:5af4d543e3d4b485f328ad6d36d322a9c03cb6614bb4724614ec8f665be13c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169915563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c2a79c3168c143f830ae4b06fca5c9cf6d0f590aadca72305575869f80a0d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 05:31:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 05:31:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 05:31:55 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 05:31:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 05:32:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 05:32:04 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 05:32:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 05:32:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 05:32:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 05:32:12 GMT
ENV PG_MAJOR=18
# Tue, 04 Nov 2025 05:32:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 04 Nov 2025 05:32:12 GMT
ENV PG_VERSION=18.0-1.pgdg12+3
# Tue, 04 Nov 2025 05:32:53 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Nov 2025 05:32:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Nov 2025 05:32:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Nov 2025 05:32:54 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 04 Nov 2025 05:32:54 GMT
VOLUME [/var/lib/postgresql]
# Tue, 04 Nov 2025 05:32:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 05:32:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Nov 2025 05:32:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 05:32:55 GMT
STOPSIGNAL SIGINT
# Tue, 04 Nov 2025 05:32:55 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Nov 2025 05:32:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9103551c5ae3de0bf7412fc3c3b589558b7a201cbb70143c80bd2b0f61436dea`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d8d801e7df0e946c6ef493f47fde8298f346b4857822e8cc845ec2dace394c`  
		Last Modified: Tue, 04 Nov 2025 05:33:52 GMT  
		Size: 5.4 MB (5368449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804b885fd04fae73183839df1808db9272d0431ae0f0928bd6b382d946151cde`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 1.2 MB (1208164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b3fc93c49f7cc3807da4615adc099c2bb10e0cb4118ef25ee5f6b9a5e558ce`  
		Last Modified: Tue, 04 Nov 2025 05:33:52 GMT  
		Size: 8.1 MB (8066533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a273919551517ff19ec39b648f56896c0ad54a2bd41122a406872dd4765d5d2e`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 1.3 MB (1283653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ecc47ad06fcbf1282127b790eac31a18c8f9f33a45e576e3a31d852677b9a7`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0009da3bc6b84521bd539e23e6eb6607d2c54baf338648051dba9320134fc83d`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03383d208009a05e72821d2a0a8ba91e04f1053ad140d660da621472f1f0b20f`  
		Last Modified: Tue, 04 Nov 2025 05:34:03 GMT  
		Size: 121.9 MB (121889951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9a026645fd5f045b23239b2b483a21608e42662db5c1e38581596033251641`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 19.1 KB (19092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16cfb201e1b375472bf8c96c9789202884362b2f2d4e431899da380e55c0b3f`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f08fffc721d48d5685c7e4f28b402e55698e5ac88f04502251da3fb0abb029`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56eb6b46ad8798f4e8a874563966a8e55ecf380be593d6d03879fb8cd1ae2d2`  
		Last Modified: Tue, 04 Nov 2025 05:33:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d8ff852111c1dc082a1857e35596b95c77daabd100478b1c617bc9903f0db3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1c8ba2ecb62dd3ec53c45b9786cffe2eeb8f8efa3b6d9f13b0e259cfec6412`

```dockerfile
```

-	Layers:
	-	`sha256:756addb39491811318b50a180f8d4bdeb0ca3c7864d5b64000349cb2d4acf4a3`  
		Last Modified: Tue, 04 Nov 2025 09:12:35 GMT  
		Size: 6.2 MB (6163872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e14849197d32510c6ba51851cb3a4b1d5392657bc581dec1749c64a43fa57f8f`  
		Last Modified: Tue, 04 Nov 2025 09:12:36 GMT  
		Size: 51.6 KB (51648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:6816322a6ccafd2b2ad32f1edce21f21d99723280e476e082573c368052f6f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166357365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8a0a83cd874fec8dbf1c433fe00a22e91566a84df41b1d6b591c7b4530404`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:51:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Nov 2025 01:51:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:51:31 GMT
ENV GOSU_VERSION=1.19
# Tue, 04 Nov 2025 01:51:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Nov 2025 01:51:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Nov 2025 01:51:36 GMT
ENV LANG=en_US.utf8
# Tue, 04 Nov 2025 01:51:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:51:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Nov 2025 01:51:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:51:40 GMT
ENV PG_MAJOR=18
# Tue, 04 Nov 2025 01:51:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 04 Nov 2025 01:51:40 GMT
ENV PG_VERSION=18.0-1.pgdg12+3
# Tue, 04 Nov 2025 02:03:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Nov 2025 02:03:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Nov 2025 02:03:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Nov 2025 02:03:26 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 04 Nov 2025 02:03:26 GMT
VOLUME [/var/lib/postgresql]
# Tue, 04 Nov 2025 02:03:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:03:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Nov 2025 02:03:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 02:03:27 GMT
STOPSIGNAL SIGINT
# Tue, 04 Nov 2025 02:03:27 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Nov 2025 02:03:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be232883d651408831817911bfa9e7aa97a9c1c16f0d9f51c1e4ba7b41472bac`  
		Last Modified: Tue, 04 Nov 2025 02:04:32 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23b66b64a9cdc4ee49f93ae5b45cc117b88ef644c87e9f7b7233ad03f1df1e6`  
		Last Modified: Tue, 04 Nov 2025 02:04:32 GMT  
		Size: 4.4 MB (4391266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7150046113cc44e28b1ef06ab4fbcccba24aaa77b823e94e7ddc78b90768e77`  
		Last Modified: Tue, 04 Nov 2025 02:04:32 GMT  
		Size: 1.2 MB (1222763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803591ef6beb1305b4de9cb08ea0a5a7155ba4c21ab320b03dd2534e3cc8350c`  
		Last Modified: Tue, 04 Nov 2025 02:04:33 GMT  
		Size: 8.1 MB (8120685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaa31f35ea72d07928eb7499fc5efc4246391480d5cb584d9d0697eed9f4177`  
		Last Modified: Tue, 04 Nov 2025 02:04:32 GMT  
		Size: 1.1 MB (1097009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d55137c99bd935b934b11785cb06835fd3dab3bbeab391582d16418c871865a`  
		Last Modified: Tue, 04 Nov 2025 02:04:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a18c5bf9206e23832e577d19e87876f15f4e9d70196bbc3e360ccc62fdb32e`  
		Last Modified: Tue, 04 Nov 2025 02:04:33 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86535f53de481fe16ac5984e761f3a5788c24791ef529811d506e268003f1407`  
		Last Modified: Tue, 04 Nov 2025 02:04:48 GMT  
		Size: 124.6 MB (124611184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a721179bb4c5640bd69639a27bd804621f2dcf68483a37e77da8268ac2a3cdd0`  
		Last Modified: Tue, 04 Nov 2025 02:04:33 GMT  
		Size: 19.1 KB (19092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d53dd3793544207f9d9577eede03511cfbc93273bf3135e8734dc44146703a`  
		Last Modified: Tue, 04 Nov 2025 02:04:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2072ef55ef62c575c76a71fec886217fb4ad8eb73b576894b7098a8d30d238`  
		Last Modified: Tue, 04 Nov 2025 02:04:33 GMT  
		Size: 6.1 KB (6080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc87be269c1fca161b909ff047d708929a4eda38aa6a4ceff102da561cf94a0a`  
		Last Modified: Tue, 04 Nov 2025 02:04:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c49d14fb5e3a15ee748b384b23be295149103cc8682d579bf41f7e6b1eb5ee23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd81aba3aafbc0be1d1fed20a372b099f8a8238439351c06da80d91ff3c73f76`

```dockerfile
```

-	Layers:
	-	`sha256:5c5227f5580106f963b3304de9fe569146b504185f9e24abaccd3bad0d21061c`  
		Last Modified: Tue, 04 Nov 2025 09:12:41 GMT  
		Size: 6.2 MB (6171145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f92a61aa3d807a6efba9df68969f1032548aa2ccba995bf97a596130b9642547`  
		Last Modified: Tue, 04 Nov 2025 09:12:42 GMT  
		Size: 51.6 KB (51589 bytes)  
		MIME: application/vnd.in-toto+json
