## `postgres:bookworm`

```console
$ docker pull postgres@sha256:8d3d8865da57e9f399f678971a35a53ceccaae6d2323ffe737e304707184c3fc
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

### `postgres:bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:96a609bfaff93b7201cd9de54cf8595d15f2c4ba0d10faecbb5fb78d83d24391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157057362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5de80f3a686c48c61c4eb7f66c750899c1fc297aacbe6b1672419aa18ff9f90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:18:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:18:35 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:18:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:18:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:18:39 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:18:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:18:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:18:45 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:18:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 19:18:45 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Fri, 14 Nov 2025 19:18:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:18:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:18:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:59 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:18:59 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:18:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:19:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:19:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:19:00 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:19:00 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:19:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2825d16a9f2ae7196de7ab5a8a98d594bd0a10f9a6e074dcd550c361b4c677e`  
		Last Modified: Fri, 14 Nov 2025 19:19:30 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09fad97f3ddbe00bef791c7e449f91adea63be10a227a9553b723c98c683d67`  
		Last Modified: Fri, 14 Nov 2025 19:19:31 GMT  
		Size: 4.5 MB (4534044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ced016dea8c3e3dfd410f3017eeac4b9bc1b326c6a236b8697a4c0ae44f3aa0`  
		Last Modified: Fri, 14 Nov 2025 19:19:30 GMT  
		Size: 1.2 MB (1249519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d467c2b931f9eba41c260885ec4852bedc113af39bc3e4b3c4ba2fe0fb630c3a`  
		Last Modified: Fri, 14 Nov 2025 19:19:31 GMT  
		Size: 8.1 MB (8066403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ad165c37eae3fd8558f72cf3893be25c8cb4c42efaad78018e2e43849c45fe`  
		Last Modified: Fri, 14 Nov 2025 19:19:31 GMT  
		Size: 1.2 MB (1196392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe060b0be1409970cb1a71bafd49d74d7531e4edd305a684cfe594f34a47018`  
		Last Modified: Fri, 14 Nov 2025 19:19:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ad25a2005d37e95139d94cfcf606929ec30d950cd61f279942776117b8d80e`  
		Last Modified: Fri, 14 Nov 2025 19:19:31 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7eab96b2b99fdaa3c8a3e99ab3ecc6eb179b535eef4748e377caebd8647368`  
		Last Modified: Fri, 14 Nov 2025 19:19:44 GMT  
		Size: 113.8 MB (113752766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764c323da4cb729c1556a1154a2dd870a5c94995926c4dab8c13321d98183c1a`  
		Last Modified: Fri, 14 Nov 2025 19:19:30 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45d968983995256be841bfa7f5d3eb35d3294a5e2be4948f5f4da2da84f36b9`  
		Last Modified: Fri, 14 Nov 2025 19:19:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd12376f634c0d766aaa26077efa46f63e6c3cad137f03e5c188746201ff1540`  
		Last Modified: Fri, 14 Nov 2025 19:19:30 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6507a732e7b4bf8bee241f10d80ea91938107379958bde46afb9530e394a6a`  
		Last Modified: Fri, 14 Nov 2025 19:19:30 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:35f7289c6f31927ece673473e96351b72d005d5fd75be988aa50d857d3f4d68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1eb92b75c1be62491bbeb0a9cc284f79a2c8ac9fd305478df15c536e57d34e`

```dockerfile
```

-	Layers:
	-	`sha256:a98e162a7e7b38e1589369f6d5dde9b9dc5541495d4f79c356e5f77522037db7`  
		Last Modified: Fri, 14 Nov 2025 21:18:51 GMT  
		Size: 6.2 MB (6156487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5553cadadbab24c564e54a78167deed3b563793c3b0ace6c2959b90cba6e15`  
		Last Modified: Fri, 14 Nov 2025 21:18:52 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:55b6f674e552985c34f6142d90396d69c6fa88964483b5a40222774aadc18448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87152081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dd0d515e37c4401e029b572b9662882c7fd94b6c64f918e1f6e024c82c176d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:20:34 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:20:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:20:50 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:20:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:20:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:20:57 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:21:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:21:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:21:04 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:21:04 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:21:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 19:21:04 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Fri, 14 Nov 2025 19:32:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:32:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:32:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:32:58 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:32:58 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:32:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:32:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:32:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:32:58 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:32:58 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:32:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:def4b77141116a067c72a4f39eb9fa70634fe918be6e3df3cf0bc46323be22c7`  
		Last Modified: Tue, 04 Nov 2025 00:12:34 GMT  
		Size: 25.8 MB (25757661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6583851563050769ee9d66e953595803d0660b93501f859dd0e4e834c50af15d`  
		Last Modified: Fri, 14 Nov 2025 19:33:23 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57837587cccf38cee37d36508883fadea3a1bc45ca9f676d6332d4e4482a640e`  
		Last Modified: Fri, 14 Nov 2025 19:33:24 GMT  
		Size: 4.2 MB (4151199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4234ab4d68babd468e42864e5d626fca698892d57c366f86d6edcb725a0543c5`  
		Last Modified: Fri, 14 Nov 2025 19:33:24 GMT  
		Size: 1.2 MB (1220023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ab2854fe8852acd87f4e247a98470a46ca1dce3936a7f11c53357d07c221fd`  
		Last Modified: Fri, 14 Nov 2025 19:33:24 GMT  
		Size: 8.1 MB (8066546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8adec54aacb827f25be150e2908c0b61935ea35908844f61351f7d3a71381b`  
		Last Modified: Fri, 14 Nov 2025 19:33:24 GMT  
		Size: 1.2 MB (1195048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69afa08689788200ad601332c147cc264897187f00acf99386ddd37dcdcb449b`  
		Last Modified: Fri, 14 Nov 2025 19:33:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68386c1c0b54a25e093c27669e9fbcd81164ef652f7a998b35d2a3279c94c73`  
		Last Modified: Fri, 14 Nov 2025 19:33:23 GMT  
		Size: 3.1 KB (3147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3373517938accbbd595c599a648e3ddc51828b10b7a901bf0b6577b771ea2b8b`  
		Last Modified: Fri, 14 Nov 2025 19:33:26 GMT  
		Size: 46.7 MB (46731928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e319c7379dda40503e2e45eb42508515a81e329ece8714adb3898e26519310`  
		Last Modified: Fri, 14 Nov 2025 19:33:23 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8ef3d4fdef369d62fe943041ef086d60ab81ac9ab5e160801b03a95626bade`  
		Last Modified: Fri, 14 Nov 2025 19:33:23 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be06c24ae4c7260d71dd3a95b5e01eaffba56fdf0be31385236be941c313d1c`  
		Last Modified: Fri, 14 Nov 2025 19:33:23 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88060516a4c395d80c2767a64b9af56199c908b19e5a86c1782fd58c71134434`  
		Last Modified: Fri, 14 Nov 2025 19:33:23 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:86de1a2e37781cfb7c3e6e276cca1972be9eff526eb13ea2bdc1cb3d11fffee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb506fea9b776253020dec664836aa0123e0fb49f498e999f9f50fd8570503ef`

```dockerfile
```

-	Layers:
	-	`sha256:7fa1a25ae4d750862155e847eb50da32f9200c67cc06cfd57893c3dca60cd1f4`  
		Last Modified: Fri, 14 Nov 2025 21:19:00 GMT  
		Size: 5.3 MB (5317006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0f3597ff0923d2a489a532342f91939790374856738532b5317431e55428e9`  
		Last Modified: Fri, 14 Nov 2025 21:19:01 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:be1231a99a72c911c89ba237b9c08f4c5fe3868b8346e2e6c42bbf883263b8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83277014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb9c7689e0f9e09ed5a53cb08affbe66b2b4402a840a30caf99358412697519`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:22:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:22:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:22:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:22:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:23:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:23:03 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:23:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:23:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:23:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:23:08 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:23:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 19:23:08 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Fri, 14 Nov 2025 19:34:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:34:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:34:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:34:27 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:34:27 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:34:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:34:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:34:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:34:27 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:34:27 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:34:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dae611a010be6eab1cdff516b7db8214a5d92b74372702ade8cd5e6bb793dfdd`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 23.9 MB (23934126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f938f8fa2e74fd1797642b36eb1eaa82f84b121d463a1877fc11f4dbd7051e`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32192eee72583a220f92e6b20624e8c5e54f39fcd4d2868fea051345cbac464a`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 3.7 MB (3742621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17b6491688748b24c9be0c13cd25cdb6a89955f998dfcf9015394d24ac84a50`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 1.2 MB (1215946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8918a8f710f2ee816680f8feb56a3d1588b1d28960965b68364da61966fec4cc`  
		Last Modified: Fri, 14 Nov 2025 19:34:50 GMT  
		Size: 8.1 MB (8066396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3b56d27d2534bf60a5d8fc2c737dff996ce6fd389e34dc9e5492058f89d21f`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 1.1 MB (1067230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb6a12119f803b7e40ec7293563f54d66bfd591b71c51b799c6fa9f994e57e5`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504b209e972547b6f8c6f00853f6c5c4e461b95f1596810ee4abf1f3ea835a88`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1e0dc7b5f4fde4e81e6d091f2415070e5cd765043c6d495f6e377a794da3bd`  
		Last Modified: Fri, 14 Nov 2025 19:34:53 GMT  
		Size: 45.2 MB (45221026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fd104a797db41b04bce887e18e6e3b474b843b9d729ff77d11f0e57d59db19`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7c7336cd872459fbb71e142f46d71e602630629625e0fc2dd6efc2fd106611`  
		Last Modified: Fri, 14 Nov 2025 19:34:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be7038a48e06d257ad253fa5db305b5c54ab7f7102aa1bc7657be36f1796d49`  
		Last Modified: Fri, 14 Nov 2025 19:34:50 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f496220939d055bd687e42c2ab514f00c2f797a58f444f602aef641881f4444b`  
		Last Modified: Fri, 14 Nov 2025 19:34:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:22faf460fddf246ef04465b6c152a540172faeca23a0acf10c992acb873b8344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7da5e26533b98839b19df81e3f41d10d210e2c15df6812478ce1662366cdbe`

```dockerfile
```

-	Layers:
	-	`sha256:eab0ef687af2c15d19e4b52f23159359383113b29cadc7efdfb48631fdef3f21`  
		Last Modified: Fri, 14 Nov 2025 21:19:07 GMT  
		Size: 5.3 MB (5316257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371714eaa3b9b69a1daeeaf4339da80564ea148a1648e5dc61db03e73464b05e`  
		Last Modified: Fri, 14 Nov 2025 21:19:08 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3d2b8c1d7474908e356ed490cbd7ac107d58aa5c12c6534cbfe70eb5fbbc6eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155019331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b7eedef193d5b0252147c8136e90bae9a0d4df9462b05c9eed4156cdfb59a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:17:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:17:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:17:55 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:17:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:17:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:17:59 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:18:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:18:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:18:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:18:03 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 19:18:03 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Fri, 14 Nov 2025 19:18:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:18:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:18:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:18:20 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:18:20 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:18:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:18:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:18:21 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:18:21 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:18:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4d5ca5fc94cf00faf70a97004267545fb157cd0b48001c852b64754d0b3b41`  
		Last Modified: Fri, 14 Nov 2025 19:19:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7658a4f50a98dab272836edf967c8d18667e85f67a1513189a002e09252234b`  
		Last Modified: Fri, 14 Nov 2025 19:19:04 GMT  
		Size: 4.5 MB (4519820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143b5bf3a74c65ab121fd1c80cc264b8ccd982c0264f4a80df1e9f797433ee3`  
		Last Modified: Fri, 14 Nov 2025 19:19:03 GMT  
		Size: 1.2 MB (1203263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333bf7361ce63b55e2fed995148efd21618cbb41a7292166d6ec34acca186ce6`  
		Last Modified: Fri, 14 Nov 2025 19:19:04 GMT  
		Size: 8.1 MB (8066449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0c1c3afb34b3e7059c1381c2e85b234099c74b2748e0447b7356f9ba58f3cd`  
		Last Modified: Fri, 14 Nov 2025 19:19:03 GMT  
		Size: 1.1 MB (1108966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b29e2391c16964a2771e65ef5683fa067e32abd54023b5b96ce10576a8b27`  
		Last Modified: Fri, 14 Nov 2025 19:19:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e478ee0bea28379dcfe936689dcba7ae75ba798d560546f8274e06acd2e01b`  
		Last Modified: Fri, 14 Nov 2025 19:19:03 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416c1cc3d9be780d3ad53cc08662683f137feb55e6fb35fcaa4b99d75ceb8399`  
		Last Modified: Fri, 14 Nov 2025 19:19:15 GMT  
		Size: 112.0 MB (111988788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a13d84bb81b2c427310081bba15f606c9e0c39006ea83cfff0059f80602fd`  
		Last Modified: Fri, 14 Nov 2025 19:19:03 GMT  
		Size: 19.1 KB (19092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d178dd935ae58b61c1f1dad9eb7ff3738fb8c5031cafbb5d576b0e70e4ae90f`  
		Last Modified: Fri, 14 Nov 2025 19:19:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3a70a4ac064d1d8c02d217024dfe3e8c47ec7e304c44de23574108be078b4f`  
		Last Modified: Fri, 14 Nov 2025 19:19:03 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fc506943d7685f9e7c20f3fbdf2626c728db044398984db0669668cc4d8683`  
		Last Modified: Fri, 14 Nov 2025 19:19:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:08600402124a28cc626ef817ee3681c42356fbe77bb94938ce999c439e57a937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591e3cac4b380356519f2e7a2fe13b65a872209f6b7a7cfdaa06188879c55ea4`

```dockerfile
```

-	Layers:
	-	`sha256:cf1f538a29991260707e66abdad8430d4e02a29108ed2d7fdc946f8b0d16ce15`  
		Last Modified: Fri, 14 Nov 2025 21:19:13 GMT  
		Size: 6.2 MB (6162812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91c9b349cc10518242b5b78573b13129cc6ad753079a4461b6f7dd8366f38fa7`  
		Last Modified: Fri, 14 Nov 2025 21:19:14 GMT  
		Size: 51.8 KB (51832 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; 386

```console
$ docker pull postgres@sha256:20b35489c3826a8204942374a80b10f569e2b3b5608c2422cdea09125295d104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93932958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67771f15e35da17c7c4e2485a6a959a16ac99cd958ce3ea43fa8feb3eec7dff6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 19:19:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 19:19:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:34 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 19:19:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 19:19:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 19:19:39 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 19:19:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 19:19:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 19:19:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 19:19:43 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 19:19:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 19:19:43 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Fri, 14 Nov 2025 19:28:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:28:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:28:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:28:39 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:28:39 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:28:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:28:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:28:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:28:39 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:28:39 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:28:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727e079d64d0a29c2bed64ebf9f5ea06715aee8cf8bf0f508f9b161672c94f8b`  
		Last Modified: Fri, 14 Nov 2025 19:29:01 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fe89d44b100c2efd40f2b615590f700fa38fbbbeb481fc95effe8d662a77f4`  
		Last Modified: Fri, 14 Nov 2025 19:29:01 GMT  
		Size: 5.0 MB (4965331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7899e567d909bff01af28f760559372607c9b316207e3c39f9a4e6b3abf574`  
		Last Modified: Fri, 14 Nov 2025 19:29:01 GMT  
		Size: 1.2 MB (1218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb33bb25087aa5c09e410a9e0d0dbce83874152c66080ca969c5146224a6659`  
		Last Modified: Fri, 14 Nov 2025 19:29:01 GMT  
		Size: 8.1 MB (8066477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2216ef793e4cdff6f082357d40a759915d1f106bd84d4cae2ca3be2d6951cd5e`  
		Last Modified: Fri, 14 Nov 2025 19:29:01 GMT  
		Size: 1.1 MB (1137407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2db3dd76baa5444eea7f254a76045218460434c9d185bb55b184d26677762b0`  
		Last Modified: Fri, 14 Nov 2025 19:22:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdcf07d803ba86b52398f832ed61589d6c7c29f551e0f01e6d83a80e2cd4270`  
		Last Modified: Fri, 14 Nov 2025 19:29:01 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7a660d9c77759da70a7e13e68b50f3069239e310df7f7ea2cb4d426626a105`  
		Last Modified: Fri, 14 Nov 2025 19:29:06 GMT  
		Size: 49.3 MB (49305621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23300b391c01229dd37df86e7335cafab3ef37ec7c5457103418d56c56a67e53`  
		Last Modified: Fri, 14 Nov 2025 19:29:01 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9da0f3433bcabcb09fb9b96cd6b158c49bd20a86f3c21cc4bf2e381bfc7ed1`  
		Last Modified: Fri, 14 Nov 2025 19:29:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71839bdd3bd86dbb7d8e17fb78282ce62f5acebed7e3a5c89c39599af026627b`  
		Last Modified: Fri, 14 Nov 2025 19:29:02 GMT  
		Size: 5.8 KB (5843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60159445c322436c210a705023ee4293b6787e93f824215dbafdb535410558b`  
		Last Modified: Fri, 14 Nov 2025 19:29:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f5984c9cea282f8fe64cb55600a6bfff2c40c58dd9c3afe7b845a70bac78d694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba152c0c8eb4758cce9ae087a9781f056fad829bbcca80e3bb0e0dd973e81153`

```dockerfile
```

-	Layers:
	-	`sha256:6688741f4f95b59dbe32817c50a8c81d4c3a0790dd5a843cf47fcd65ab964f46`  
		Last Modified: Fri, 14 Nov 2025 21:19:20 GMT  
		Size: 5.3 MB (5311572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeff60f914244f14aafda05ae057030d7af04fc38a847e418a7bd002be83bc1c`  
		Last Modified: Fri, 14 Nov 2025 21:19:20 GMT  
		Size: 51.5 KB (51538 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:b224c8c090e46dc6555a9448d6c34f9414c580473bad6e51c0f74ccc9e42dbb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155913733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e2aa87d122a4b7e35ff63edacd02ffdf704d5315c270f758267c6c365d4e7b`
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
ENV PG_MAJOR=18
# Thu, 13 Nov 2025 21:07:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 13 Nov 2025 21:07:02 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Fri, 14 Nov 2025 20:26:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 20:26:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 20:26:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 20:26:59 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 20:26:59 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 20:27:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 20:27:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 20:27:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 20:27:02 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 20:27:02 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 20:27:02 GMT
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
	-	`sha256:f35cff4123b548b3414f4bb83ce9de837602253791c7286017ffa3ee839c067f`  
		Last Modified: Fri, 14 Nov 2025 20:29:45 GMT  
		Size: 112.5 MB (112485781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc5482f75ed96393d4ca9895917c2901974bb3d9d5644acc0ca1de0e8f4459d`  
		Last Modified: Fri, 14 Nov 2025 20:29:36 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3114fff0bd2116aeaea6171950379ca10c382c1fdb183a0a8519107f8fc4ca94`  
		Last Modified: Fri, 14 Nov 2025 20:29:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd4c60b26d8d416374c1c131478cced7d68a217df22e26e172d137870bd652b`  
		Last Modified: Fri, 14 Nov 2025 20:29:42 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f1b948bda390b10098684821429b504c8d32888ab82237322588d0b5288ee1`  
		Last Modified: Fri, 14 Nov 2025 20:29:36 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:74f80f38f12f80243312043c4b18bce2f63ad04ba49691e7e84500db6c7b4966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 KB (51462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1440780be7118227227a402ff3651b03b37ab29be5dfc0e29b68a1bc6567ba7`

```dockerfile
```

-	Layers:
	-	`sha256:02bd57b9c7298ae4c068f59c58303b96e6a5643c21eac14af30fb5a15fe2e8b3`  
		Last Modified: Fri, 14 Nov 2025 21:19:25 GMT  
		Size: 51.5 KB (51462 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:a41656ca4f126de2c5823cac9b0efc0efcb0ebc90e536e35ef72a9a14e4478ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169939682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e531652750dee1c0a5abd9fb39207b480fc255b408e9fd8d98d0250bb33a05`
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
ENV PG_MAJOR=18
# Thu, 13 Nov 2025 21:06:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 13 Nov 2025 21:06:56 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Thu, 13 Nov 2025 21:07:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 13 Nov 2025 21:07:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 13 Nov 2025 21:07:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 13 Nov 2025 21:07:30 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 13 Nov 2025 21:07:30 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:30:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:30:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:30:25 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:30:25 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:30:25 GMT
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
	-	`sha256:570fcf0336a04f0782510713285b489a426e11e301a298290a6131a1894c99a3`  
		Last Modified: Thu, 13 Nov 2025 21:08:42 GMT  
		Size: 121.9 MB (121914433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829a8a389a2e3389013abb3896fb987339177e20c9770983a1229476c280998a`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583b149b01468e6bd997f33da02a729e24f2e0bc7f59b11392ccd9e466ad33b3`  
		Last Modified: Thu, 13 Nov 2025 21:08:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b7a7494a3d38a3e7c86689a6f893c71897c6eef488e6110a2dee329b9bec21`  
		Last Modified: Fri, 14 Nov 2025 19:31:07 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31352de829b6b654615552c3ec71b055c64c7adc255e7f97514e38292bd7a60`  
		Last Modified: Fri, 14 Nov 2025 19:31:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b0153704c192f1bc5f983bc7f640fc34e4a59c4680cf2852b3702caf2939f8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edf5fa9b37aac963302a1c88e0457072a167fd4d665c7d5300faf795c78ecc7`

```dockerfile
```

-	Layers:
	-	`sha256:a446b44d92211f6cf1ba308ee72375b9c124f36a5ad677d312056bcf5bcfa334`  
		Last Modified: Fri, 14 Nov 2025 21:19:29 GMT  
		Size: 6.2 MB (6163872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb5eeda01c29a257c6f01abd3962f391ccf2a05b8eb2531b50e9b41500d5560`  
		Last Modified: Fri, 14 Nov 2025 21:19:30 GMT  
		Size: 51.6 KB (51648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:9e4fe4369988c3ffa8fc802bb480e9fa92669307112f78069f44f3f8a3526e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166370467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe1f0d0a93011c2e33b8c9cc2cf79494de899fa07c1b02ee48f903ba890b124`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 01:13:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 14 Nov 2025 01:13:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:13:48 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 01:13:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 01:13:53 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 14 Nov 2025 01:13:53 GMT
ENV LANG=en_US.utf8
# Fri, 14 Nov 2025 01:13:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:13:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 01:13:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 14 Nov 2025 01:13:56 GMT
ENV PG_MAJOR=18
# Fri, 14 Nov 2025 01:13:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Fri, 14 Nov 2025 01:13:56 GMT
ENV PG_VERSION=18.1-1.pgdg12+2
# Fri, 14 Nov 2025 19:29:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 14 Nov 2025 19:29:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 14 Nov 2025 19:29:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 14 Nov 2025 19:29:30 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Fri, 14 Nov 2025 19:29:30 GMT
VOLUME [/var/lib/postgresql]
# Fri, 14 Nov 2025 19:29:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 19:29:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 14 Nov 2025 19:29:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 19:29:31 GMT
STOPSIGNAL SIGINT
# Fri, 14 Nov 2025 19:29:31 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 14 Nov 2025 19:29:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147120a275748d7cfba32c7910cfdd1921b82567283d3f4872b29d3332df0cb9`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c4dbe2517a4fe7544130e6b0f0c1fdb94aca456f3aac1d7c02b5ed01f5cd44`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 4.4 MB (4391284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6596bc653f8082ee398adac92ec9eeeb716e58a3ff8dc430e86ab5a62e379f53`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 1.2 MB (1222779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dfd95f329d9b74ae2398d490dec8eb6362df90f950e7dfd6f7b8fcca8ba92c`  
		Last Modified: Fri, 14 Nov 2025 01:26:43 GMT  
		Size: 8.1 MB (8120661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe45344ee09474fa4b6ee71a5418dc97a3568680ceeb233e3cce2390bf5c976`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 1.1 MB (1097014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3440c5db601ce3b77d5499d0b8bae3d7b2e8fa0bb886209b43bf5f0dac95a1e6`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44adc8c24a16e584037f1d62236ba2c26a6a40b5d7d6d65244a9f196c29e4839`  
		Last Modified: Fri, 14 Nov 2025 01:26:42 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acad9cb1b2963651a882379bce703488dacce2f109a09e8b46e514e2bf82005`  
		Last Modified: Fri, 14 Nov 2025 19:30:41 GMT  
		Size: 124.6 MB (124624509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d57dfaaa42127b43e7be92b4bdb9ad84c2ff75843666e39d6810c2683849af`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40324e08aac49920eedcbcebe60fad0badc6032e0ceb132caa3a73d93bd51813`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d74f6133bc38a733c71bb6b3b4cd0bd55abbe2a3881fc9e098adeeb29181858`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10b25cf4862b19a21be219dd3bf21f2698c52e434a94088ea2d743d316e7225`  
		Last Modified: Fri, 14 Nov 2025 19:30:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0e1aeb5e90652ca6902015982311486c331fac8b71b697e9be5a8d50bac48fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55255e921ee3fc13c9997472003e44714bddcf66bcf5f0534f2e4c1b335052a`

```dockerfile
```

-	Layers:
	-	`sha256:292f03466a9bae7f02f64611bc34c74f81d96089aacd64cf88744752742ca0a2`  
		Last Modified: Fri, 14 Nov 2025 21:19:36 GMT  
		Size: 6.2 MB (6171145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6770e43cb1cef54440d29ac9b5b1de3b3854e3f341379ec2d317d06a9da5128a`  
		Last Modified: Fri, 14 Nov 2025 21:19:37 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json
