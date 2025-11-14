## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:e3d7040cef3d020762850712a7ecd27b8f718c18d6b0901e41cf402a814d65ce
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
$ docker pull postgres@sha256:b018788a4d41a1a9f8532aed3dedd34f92096ad7170ebe06f67cb00fd6db929d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.9 MB (152900420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc032ba59fdae01c9e523478728a2ca101972c16fd0dcb30ff9007f7302466b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:20:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:20:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:20:22 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:20:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:20:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:20:26 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:20:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:20:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:20:30 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:20:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 14 Nov 2025 19:20:30 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Fri, 14 Nov 2025 19:20:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:20:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:20:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:20:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:20:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:20:42 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:20:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:20:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:20:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:20:42 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:20:42 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:20:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a76c308d60baeb39069c40496a4b5d6416ebb5fa73e070d5e138d1c42283b2f`  
		Last Modified: Fri, 14 Nov 2025 19:21:12 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bb86df1cd5df2cf4d185bb636cb873412a12b97feb2b96856615f34e482bf3`  
		Last Modified: Fri, 14 Nov 2025 19:21:12 GMT  
		Size: 4.5 MB (4534036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467453a569e5e79e80af9c55459933ee02c50955123e43715c13732c1b208a0c`  
		Last Modified: Fri, 14 Nov 2025 19:21:12 GMT  
		Size: 1.2 MB (1249481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdda40d71617af85fa91990a978875e66c3b2884b243bd752677147a485014bc`  
		Last Modified: Fri, 14 Nov 2025 19:21:13 GMT  
		Size: 8.1 MB (8066440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0a861cfd0543853d81467e46923f4e2235462f6e16a6af32001ef438a526db`  
		Last Modified: Fri, 14 Nov 2025 19:21:12 GMT  
		Size: 1.2 MB (1196374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb80df76ce08bf8aa9fee8b6c7a51d357925aa1e709ef5c2deb6429bebb968af`  
		Last Modified: Fri, 14 Nov 2025 19:21:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5b0499b9199d966d1c0bc39c72e655938acb413155d6e35acc229fd0799b2b`  
		Last Modified: Fri, 14 Nov 2025 19:21:12 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3da88a1955ca6a73b57e04ab4cc0791cf272d59e471a938078fad0e70be5f7d`  
		Last Modified: Fri, 14 Nov 2025 19:21:29 GMT  
		Size: 109.6 MB (109605007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed6a9f2b818d8fe25ee528c5f8557faff1a445ea6f9d097b2d13f91a45fa049`  
		Last Modified: Fri, 14 Nov 2025 19:21:12 GMT  
		Size: 9.8 KB (9775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbab45465f032fd25831267a958564dec132b4965050e1bdb34c097b45c8df3`  
		Last Modified: Fri, 14 Nov 2025 19:21:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69987f5d1b652f612fef206b565b48a84d31422dd80738a8fa618b1366cb438`  
		Last Modified: Fri, 14 Nov 2025 19:21:13 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d833b28b25a9438736cd3cd2f38ac3dae829a6b72b5d172c2276fe291d0efd12`  
		Last Modified: Fri, 14 Nov 2025 19:21:13 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6add1308f1af08ab3baf09416f14b0362542312b01277e04ff10617c091129d1`  
		Last Modified: Fri, 14 Nov 2025 19:21:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e06631ae6e6902b77388cb2c2705d08483b47f3667e7b867bc9ae8b2b3e7a51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69672c3449345e17c7a46d1a3c6f0563559c268b24face52820c035288b60827`

```dockerfile
```

-	Layers:
	-	`sha256:cc77c3935a937ed3fdcb71e33f6ead398280f9a5d8d7c1fded59f2c6f1ecc192`  
		Last Modified: Fri, 14 Nov 2025 21:11:46 GMT  
		Size: 5.8 MB (5843338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb823ea7159ca3d24e2afe477e7f95905e491ae45a912e8a9968c3731d64e0d6`  
		Last Modified: Fri, 14 Nov 2025 21:11:47 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:fed3b7d29d72ae89308c9f3c762eb94f9ebed4cf7436270e7a8572427f4b5aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145846590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b15d153538e4c108ee6107e95ff3ba8d85b365664ee014dc7e5d955bab539fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:19:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:43 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:19:50 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:19:56 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:19:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 14 Nov 2025 19:19:56 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Fri, 14 Nov 2025 19:34:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:34:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:34:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:34:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:34:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:34:12 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:34:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:34:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:34:12 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:34:12 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:34:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:def4b77141116a067c72a4f39eb9fa70634fe918be6e3df3cf0bc46323be22c7`  
		Last Modified: Tue, 04 Nov 2025 00:12:34 GMT  
		Size: 25.8 MB (25757661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d707ca23984c54544f41535d5e500a24b15c7c1fa9df68030857039c2b2fef`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c18a66bcc5507d2f794ed86a509d571b002a54f0a63006c5330b9876aa2fa47`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 4.2 MB (4151200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25632ae93563130a3b8ca5c4c561fd9801756a42204cb5528109ffd9e1850002`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 1.2 MB (1220038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b06eecf6612338b3b7dfa0f8c52b14beb45dff2e1bf340c24e95fb4b6dd5628`  
		Last Modified: Fri, 14 Nov 2025 19:34:45 GMT  
		Size: 8.1 MB (8066537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c76a01daa23da4ca3bdec914ac220a128680bc70734544349e207b7f08191f`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 1.2 MB (1195037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd0b3b8f0a7d70df320cf698434adaa5700704dab8e72b79808611cc0c2d270`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a9f43351cab9b42321f71aaaa2977efa416f0f33705dcf87a3344b97111544`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12d90039b9d740c858ffc4afdbff8eec39ee35870c6ba33dde5f96f72b75d2d`  
		Last Modified: Fri, 14 Nov 2025 19:35:05 GMT  
		Size: 105.4 MB (105435588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163f047cdd871ac5dc8f0c3cc0602d49e07116fc9a486e053ae4eb98cc11810f`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277d08bada465686315708b8bbae57e3305e530f7d1da4e9ba3c1ea5f52f34fb`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd37020e7dc690877a4a732ce48d7590f5d44c7d4df121d65309039e811c2fa2`  
		Last Modified: Fri, 14 Nov 2025 19:34:45 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693607c5a549c1abd27313d923d5885b79a14f90247df344c4a7f9c75bb2792b`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8355c46be9f85aded589ba26f7c2329583a2dad9e73814384b7dcfd5c0dbbd0`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8596ed4103c06e044167cb4e7ea25ce7e643d45069ede5005c17b7a10bcbb44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab076fa87d552ed2a3518f4e1784c58bc488ec03a894ed22c20a3fe9039f81f`

```dockerfile
```

-	Layers:
	-	`sha256:eb4965cf70f3823f3c1d179e4cf0c78775750de6899336521016ff06d03be183`  
		Last Modified: Fri, 14 Nov 2025 21:11:52 GMT  
		Size: 5.9 MB (5857439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b750cb256eae9a4ee9fd0aa30ea52663f3484b2f53c269176582704586b76cc3`  
		Last Modified: Fri, 14 Nov 2025 21:11:53 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c5345a1d938a95bfbcd4a89aa2caa44d0fa7c19b5e53f1a33d50b1811541e425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140925391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4021639f20c73646782a41f49d6c0602b531e363e87412d04fd1c7949082375f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:47:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:47:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:48:05 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:48:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:48:10 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:48:10 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:48:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:48:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:48:15 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:48:15 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:48:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 14 Nov 2025 19:48:15 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Fri, 14 Nov 2025 20:02:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 20:02:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 20:02:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 20:02:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 20:02:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 20:02:13 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 20:02:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 20:02:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 20:02:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 20:02:13 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 20:02:13 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 20:02:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6d0e47732f72e3c75486da64ae10a064277c404588defcb0065fced3e29d5`  
		Last Modified: Fri, 14 Nov 2025 20:02:44 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021b1c1169918af7dfbe272e93eb4ab51deadc126b04d2ae5c332aac5afead4b`  
		Last Modified: Fri, 14 Nov 2025 20:02:44 GMT  
		Size: 3.7 MB (3742653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97118636531cdafac12ddd33a9f703559e96180c123154440c31b2ffa131deac`  
		Last Modified: Fri, 14 Nov 2025 20:02:44 GMT  
		Size: 1.2 MB (1215974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871e05ca10f38cba2c9b50435065695889b8c5ece26f7f57744ff897ef0e555a`  
		Last Modified: Fri, 14 Nov 2025 20:02:45 GMT  
		Size: 8.1 MB (8066415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a58afab628800f0d99fcb4a8b897da696cfa24378a14aa50556d5c63586cf5`  
		Last Modified: Fri, 14 Nov 2025 20:02:44 GMT  
		Size: 1.1 MB (1067235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5963ca5cffd4b9898166f03b378e721c92c0f22534d598709193226162107f4a`  
		Last Modified: Fri, 14 Nov 2025 20:02:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b999054b06b00703ba66eee509936a1fc600f3e487ba372a853840ba6d6d2`  
		Last Modified: Fri, 14 Nov 2025 20:02:45 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14df011e42b6f21e0201e713038ec15069552688842ee877c048008a77a84fdb`  
		Last Modified: Fri, 14 Nov 2025 20:02:52 GMT  
		Size: 102.9 MB (102878455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c1afc06db0b083776ff7ff0825f1f697972184fd5617c725a63b0b568400ab`  
		Last Modified: Fri, 14 Nov 2025 20:02:45 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7fc3110dc36a8d90a53aa8f8c16b066b69b95e9cd680c6d60898c1b7686b2a`  
		Last Modified: Fri, 14 Nov 2025 20:02:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188f0c20e0a577494eb907d34715cfc17b2236ed51426afdd0ad7b60e59911dd`  
		Last Modified: Fri, 14 Nov 2025 20:02:45 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2554eb5fe0fc92382b9cce3b7e221347f7153acffae15a00e6c85d315cb5d29e`  
		Last Modified: Fri, 14 Nov 2025 20:02:45 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5781c06ad7dc9141dce8a9f48fdb7bc67469316b5f633697b0b77edcef0ec3b`  
		Last Modified: Fri, 14 Nov 2025 20:02:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a1a61e48c382573cd18976b0845d02a8aa91095d858b8b71e6883ae715c375eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663f9e16f3fffa43e682a34c060ae0b01a3e233af0eb578a6ae4be0c0d6742eb`

```dockerfile
```

-	Layers:
	-	`sha256:cde408f9c4a9b981cdee695f7418bae4dc53ce278b39b22f1015b7f83b1e9c45`  
		Last Modified: Fri, 14 Nov 2025 21:11:59 GMT  
		Size: 5.9 MB (5856694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96eac6e8bc971b70676b52c9a79382c4ae6a0547c3792c415541849d5c271902`  
		Last Modified: Fri, 14 Nov 2025 21:12:00 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:5429bb2827851205f9d3efa8418b79f6af74e6e00b88d3a47fa5795b6f35d507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150895801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfcf47a5be6936eea08ca759ff885c15d41c5e18bcef3bdba7e27e7d438e42aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:18:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:18:41 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:18:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:18:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:18:46 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:18:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:18:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:18:50 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:18:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 14 Nov 2025 19:18:50 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Fri, 14 Nov 2025 19:19:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:19:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:19:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:19:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:19:03 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:19:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:19:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:19:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:19:03 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:19:03 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:19:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d322ff6ced287d634663ba34abba4b2f9fe3859172fdf84773bd7699a5b49c`  
		Last Modified: Fri, 14 Nov 2025 19:19:34 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985bee11478c4b8481bd9f78c39662443403f759aea292e54dcfab902c510f76`  
		Last Modified: Fri, 14 Nov 2025 19:19:35 GMT  
		Size: 4.5 MB (4519810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911d0f47feceb6e29340fcf1c6aeaea36e84111c06ea673957f42d67c8e194f4`  
		Last Modified: Fri, 14 Nov 2025 19:19:34 GMT  
		Size: 1.2 MB (1203255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3de15ff3a0ee1c4d1c155e842e5d66b897fe801a36e922ce8d53ac8fb6f4628`  
		Last Modified: Fri, 14 Nov 2025 19:19:35 GMT  
		Size: 8.1 MB (8066445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b87a8c9fd5e25b31844750e55bdfd7306c573653e949552c2818530c3a8029`  
		Last Modified: Fri, 14 Nov 2025 19:19:34 GMT  
		Size: 1.1 MB (1108953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41c5485b6230376832d0879d61f851ff02332153e98e1d8491b5cd0198c74e7`  
		Last Modified: Fri, 14 Nov 2025 19:19:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a2df6fcec67e61d87a54b857535a1b82cca19cff33bab903b6c008244d32b2`  
		Last Modified: Fri, 14 Nov 2025 19:19:34 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3201ae07c6694413d5c8d2f255399fc9240fc01767af056cb4b136b4e93046ad`  
		Last Modified: Fri, 14 Nov 2025 19:19:45 GMT  
		Size: 107.9 MB (107874432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bf3accf9431226388a404931ecd4ce57e3bc6bb6e0d39ac1b93dcc57a45d49`  
		Last Modified: Fri, 14 Nov 2025 19:19:34 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0b6c08cf7833a3cf92347b26450a1c436b0dbabce60a771482861400922714`  
		Last Modified: Fri, 14 Nov 2025 19:19:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cf938713bcf0972cbe70f77295b22b0170f6a8355c742f339fce02910e38c2`  
		Last Modified: Fri, 14 Nov 2025 19:19:34 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69fa96ed4928be8c708c776fcefa435bb7073bde459e68e4e67fed396fb1232`  
		Last Modified: Fri, 14 Nov 2025 19:19:35 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fe6c3f0662bfab0f0dfb7343352996ed5803d98d96f38cb1e57b2064c66baa`  
		Last Modified: Fri, 14 Nov 2025 19:19:35 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9b594563ae2cb98e47b80348105199ac40adfff31a46ed8c18f590d18779b7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5903190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123bc9272956ad44ad67925ee0ab01b55c9a572df5462f2e32bea5297645f583`

```dockerfile
```

-	Layers:
	-	`sha256:9d02feaf91d7502a21a7c0743f5c23b07e3a102a5b755fb9684fe5054f1ef5c2`  
		Last Modified: Fri, 14 Nov 2025 21:12:06 GMT  
		Size: 5.8 MB (5849649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57addbcfe20511f0d9d59d7a7f1ba33d6107b1c754005dee9dcf7ebcebb7edf`  
		Last Modified: Fri, 14 Nov 2025 21:12:07 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:834adab92d73f124316122637057689d0ab5553a5f8d3d65009c30e979f6bbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9033d0c8dd2c1bfaa881c40f40eda1cb0dabacb8234119c6a970eff4ec0d007a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:22:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:22:58 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:22:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:23:03 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:23:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:23:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:23:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:23:07 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 19:23:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 14 Nov 2025 19:23:07 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Fri, 14 Nov 2025 19:34:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:34:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:34:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:34:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 19:34:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 19:34:14 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:34:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:34:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:34:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:34:14 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:34:14 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:34:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2eff29f4419d4316de7184944102781aa38f76bcfe4118a80e91d375380b2e`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8da9e6afcea9986a9f0a4a8dea82b5257a305a8b49afec04501929bd28346a`  
		Last Modified: Fri, 14 Nov 2025 19:34:45 GMT  
		Size: 5.0 MB (4965360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27963fb9cf399b25f389581ce0605d04802de4f8db4fc81109b99ec9af32da2`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 1.2 MB (1218647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6889e68ebc01bb86293e8d8fa1743ca3c532b626c728f93c2e0bf698089a49`  
		Last Modified: Fri, 14 Nov 2025 19:34:45 GMT  
		Size: 8.1 MB (8066436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3531caae39747b0cc69532073ae1b76fba46d1819ea449eaf8e73bfe0bf87cb1`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 1.1 MB (1137431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee26d05babdf6ebe4a5add3f928a71bf383c21724cef0a4ea7a42bfe5be0606`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8908941abab24e91f2d2309b2e39d1739d03c6db17e460d054e080982f63f370`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a8b4f55e710c6f44e923b53317b1832237c1a772c6dde971c67d33644e836e`  
		Last Modified: Fri, 14 Nov 2025 19:35:00 GMT  
		Size: 117.0 MB (116985021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d132cffedbacb2c49b9fda6a44208b2f4896e691b19b40570e9f9956b69db2c2`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacb44c2f5a16c3ffb02d6f29a792a1cccac0b3ac96b27f72334a53b63a67ccc`  
		Last Modified: Fri, 14 Nov 2025 19:34:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100ae4004cfdcbefa326b0515e78be071344b845323c9d6cd4da6672a7f7e30d`  
		Last Modified: Fri, 14 Nov 2025 19:34:45 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeafa48ceccd8929dab6bf2869844f2a4f46003e77f59557032d32487f97145e`  
		Last Modified: Fri, 14 Nov 2025 19:34:45 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d7a3bfe4af36c4ad8158644868abd9957a92eaedeb30cec1f5562798dd6f83`  
		Last Modified: Fri, 14 Nov 2025 19:34:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:39f08d22d26ab97a1a906c5b651b83fd1cce06949f7d2b58302098c599463259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62b19530b7cb50b937fa44f7fbb391755432e7cf0a9b63ba80c5b633b5a1d95`

```dockerfile
```

-	Layers:
	-	`sha256:2fdc562875841aa9570b391d72eb35863d3a9940a20578fa7f6b8ed89f4a97ad`  
		Last Modified: Fri, 14 Nov 2025 21:12:12 GMT  
		Size: 5.9 MB (5855582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9071fe4114b8238f9c1e2d4aba67faad261be4065352511fc73000ec01537f9`  
		Last Modified: Fri, 14 Nov 2025 21:12:13 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:b3dac3edaf12e8376aca878710c8c6215d803a5ea6fbf65b02e27cbe83f2af96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151702423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e49a980a3f9be30b0f0ebd21bf304545c6f3a63c7f15bfc93303a2cf73962be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1762202650'
# Thu, 13 Nov 2025 21:05:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:05:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:06:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:06:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:06:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:06:42 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:06:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:07:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:07:02 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:07:02 GMT
ENV PG_MAJOR=15
# Thu, 13 Nov 2025 21:07:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 13 Nov 2025 21:07:02 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Fri, 14 Nov 2025 01:49:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 01:49:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 01:49:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 01:49:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 01:49:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 01:49:06 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 20:31:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 20:31:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 20:31:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 20:31:35 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 20:31:35 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 20:31:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:86a398000765b1c4b7c071dc9cc165bf6a4cd12fe05016be099c4927b331abf2`  
		Last Modified: Tue, 04 Nov 2025 00:11:46 GMT  
		Size: 28.5 MB (28513928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5897551a2552577c61ce4f6d3e050bbbbd0995790b8b73fd7cdc49d9b055ca0d`  
		Last Modified: Thu, 13 Nov 2025 22:20:56 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b9405847d098fc620886493e72f0e5dcfa97b75cd6a9d59224eadd9cf8bf61`  
		Last Modified: Thu, 13 Nov 2025 22:20:57 GMT  
		Size: 4.5 MB (4475523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86912819250b1edacb6275958b1d6055f3687a17efc34555ca245fa2a3f316a9`  
		Last Modified: Thu, 13 Nov 2025 22:20:56 GMT  
		Size: 1.2 MB (1159224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015e6a2dc648c577e7ac47c1e80d70878a92c9f27c134326e965177da8792833`  
		Last Modified: Thu, 13 Nov 2025 22:20:58 GMT  
		Size: 8.1 MB (8066657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa007178d718a756ccdfbeb8c247a03eda9ad3dc8be24dd059f059232f3a6add`  
		Last Modified: Thu, 13 Nov 2025 22:20:56 GMT  
		Size: 1.2 MB (1182940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690eb075c7ebd3f7bcca7651222ff06cc5008a2d145c481e10ab2a986b8028bd`  
		Last Modified: Thu, 13 Nov 2025 22:20:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975fe054767ad80c6798f32c109fc8599d39e4529f526f5ebc589b754ed5120`  
		Last Modified: Thu, 13 Nov 2025 22:20:56 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f70cea816bcae5d86e92444c1f142a9cb45aaef7a1c9966c28c632b5efd6837`  
		Last Modified: Fri, 14 Nov 2025 01:51:31 GMT  
		Size: 108.3 MB (108283613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d1e2b6deff2c5adf1fab90eaedd93bc9cee497b38e9f6b6e20065ac57df2ef`  
		Last Modified: Fri, 14 Nov 2025 01:51:20 GMT  
		Size: 9.8 KB (9788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4e88d98a22c533ab65319c96f317d18e2b50d474dfb978b6445258dd40f2ba`  
		Last Modified: Fri, 14 Nov 2025 01:51:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467b5d1ae8feac7799135438b8cec862d0c6bdcffd5926c19feaa907672f96f1`  
		Last Modified: Fri, 14 Nov 2025 01:51:20 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d06efabd0264e7ceb64b5c26d5c016a571e4b9bd6e77e6087348db0a1e397d2`  
		Last Modified: Fri, 14 Nov 2025 20:32:09 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6a9e434b131aeeb3d43034d979c5b63d89f04d426f2bed9df44a3b5b9adedb`  
		Last Modified: Fri, 14 Nov 2025 20:32:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:464f8b1cba7f107b3ed333fc276b1b332387433db638cd58f4432c07ac6adc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df07c73d5cb5f30d926f6c72cb3336ffcac1da95face84f04db0439288297fec`

```dockerfile
```

-	Layers:
	-	`sha256:64474155565de2e9de92c2323851f2ce90e4f60534999213be4c1713a262669d`  
		Last Modified: Fri, 14 Nov 2025 21:12:18 GMT  
		Size: 53.2 KB (53161 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:394e039da147775c57d1c9e5bf7a108429088fbe0fe74fa576ff89809c04e107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165633773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfed2fab164b688b662651796e73c4359bd0d6b77ac177bdaf30aa40dc3a002`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Thu, 13 Nov 2025 21:06:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 13 Nov 2025 21:06:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:06:41 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 21:06:41 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 21:06:49 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 13 Nov 2025 21:06:49 GMT
ENV LANG=en_US.utf8
# Thu, 13 Nov 2025 21:06:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 21:06:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 21:06:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 21:06:56 GMT
ENV PG_MAJOR=15
# Thu, 13 Nov 2025 21:06:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 13 Nov 2025 21:06:56 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Thu, 13 Nov 2025 21:38:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:38:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:38:38 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:38:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 13 Nov 2025 21:38:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 13 Nov 2025 21:38:39 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:35:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:35:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:35:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:35:05 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:35:05 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:35:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb270615848954e048e023b4b3b91e35e7f942e570ac7859868c4a059ec785b`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb722f1eaf84fd544360fca60ec8af94a1d3385ecafb0ce33f4645c4d8795f79`  
		Last Modified: Thu, 13 Nov 2025 21:08:30 GMT  
		Size: 5.4 MB (5368424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ac73f938bede2d8d0b71d2112ae0b4578cc125ae15b73533d4293440924a5d`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 1.2 MB (1208142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e9b5369d12206889008e433fbe718a7c4cf0a7785d73c27651f608c39e2caf`  
		Last Modified: Thu, 13 Nov 2025 21:08:30 GMT  
		Size: 8.1 MB (8066503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cc7c5ad06e2d4ea662fc5f43fae09d9e0795a386f62f9c1baec5fe27db15d8`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 1.3 MB (1283606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad27fffb2fea9f82aeb115bdd927b81c260f90ac97f28644937b05f4e1b4135a`  
		Last Modified: Thu, 13 Nov 2025 21:08:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a67fbbadbbb6c9a29d8a12ffe01107d9283b5139ef0e881c9cfb2675710f6`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f7cad7bb9d9ca433c0daf2a8484d38a28c8a878c35ca752c101040f074c169`  
		Last Modified: Thu, 13 Nov 2025 21:39:42 GMT  
		Size: 117.6 MB (117617664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b008743719ac3e2ace8a2f7ff5a8195faaa88e7375f7cfc6b36843252b860833`  
		Last Modified: Thu, 13 Nov 2025 21:39:31 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f60cacf3dbef4fcebe484f6783ff080a8e8b30b7327410f70940bcb437223a`  
		Last Modified: Thu, 13 Nov 2025 21:39:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cc4a10c6069530e729b4e62a5ced09b8cb3301a6457c1f80c71f5ecccc4677`  
		Last Modified: Thu, 13 Nov 2025 21:39:31 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a97061d3c10be763aa651b045a50ab74b5ce9bfe7bd76170d6f5b142efec0b`  
		Last Modified: Fri, 14 Nov 2025 19:35:43 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca415e1a9df6aa7b81225e0ad7e6214a0b06c120a036c988f94bf7f32e345acb`  
		Last Modified: Fri, 14 Nov 2025 19:35:43 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f5a4a7193255e02d47aa8a3bac328d205948e3a60cd46130ff37e70b3cd9f4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37fa75cef86f9a88782899f2a2c7e6a5402a1f005d87be86371bd36b377858a`

```dockerfile
```

-	Layers:
	-	`sha256:ec233941217b54d052a3917d37b708b5fffdcfd794e32fd69ae149f87f07a9eb`  
		Last Modified: Fri, 14 Nov 2025 21:12:22 GMT  
		Size: 5.9 MB (5850699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:566a64ca37ab1e0e4c197fd8d1d1091eef81275005b118fe9f24246edca12d55`  
		Last Modified: Fri, 14 Nov 2025 21:12:23 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:173165bcc75a3d12d26e4e1281c9a0d8cbaa8869398d4fa2bf8d69fe52390ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162098450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb1a79b7baa12963cb3186c27875f5a7132ece896d91674579d363c501c962f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 01:06:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:06:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:06:29 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:06:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:06:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 01:06:33 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 01:06:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:06:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:06:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 01:06:37 GMT
ENV PG_MAJOR=15
# Fri, 14 Nov 2025 01:06:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Fri, 14 Nov 2025 01:06:37 GMT
ENV PG_VERSION=15.15-1.pgdg12+1
# Fri, 14 Nov 2025 02:49:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 02:49:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 02:49:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 02:49:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 14 Nov 2025 02:49:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 14 Nov 2025 02:49:58 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 14 Nov 2025 19:35:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:35:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:35:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:35:15 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:35:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:35:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f8fa7c9be40e65c6864a8067075ec5b333329c2a64af66826dd5ac9227bbb7`  
		Last Modified: Fri, 14 Nov 2025 01:20:20 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aee8139c54cf291aecadb44b89451118714e2196939c90b774dec33e567b27`  
		Last Modified: Fri, 14 Nov 2025 01:20:21 GMT  
		Size: 4.4 MB (4391303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fb3c76a11d58811e75513137736de479edf26bb633dede480ec83c00ff5782`  
		Last Modified: Fri, 14 Nov 2025 01:20:21 GMT  
		Size: 1.2 MB (1222780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f92f27a0f2e926eed87d09ada3e43f3d25f045220cc9b8fbf4d24c4209869a`  
		Last Modified: Fri, 14 Nov 2025 01:20:22 GMT  
		Size: 8.1 MB (8120665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0522a54daed1b0ec3734c45eec7150c8c4b9fd9096be1a57a695ed6ada4134`  
		Last Modified: Fri, 14 Nov 2025 01:20:21 GMT  
		Size: 1.1 MB (1097023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0aeac068244937cecae3d66002544be8f25d6b576886c2db71f3e7ed6e8f82`  
		Last Modified: Fri, 14 Nov 2025 01:20:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c286a97ecfb3938dd38e57b6779ef0b5c261fccfc81873eb3c40258d0bbeac81`  
		Last Modified: Fri, 14 Nov 2025 01:20:21 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15252e34344a9153042f441c9765b2f06ae07bc398b649f4ea32d695412c09b1`  
		Last Modified: Fri, 14 Nov 2025 02:50:46 GMT  
		Size: 120.4 MB (120361597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fda3b5c7cd735f38c4b33ddef294d9796226976901c1aeb9ede575e50d4459`  
		Last Modified: Fri, 14 Nov 2025 02:50:34 GMT  
		Size: 9.8 KB (9786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91168b1bfcb82270843c57ec32e52bec943148e3cf4be2c9098544a0beb95a9`  
		Last Modified: Fri, 14 Nov 2025 02:50:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed304547ab7d967d6d4d7a0812a852d79f8bd4daf372c1b4a8ecf3b09341184`  
		Last Modified: Fri, 14 Nov 2025 02:50:34 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa4b4522d6ad6140bf021fb8c4ec386de577ecd5a7735007f50f6c5c8c6f10`  
		Last Modified: Fri, 14 Nov 2025 19:35:38 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bd007d79770e3dd5bf1c5dfc48941fdd9dfb0317ee2492bd597ff40d4c492d`  
		Last Modified: Fri, 14 Nov 2025 19:35:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:509c47041371145267d42f292089b01d36fecc348713ca49d872f2b27b469fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b348564ea6b2925bdb8f1069c441e438156563578e0818e78a293b6e4fad27a2`

```dockerfile
```

-	Layers:
	-	`sha256:5afaf6ef5c5281464b37db79ca1fe531c7dcc95b1d42f21948bef78f7361b0a3`  
		Last Modified: Fri, 14 Nov 2025 21:12:29 GMT  
		Size: 5.9 MB (5852058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd1515249f7899792ce9de7baa30e32afba1cab081af0813c64f7cb2e0761bf9`  
		Last Modified: Fri, 14 Nov 2025 21:12:30 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
