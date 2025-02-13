## `postgres:13-bullseye`

```console
$ docker pull postgres@sha256:bf0ea1c00fc4ceb40258001e5b285fe7bc6b7c4cdbee94a0dc3bf59b460d3eea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `postgres:13-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:e60677337477d4a2d272d074f391d1907b6c2a4fbbccc14aa82224375f8767b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144703707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e1b909d0fad5cdfbf531dd48221da4ba1bfd7d5a55f242d1f7779a19a217e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18-1.pgdg110+1
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656a17f4d97dd4ed45fe66b8f856c33c0fbd60a582fbf5ee47c9115f16525921`  
		Last Modified: Wed, 05 Feb 2025 00:20:48 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f19ed2584bd9ac6867e68616bc130a33bea8353bf20d3b554a3373ac43e3ea`  
		Last Modified: Wed, 05 Feb 2025 00:30:49 GMT  
		Size: 4.3 MB (4308149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf274d81a07b696c36e1d3496f9c8ecc91d6c9094dcd8afc5b1f3e1a4b85fb0`  
		Last Modified: Wed, 05 Feb 2025 00:30:49 GMT  
		Size: 1.5 MB (1472214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58f497746988b7b184c13e9497e7dfff9167744378a35493130918691124a51`  
		Last Modified: Wed, 05 Feb 2025 00:20:49 GMT  
		Size: 8.0 MB (8044561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b33a96e8b1824733831da52ad2a6f4f033d0385e603811f75a0b87a2c7d32`  
		Last Modified: Wed, 05 Feb 2025 00:23:21 GMT  
		Size: 1.0 MB (1038348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dd2bef53aac65da3150af92ec2e8eea41671ec400c748b3644be4f1516509c`  
		Last Modified: Wed, 05 Feb 2025 00:30:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc92cb12baf91437062f766889d95ee115f5b228014044979ad48d3cf2aea13`  
		Last Modified: Wed, 05 Feb 2025 01:49:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675080d6407621ce78d23a1dcda58dcc44ebc0ed2c2de7941c680f3ed048820b`  
		Last Modified: Wed, 05 Feb 2025 00:23:26 GMT  
		Size: 99.6 MB (99567662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d739f0f3016095a990fb1727853f2d2351c9a50fbee37b12b39d6b870c814c8d`  
		Last Modified: Wed, 05 Feb 2025 00:20:49 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3668fda8af24b1d903c34f5e83aa73300b1ae347e6391f290dd1bdf738efaf`  
		Last Modified: Wed, 05 Feb 2025 00:07:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da2756d1f4ff00c7f74ad6b59fd1b9757896dadcb4a5a3b118d6ea0f8a141c1`  
		Last Modified: Wed, 05 Feb 2025 00:23:23 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aad3a32fce0cf3007464e6a0c34df4d5e70bc3a17e8e10a6a8bfe5e91b4f72e`  
		Last Modified: Wed, 05 Feb 2025 00:20:51 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093d4f5c7d0a1dcd3057d622ecf86a3fd81fc7fa031a479e5a031785019ded3`  
		Last Modified: Wed, 05 Feb 2025 00:20:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:6de7140da77e2185e48092eeabfa6fa151344fe42e31d506df539bb97711a6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5916353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a32cab6e11e7db4c0f07ac1ca864d0a099b7701994738154eefe5e4b27b494`

```dockerfile
```

-	Layers:
	-	`sha256:d9824890ce2dfb7765da1a569a39e8fbd66689db61c70317e5b9beb8b15b6317`  
		Last Modified: Wed, 05 Feb 2025 22:00:25 GMT  
		Size: 5.9 MB (5862481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45d89c89c0c8bf2948e19fa6fd9b05c08cebd7b0a429f4b3d49c5ed50b234f3`  
		Last Modified: Wed, 05 Feb 2025 22:00:27 GMT  
		Size: 53.9 KB (53872 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:cef1b2693b7caf81b3450515c6dd5cdd72493c243322be39cbff7ef5c49869e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132913018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0370c9cb8f12fc8bc7dd147a81daf4b72447ec5c4855b37dd5182c0d18e20569`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18-1.pgdg110+1
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 08:24:31 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58757938f9c4aa50dbc78e022bbdaa24d21099a039910f446209a779868b80e`  
		Last Modified: Tue, 04 Feb 2025 22:00:22 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62775880bddc861108aa9f905791f6a3771e3653ba8b7d4d10bcd4ba90c29a2`  
		Last Modified: Wed, 05 Feb 2025 22:00:31 GMT  
		Size: 3.6 MB (3601780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0f4c44e421a4e93937a077a296f3ebc4f1ef3d241a191f9f0d0aa60140db88`  
		Last Modified: Wed, 05 Feb 2025 08:51:36 GMT  
		Size: 1.4 MB (1439324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165c94191e8ff6def5554f08ab11e45e520d6c978676371a7a3f49e3588e0adc`  
		Last Modified: Wed, 05 Feb 2025 22:00:34 GMT  
		Size: 8.0 MB (8044548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca6fd9675bb8eb2bb071085178e577d32b1efa16ad993abeaeacfeec533a93`  
		Last Modified: Tue, 04 Feb 2025 22:00:25 GMT  
		Size: 908.7 KB (908666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d52c9086f5bf4998da3823aa55355ab2ef7a22afbafda64d9ec7b91c05273`  
		Last Modified: Tue, 04 Feb 2025 22:07:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5e6cfc1e56108a8465fafbd38c207a134683e6e9310e0edfe9f34bf75df401`  
		Last Modified: Tue, 04 Feb 2025 22:07:05 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a58bdf81cdd297d195095d2667bf12c7c1c391ba69552bb9200ee07f2cf3891`  
		Last Modified: Wed, 05 Feb 2025 22:00:45 GMT  
		Size: 93.4 MB (93364641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d572d7eaba4973fbf209c2281faac436eba67ca58b5484d261ce563d7fec06`  
		Last Modified: Tue, 04 Feb 2025 22:00:29 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5201c77619cf2c078a44871bfab51f15d0ab7824ad767d359bf73402a7f6eb`  
		Last Modified: Wed, 05 Feb 2025 22:00:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d4a91afcd881f09ac4c906c51c5cf93410cb65bda2ce41cf0b702ebf1e18a6`  
		Last Modified: Wed, 05 Feb 2025 08:29:57 GMT  
		Size: 165.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c602879bd8c9d8272d1b96bf615f9951e41594322da410ae01f3d07af37103bf`  
		Last Modified: Wed, 05 Feb 2025 10:48:19 GMT  
		Size: 5.4 KB (5412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c87ebf2cb57c4c59d65c866fe374c9b0e9db9b12115c07bb9ee9239e2dcbb35`  
		Last Modified: Wed, 05 Feb 2025 10:48:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:07361612c8a910da37a1cf020a23c8d540b792beb5882a7da65ff01f5d310000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5927212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b13207771847cd95a115c53cdae972b0c9350061e7e0763f842e5ecc16d6f4d`

```dockerfile
```

-	Layers:
	-	`sha256:297f73c35fb0d819605b5c3e98aa091115c2dab7ba49d5a6bb87a5d1e7636071`  
		Last Modified: Wed, 05 Feb 2025 08:29:48 GMT  
		Size: 5.9 MB (5873146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63e1d886383f1ad310501f6bc9c682ed4e8494d63addea7d890e97d8e7d04c7e`  
		Last Modified: Wed, 05 Feb 2025 22:00:32 GMT  
		Size: 54.1 KB (54066 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9f59facbb76b2a02c79f5d4a0292c0d19178311ba41edfca6bfa153307946339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141722870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069006ccfecdbb8e62c02d45b51f74cf7754a85e75ab5d61c55ecff7d3a96bee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18-1.pgdg110+1
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851fb9604468f4d3d1f2d0f531d013bfc5d6b95d99e8a7f640ca42325df3ca7`  
		Last Modified: Wed, 05 Feb 2025 03:28:18 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb22dd44be99186db58182b681f83eae665de75553f6b64937c426586a26883`  
		Last Modified: Wed, 05 Feb 2025 03:27:33 GMT  
		Size: 4.3 MB (4312866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586dc470881d6f1e9635736743d9217602147a7fb0f59e762c76b6e021d8d233`  
		Last Modified: Wed, 05 Feb 2025 03:10:25 GMT  
		Size: 1.4 MB (1404143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c26d7f7fc835a31f3a2df64bad52775e6c8589d5877ac1a6b42c6389dcb31f`  
		Last Modified: Wed, 05 Feb 2025 03:10:32 GMT  
		Size: 8.0 MB (8044431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ac90b2904f37b8728a970638c180d074e41e20b7888dd23f5a9c93f83cf29`  
		Last Modified: Wed, 05 Feb 2025 03:16:32 GMT  
		Size: 1.0 MB (1026615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a9c2f7e28227ab51a02af4e0fbb24857d3fc9df77dd25bc975eb7dd110fbd8`  
		Last Modified: Wed, 05 Feb 2025 04:53:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b6b9c08bb7c8a6bc35d1728a35f2d4e1dfeaa1ec4183abc2d6e2c5928eb684`  
		Last Modified: Wed, 05 Feb 2025 03:27:32 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad9df75557ed1a37d6e437e057e8f7522d5cecfb16779de97385ebdf80ab4af`  
		Last Modified: Wed, 05 Feb 2025 08:30:00 GMT  
		Size: 98.2 MB (98169825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b210063adc9f94fbef58190c1fb41a58c611040cbab571a1c9968705c92b47f`  
		Last Modified: Wed, 05 Feb 2025 03:42:07 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dee7a7886792f0cbb6d736b550434941cb93396570d8ce01a765fa7935ac3b`  
		Last Modified: Wed, 05 Feb 2025 07:07:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec06c5b6b1ba6f666566415f38eba83f76b7b604fde205b282b57d35bd0aca9`  
		Last Modified: Wed, 05 Feb 2025 09:24:32 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf64c66a77597c9878374971e0b86c0be82da30c9be46f04302da19327dd364b`  
		Last Modified: Wed, 05 Feb 2025 07:27:22 GMT  
		Size: 5.4 KB (5412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86877a6e6722240064ea11e2130ab1bb87622ce479913140645a8304a93cd488`  
		Last Modified: Wed, 05 Feb 2025 09:40:40 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:777aa8122a4d8c588d54e2346bcdbdebfb6e846185850c7450e153926a981521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5922886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a3358e7e0e76f5a9e56188b29d02e64063afb8ff7d6b31e7a08ee3eeea933d8`

```dockerfile
```

-	Layers:
	-	`sha256:a263fd75543b5ddda8210861404da70cfda49ce9b2bb610e91abffb8c5224163`  
		Last Modified: Wed, 05 Feb 2025 22:00:46 GMT  
		Size: 5.9 MB (5868769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa55396cffb3ea04322edc780e89976e9ab91cdadd4ead28037212ac1b1f338`  
		Last Modified: Wed, 05 Feb 2025 22:00:47 GMT  
		Size: 54.1 KB (54117 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:6aaf2ce1b39c5ae6f059a3964a90170c7a2247a18eebc432bcc0da2e0e929d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152753497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293b1c0d82b2444399243c171158082f496cf7c78f77f0898cc9881a379bb0d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=13
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=13.18-1.pgdg110+1
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 05:05:20 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224b6eef2e90a76ce6e22f75bb15c3a920b7b2074b2e03c8682ca48a8eba2263`  
		Last Modified: Wed, 05 Feb 2025 22:00:49 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b536cc8c44e9028b6d393b79186d4f76eb05db6336333c70159f551960cbfb`  
		Last Modified: Wed, 05 Feb 2025 22:00:51 GMT  
		Size: 4.7 MB (4719686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2f4f877d436637cf946ffd33686965569b82b840b8ba36fbed975617250b0f`  
		Last Modified: Wed, 05 Feb 2025 14:39:52 GMT  
		Size: 1.4 MB (1447783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a5bbfedc0e9bf50c986d379dac8d2df6da0a758338e92b193dcf752854c27a`  
		Last Modified: Wed, 05 Feb 2025 15:45:49 GMT  
		Size: 8.0 MB (8044441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ee8c0c74dfd91227cf0bbe66639733f008821800f65490d12db9202a92b16a`  
		Last Modified: Wed, 05 Feb 2025 14:39:39 GMT  
		Size: 1.0 MB (1028948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106275d19855820430c5029565566584b4cd8c8a4cb64a3751cd1e6e5fc23c1d`  
		Last Modified: Wed, 05 Feb 2025 22:00:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a3279bb71819355aefa39ed8b7906fefd762a80d40c99079c87c96169ab74e`  
		Last Modified: Wed, 05 Feb 2025 22:00:56 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c166d2a5b9080ad1070f73293801f92bd04da17ce9613d893a2721fc84437b`  
		Last Modified: Wed, 05 Feb 2025 22:01:06 GMT  
		Size: 106.3 MB (106313584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c7322011adb49420dad60871e5e6a632911a7cae165ae2240f94eead8b9068`  
		Last Modified: Wed, 05 Feb 2025 17:34:57 GMT  
		Size: 9.4 KB (9352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4a19f26a3018fe11c4b552f80232861552881081d0a412161492660e515d1e`  
		Last Modified: Wed, 05 Feb 2025 15:45:36 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d68bf6a8d4895b6b863eba2b11d57c8e22c46174a9fbb26462c0145f6f7be9`  
		Last Modified: Wed, 05 Feb 2025 14:39:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c87de94b238e736afaf6e7d6410e9ac033fcfb359f81e275d7c372638c3eb62`  
		Last Modified: Wed, 05 Feb 2025 17:34:59 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ae5f5e857e68432a78b0e7f76c2119f40d8206b4a03b39ad6a22eabfbc1cbf`  
		Last Modified: Wed, 05 Feb 2025 15:44:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c0947a2ab02b16c3ad89ea16e5d56d17fae662acdd78b8bd81f51271b294fb3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5924754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42786fcc7c5a33f3d8656b5bc061df2c0a0faf242da2f99adfc2857ce7ceaa`

```dockerfile
```

-	Layers:
	-	`sha256:3759aa6d1572f878f40d4129aafd17f47619cdfc0e1dd779d26c22821ec3f70e`  
		Last Modified: Wed, 05 Feb 2025 22:01:12 GMT  
		Size: 5.9 MB (5870921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6b30bd0791cbafb71edf51d7af6b0d9a8d2b1c48fdf59ced6c810e0f4b6d70f`  
		Last Modified: Wed, 05 Feb 2025 22:01:13 GMT  
		Size: 53.8 KB (53833 bytes)  
		MIME: application/vnd.in-toto+json
