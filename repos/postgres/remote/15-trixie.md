## `postgres:15-trixie`

```console
$ docker pull postgres@sha256:9d6e29202285894b16c99a14f8bb2df5a37a98791f4840d98c318de545ade08d
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

### `postgres:15-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:5fbbf7b4bd0c7f7faedb9814ec02cb8b639f44ccd5e81e5332e55e7b6b0f32b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158082939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27deb4ec2bb412020350d8127f6264073edc0cecb7fe39d4af339898c55a47f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:16:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:16:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:16:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:16:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:16:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:16:37 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:16:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:16:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:16:41 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:16:41 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:16:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:16:41 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Tue, 19 May 2026 23:16:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:16:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:16:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:16:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:16:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:16:55 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:16:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:16:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:16:55 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:16:55 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:16:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faac557a4014a17628e2db68f7de97eb4c058c823ac41dbfa8561588d8805b99`  
		Last Modified: Tue, 19 May 2026 23:17:15 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ae1f680f8fdc0f4e0f1e0d8e87fc4e750263027edfbd6ba44bc581613cf2e9`  
		Last Modified: Tue, 19 May 2026 23:17:15 GMT  
		Size: 6.4 MB (6443069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85a6fe690f88c439a226ac8a182411e147575a5059156ce71c452f717799fab`  
		Last Modified: Tue, 19 May 2026 23:17:15 GMT  
		Size: 1.3 MB (1256748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b56273edfa048a23a0fbcf5570c582fa62dff15188243922ce7ca5aca2aab5`  
		Last Modified: Tue, 19 May 2026 23:17:15 GMT  
		Size: 8.2 MB (8203893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e78423263b4c996878a3adf873fd2c6af354bfb888e176a742ee91feca7ac3`  
		Last Modified: Tue, 19 May 2026 23:17:16 GMT  
		Size: 1.3 MB (1311655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64c84d18f1577702385a31b968f5f78d4c768c94abdcfe9dd1fdfebfffcd21a`  
		Last Modified: Tue, 19 May 2026 23:17:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15d3b4493f31a0af549f202c220366d406e1f2e9b30a27d00d2460f0abfa072`  
		Last Modified: Tue, 19 May 2026 23:17:16 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450a0feadfd82a230f8454e862734ac43a7734eaf916f9d9d6a1a9fe29bd8c2b`  
		Last Modified: Tue, 19 May 2026 23:17:19 GMT  
		Size: 111.1 MB (111066759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b5a6f40056d82c20e79211ff6d6a70c9eeccfcd017168e539af092d5515b1`  
		Last Modified: Tue, 19 May 2026 23:17:17 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dde53e1bfde004d6fa7361be182c76b37e371a55b1ec5b9a5bb46760e72955`  
		Last Modified: Tue, 19 May 2026 23:17:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2378712a6f4c8eb9e5ea419651e4fa7ff8446a5ab6da799f83d40a1b0ca286`  
		Last Modified: Tue, 19 May 2026 23:17:18 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1622e7a6bba67107a405a20730597831294cf61c6b1bf8d07153b475d4fc4f76`  
		Last Modified: Tue, 19 May 2026 23:17:18 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b99619cea162d89518420737050435af92ff733d755800089e6cd6bed1ea13e`  
		Last Modified: Tue, 19 May 2026 23:17:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:72fcd8ca2f7cb132d0c6387d48b00eb40c2c2f87e320f41b52591662637b14d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7061b8532f0cc5c0fc3cebdb86baa4bf84484dbfc0c422f4f3904e05cc2f6273`

```dockerfile
```

-	Layers:
	-	`sha256:3406b32a57ce7b67071f2682a52059e03271939f17393c77488aecb2772b86b5`  
		Last Modified: Tue, 19 May 2026 23:17:15 GMT  
		Size: 5.6 MB (5642596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:040bae07de180bcabd99caa4f22e9919e7275e323c8ceb2cc267c2904e8cb28d`  
		Last Modified: Tue, 19 May 2026 23:17:15 GMT  
		Size: 53.9 KB (53863 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:24750c46ca447f7db356af3bb6f00bdaa7c9ec32d30fcd98b60c1f5124c69987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152111499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5be4e60b915c2dc5c28c841ade5342091f74df7eeac97a0af44c81249a634f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:28:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:28:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:27 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:28:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:28:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:28:35 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:28:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:28:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:28:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:28:42 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:28:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:28:42 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Tue, 19 May 2026 23:44:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:44:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:44:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:44:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:44:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:44:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:44:18 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:44:18 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:44:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c121de7bbea1ecb6eb191cc3cecac813c759b709295288fd5e2ba0855596410`  
		Last Modified: Tue, 19 May 2026 23:44:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ac59b843129c706a803cbe15fda60487b510c6c8cb61acf508d5aefb2d6294`  
		Last Modified: Tue, 19 May 2026 23:44:36 GMT  
		Size: 5.9 MB (5934325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcf19d436da51c0f81acee6ed03ee2b19c32d33e92af164821c0bc92b3083ca`  
		Last Modified: Tue, 19 May 2026 23:44:36 GMT  
		Size: 1.2 MB (1227545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa0ae2e37973c8e813b26f49b632ee9684f2aa85521120cdeb89faf59cf3c13`  
		Last Modified: Tue, 19 May 2026 23:44:37 GMT  
		Size: 8.2 MB (8204289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386c5660cf4530c70f5ceefec09fd30d5ab05b645dc134af5f00ef56a58071e6`  
		Last Modified: Tue, 19 May 2026 23:44:37 GMT  
		Size: 1.3 MB (1317313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d204a20b83b1259065c4d0302bee56c85201ba6d7b50d71db5c15dc83c4b6c`  
		Last Modified: Tue, 19 May 2026 23:44:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640cbe1d3c11a2b45ab54f83b6839838504e055f4a9210e2ab0ccc39da09025c`  
		Last Modified: Tue, 19 May 2026 23:44:38 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c175ab724b01e9c322709204679170ce798040cb0b91b99e22421164d874dca6`  
		Last Modified: Tue, 19 May 2026 23:44:40 GMT  
		Size: 107.5 MB (107453271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb01903cec1c62e42e517d11ac43305247244d7ac79d2f43e9f62f783ea2604`  
		Last Modified: Tue, 19 May 2026 23:44:39 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c082fce296bf626fedb7c47f336d3d475ff55de023e2419b63d2c5050bae94d5`  
		Last Modified: Tue, 19 May 2026 23:44:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082ee82e79c6e425ccf6fec9f8910c31b47e4f1c9b6e401a39e239b9e70af68c`  
		Last Modified: Tue, 19 May 2026 23:44:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174ca82f3830734a341d8ed3241cd722c176c8e8701187e267ff7c053fec2ffd`  
		Last Modified: Tue, 19 May 2026 23:44:40 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21829001e8e56373e92e12b2deb77ebbc5acfd684a123c61b5a9f21648e0214`  
		Last Modified: Tue, 19 May 2026 23:44:40 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e4b00f463cc2eeb3d23d970836b157720a2b58fde32a937bf64f5b43ab4db2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801e97f6be48e77e790944c65a31b0a9ef2537e79400cdea7cab488bfe6b6476`

```dockerfile
```

-	Layers:
	-	`sha256:3425a857cff8ec354589a124dccb055a743b68dc43bf48ef49d96a1949a0615b`  
		Last Modified: Tue, 19 May 2026 23:44:37 GMT  
		Size: 5.7 MB (5659238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e770e65b37d0ead2c6f460fdab9530e0ac72b57a1e7da1a101a939ad9e0f95`  
		Last Modified: Tue, 19 May 2026 23:44:36 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e5180d5ea21882238fcaf3ee91a1839df68196c027cbbee4fde406f2622637ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147169766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3189c946f3a55f7d85cc1a1033493e6ca27186581300df491392a834c4fabf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:44:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:44:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:45:04 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:45:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:45:10 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:45:10 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:45:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:45:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:45:16 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:45:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:45:16 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Tue, 19 May 2026 23:59:19 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:59:19 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:59:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:59:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:59:19 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:59:19 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:59:19 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:59:19 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:59:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:59:19 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:59:19 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:59:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafab200771dcf8d3ab75a4dc9ac18ec5d5ecfbd5d0e8f645d0456787d638592`  
		Last Modified: Tue, 19 May 2026 23:59:37 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826a695423973c567225800d053e0ba3e5c003ebb1a7a55cd61545c405e28d2d`  
		Last Modified: Tue, 19 May 2026 23:59:37 GMT  
		Size: 5.5 MB (5497149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255cefabd676d94927f18ea0013ad19a9a3b5bff421e4edc5c0afdb07838bca4`  
		Last Modified: Tue, 19 May 2026 23:59:37 GMT  
		Size: 1.2 MB (1222424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb75d45320459c8ef87b829ecaffd1c83ca7cf3d9652756abb30bd7dd01d236`  
		Last Modified: Tue, 19 May 2026 23:59:37 GMT  
		Size: 8.2 MB (8204127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551bc3301fb90bf0bc5aea21edd04073745d66e95962bceafa4fb494cc2fb7f3`  
		Last Modified: Tue, 19 May 2026 23:59:39 GMT  
		Size: 1.2 MB (1172652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff9152e59f86ada14d85ae9f0c0feb1e1c3514fa3d31ec52245d72548349191`  
		Last Modified: Tue, 19 May 2026 23:59:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350f65d1e0421bba06e59ae8b9df13bdcc95f6d6f5740f4695d138f0084f86ac`  
		Last Modified: Tue, 19 May 2026 23:59:39 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b70f2710dc77ef35a35609c708e1ae9a0dce4a3389a7f3468f9cb4da93ab57`  
		Last Modified: Tue, 19 May 2026 23:59:42 GMT  
		Size: 104.8 MB (104846685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8600085671e2e49b3ec8e37b6c80a0893e36e6acb2d5ac9d7d8b7394729363f2`  
		Last Modified: Tue, 19 May 2026 23:59:40 GMT  
		Size: 9.9 KB (9894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e656b9e43bfcb15a18db018500679a7726a129c8e27f6ff4c0d122ac81a61cd4`  
		Last Modified: Tue, 19 May 2026 23:59:40 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209ebec2304b1da9f3144e14831b9a30d15390c5d39bad50843f68504452525f`  
		Last Modified: Tue, 19 May 2026 23:59:40 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4d3f2a6eb07a553172a84f404b34cb2e5d254c44a0562235ea44d8be6679e8`  
		Last Modified: Tue, 19 May 2026 23:59:41 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2019e694b7cec18a0f45c3beeced6f35e16b75603914784a07dc47b4801d7a09`  
		Last Modified: Tue, 19 May 2026 23:59:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:041467abb5c85a5871dae890a9191ba49b18af3eee77f1be686f6fff79b7839e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5712630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57607309e2cea5ec18d8eb1a4512e730c1c9fed6310ec9229de3c19b492d276`

```dockerfile
```

-	Layers:
	-	`sha256:4cbf1cf0d57e60850099fb6d9c632a07b4edc5b2c051f4808d782d217ad9eaae`  
		Last Modified: Tue, 19 May 2026 23:59:37 GMT  
		Size: 5.7 MB (5658543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcdc7937dc5ef316ec83fbead9a8f6341be4200b106a2cac8652f2ea0023bcea`  
		Last Modified: Tue, 19 May 2026 23:59:37 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:04b9e2d7e8ef2577d4deee76e0d2ef51cdab40769d9f1b7e1b21029bd16a80ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156709231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cfa4f22776adcca8436859d21c0769b0b6b479ba14a9d12c2a2383f4b4da5f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:19:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:19:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:19:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:19:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:19:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:19:24 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:19:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:19:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:19:28 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:19:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:19:28 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Tue, 19 May 2026 23:19:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:19:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:19:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:19:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:19:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:19:48 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:19:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:19:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:19:48 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:19:48 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:19:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f6c97e2134719716828baf25a7b5febe2b6b1972f652d0fb00e7319530feeb`  
		Last Modified: Tue, 19 May 2026 23:19:55 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b626a36d2076fbd42c5737bf3250e9b67b61414d96b763215d3f643e2e3f79`  
		Last Modified: Tue, 19 May 2026 23:20:09 GMT  
		Size: 6.2 MB (6235493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32cf8bf242d172392bde630ed1d79e3f59a36aa5a6029a08a8801efcb9b0cce`  
		Last Modified: Tue, 19 May 2026 23:20:08 GMT  
		Size: 1.2 MB (1209531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dad84d6372fefcc2bcdaad8b0515437fc9030778f76bfda9d458577550e80c9`  
		Last Modified: Tue, 19 May 2026 23:20:09 GMT  
		Size: 8.2 MB (8203940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14a63c25e2c13900812ec92b7c7d4a295bccf78fbbebc57f64251d039297090`  
		Last Modified: Tue, 19 May 2026 23:20:09 GMT  
		Size: 1.2 MB (1220554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4016e39418b160aa67836013be1d87500331e52470d2371797564aba29063f`  
		Last Modified: Tue, 19 May 2026 23:20:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d220de485c4bb493ea9b91d21fb0414b1d46e215fc51057ab95ef9c05bb8534`  
		Last Modified: Tue, 19 May 2026 23:20:10 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7089f30154bc8b9c653f94ca63c5e8faf1b6028b97e26485aa0d3233e7282a89`  
		Last Modified: Tue, 19 May 2026 23:20:13 GMT  
		Size: 109.7 MB (109676903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00664a0026e5b677e3beed8cf7b06de8bf58bf5b361cd881df2be0fcba4920c0`  
		Last Modified: Tue, 19 May 2026 23:20:10 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25c7ba8682809e7a3401ef9027bd3aaf8480d265a134740ab880ccb4541ffef`  
		Last Modified: Tue, 19 May 2026 23:20:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4a0ab3f05be674027d7688399dc3655c0b9f1b6e7dc5d6a7a18b0343d89cc9`  
		Last Modified: Tue, 19 May 2026 23:20:11 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3102efc973b26cb319f680c5ef4ce38d929e78dd17914f6903058b42c463bc21`  
		Last Modified: Tue, 19 May 2026 23:20:12 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb5cb84b126376d8c8ea20f0a6f91f62b3a2e217bbae2be62e3ced8d6449303`  
		Last Modified: Tue, 19 May 2026 23:20:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:76e30232a321f01b841bec4e584f55bf0bc1fe37d161ef3b86213ab0749daa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdfe15f14139762611b9cdf551e21b067c4cfe43d2204b8d511813120c2cc1d`

```dockerfile
```

-	Layers:
	-	`sha256:6caa64f9d1aeae379444dbe47ceb023fa1aa011e256029ade62065987508f9e4`  
		Last Modified: Tue, 19 May 2026 23:20:09 GMT  
		Size: 5.6 MB (5648934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bdf5901abf412598dd0a13885b5fd6ab014193c6b2705a0dd1c5b425d0b0ce0`  
		Last Modified: Tue, 19 May 2026 23:20:09 GMT  
		Size: 54.1 KB (54133 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; 386

```console
$ docker pull postgres@sha256:d71961602c1420e183310694830fe95eb2f109c1cfb9b56729535dd09fbd206f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167178061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370135ef9b0e475c3b9a3d9c2a4c4572b6e1fc0801a9e633ed0281a72ff8fbee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:14:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:14:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:14:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:14:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:14:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:14:23 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:14:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:14:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:14:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:14:27 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:14:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:14:27 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Tue, 19 May 2026 23:24:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:24:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:24:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:24:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:24:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:24:42 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:24:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:24:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:24:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:24:42 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:24:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402f667af6d1a83a510cb4ca97d3e463291dbfb52d53af86b941f4fbafc86349`  
		Last Modified: Tue, 19 May 2026 23:25:01 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6588b12b6a75e4d9076f4d4ebcd63a51e4f36c5aef33f1f615bd61fee029919`  
		Last Modified: Tue, 19 May 2026 23:25:03 GMT  
		Size: 6.6 MB (6631370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7d9ac3ae342fdf12f3a4312601ec77633b0f80d0446373084d4456faae25c8`  
		Last Modified: Tue, 19 May 2026 23:25:01 GMT  
		Size: 1.2 MB (1225806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1254e72887f61519d3e800682d01242d58b4a395102e3cf27120cf6f955d718f`  
		Last Modified: Tue, 19 May 2026 23:25:02 GMT  
		Size: 8.2 MB (8204060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4184c3b39b95d5eedbcc2ad32ced9668633042961744954f9ef8edb32687d6f`  
		Last Modified: Tue, 19 May 2026 23:25:02 GMT  
		Size: 1.3 MB (1308261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacc7f2ed5564333e04c0ad4a667d148f76706a98912f38f4f9b013d0954b9ba`  
		Last Modified: Tue, 19 May 2026 23:25:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a1efec42dafa56445270cf12a2d5a8d18912d41d9df5a220c12a48781bd9bf`  
		Last Modified: Tue, 19 May 2026 23:25:03 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a4d15eeb8883907c530b579b5af44d2a882e2c90ab60d7fdaad37685b78b19`  
		Last Modified: Tue, 19 May 2026 23:25:06 GMT  
		Size: 118.5 MB (118492338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081e9c58bc6cbbdf7df34581a3ef15a3819e791e1237fcd25986b1e80814b9f6`  
		Last Modified: Tue, 19 May 2026 23:25:04 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffdfb3de8a003f884d2415788f24ccaee95777c11ca0400e18c4fd6cf35c1e0`  
		Last Modified: Tue, 19 May 2026 23:25:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70da4d2e73435a2d57a8d86f4e6ced002a691466221d4a033d741e44e31908a8`  
		Last Modified: Tue, 19 May 2026 23:25:05 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dc3ddf0d244f914c868e8ae5d3a8f17d394fdb02fa1e9c97ed07543d2d2481`  
		Last Modified: Tue, 19 May 2026 23:25:05 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9c1ab8f6392d39e54e775143930c0c548ddd42f43abca31eb972adfcacf6b3`  
		Last Modified: Tue, 19 May 2026 23:25:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3f0c5e0d3cbdb137435819026fbefb697966a4bb54232814f98a0b7129a33b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5711941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba15d624714561e7c7b3dd5a6ee368b06d1e92cbc4419292c44c2e81241c81af`

```dockerfile
```

-	Layers:
	-	`sha256:3976a1a5e32d1e698502a62489a7591b53290b1f2a5b40a1d275599135a45c2d`  
		Last Modified: Tue, 19 May 2026 23:25:01 GMT  
		Size: 5.7 MB (5658131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c98e84189a7dd6946b04048c6df903e998d95b52f13e6b602333cb0cf6bfb50`  
		Last Modified: Tue, 19 May 2026 23:25:01 GMT  
		Size: 53.8 KB (53810 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:27b1c4974fb610791c654042245ac0ec2badf9244c76ce2c5b5440f13f0e6bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170330968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed35862b492d84f279e5aed82c196fb443b86de7e97e6fdab7426b46ecda9dae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:52:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 20 May 2026 00:52:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:52:47 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 00:52:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 00:52:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 20 May 2026 00:52:57 GMT
ENV LANG=en_US.utf8
# Wed, 20 May 2026 00:53:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:53:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 00:53:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 20 May 2026 00:53:06 GMT
ENV PG_MAJOR=15
# Wed, 20 May 2026 00:53:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 20 May 2026 00:53:06 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Wed, 20 May 2026 01:00:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 01:00:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 01:00:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 01:00:10 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 01:00:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 01:00:10 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 01:00:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 01:00:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 01:00:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 01:00:11 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 01:00:11 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 01:00:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058b47d60c3c36623902dd53cdd673ce9b93583318e52744c4f1c8fcee2210d3`  
		Last Modified: Wed, 20 May 2026 00:54:39 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c6200d019c69189d0cef55392b9d5f243922994526471f68eb529e6cea6849`  
		Last Modified: Wed, 20 May 2026 00:54:40 GMT  
		Size: 7.1 MB (7076746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123e9dad4ecf44cd33cca69d25aa161600fedac0adfc03523b3b4dbfff65d670`  
		Last Modified: Wed, 20 May 2026 00:54:39 GMT  
		Size: 1.2 MB (1214730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62d4bbb20eaa83d2a85b1f102e15ff2cb6785ca81fdda9b6487c13403ea8879`  
		Last Modified: Wed, 20 May 2026 00:54:40 GMT  
		Size: 8.2 MB (8204050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cabd8a34059cfd4179cb9b138029133ff5ac88145fbf412d16f6df32a0ee94`  
		Last Modified: Wed, 20 May 2026 00:54:40 GMT  
		Size: 1.4 MB (1394900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addd7512ebbc0491a92f74f3bc573c6005f782856ff8fc3c078b46196125f6b8`  
		Last Modified: Wed, 20 May 2026 00:54:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecb1e0239a2c6cca5794b42475503acd64e3dc81fc4796fc6d94c839b3f5d73`  
		Last Modified: Wed, 20 May 2026 00:54:41 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6856b5efb56120385484b3621a1fe96431748669de70dd4857fa63ed42f8fd78`  
		Last Modified: Wed, 20 May 2026 01:01:01 GMT  
		Size: 118.8 MB (118819205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deef1506081accf8069da9ca8324ebe9782a846e6bd97c1dde84c10bc6808d96`  
		Last Modified: Wed, 20 May 2026 01:00:53 GMT  
		Size: 9.9 KB (9879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332e7eee702c1556b43515698690c7e8bea11e74ce7b9920d0696d7248d9b43c`  
		Last Modified: Wed, 20 May 2026 01:00:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ce58a387521bedbc52600da20a655074453b2c33e7106db3e271a09747dc9a`  
		Last Modified: Wed, 20 May 2026 01:00:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0b51bbb2c69d7f7dcfc0cf268667090fc885fe6daa25897063925e1835260a`  
		Last Modified: Wed, 20 May 2026 01:00:54 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ac8e58169d57a56fda3fae1fd3e6b79b055c0f8c87327f4d942453818fefc2`  
		Last Modified: Wed, 20 May 2026 01:00:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:67e47354496ad0466d4c04cb82ce2718526b419cde36ba460e650208bc45dba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f905093a72756fe3426ff00428d8676e2efe1dbe789ff9b24aca33413325a2`

```dockerfile
```

-	Layers:
	-	`sha256:422b474ebb880bb3714e59fa70a82948247b9e3973150a368acfd14ea073aa93`  
		Last Modified: Wed, 20 May 2026 01:00:56 GMT  
		Size: 5.6 MB (5649209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dea9cb9c7e184c8df5ec076a9fd70248f6bb48af67c56c0883b8c3c355e1925d`  
		Last Modified: Wed, 20 May 2026 01:00:54 GMT  
		Size: 53.9 KB (53930 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:55e4d812ed49b06d4d359c48a4d713e603ce67157bb25d06029621353b8da4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92644471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a1e55cc3b6c9a45c9b3d547941cc6b4f1cbf5a0cabdcd4fbd16cf4074f7c59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sun, 10 May 2026 12:21:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sun, 10 May 2026 12:22:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 May 2026 12:23:42 GMT
ENV GOSU_VERSION=1.19
# Sun, 10 May 2026 12:23:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 10 May 2026 12:24:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sun, 10 May 2026 12:24:43 GMT
ENV LANG=en_US.utf8
# Sun, 10 May 2026 12:25:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 10 May 2026 12:25:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 May 2026 12:25:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sun, 10 May 2026 12:25:26 GMT
ENV PG_MAJOR=15
# Sun, 10 May 2026 12:25:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Sun, 10 May 2026 12:25:26 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Sat, 16 May 2026 12:10:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 16 May 2026 12:10:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 16 May 2026 12:10:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 16 May 2026 12:10:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 16 May 2026 12:10:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sat, 16 May 2026 12:10:56 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 16 May 2026 12:10:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 16 May 2026 12:10:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 16 May 2026 12:10:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 May 2026 12:10:57 GMT
STOPSIGNAL SIGINT
# Sat, 16 May 2026 12:10:57 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 16 May 2026 12:10:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988dc2de045f11813ef1359f5abe174ba62914438fb92d75cab7c65a9647aed2`  
		Last Modified: Sun, 10 May 2026 14:30:04 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bf149e5f1637f24cdc4c472d6e4ca943279612e0d39c8e267125e4ebbe141c`  
		Last Modified: Sun, 10 May 2026 14:30:06 GMT  
		Size: 6.3 MB (6293378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22405ed7ddeb3ddb041a0d46f2314cf33a0b76a8a467e9c2d55a2a69b23735f5`  
		Last Modified: Sun, 10 May 2026 14:30:04 GMT  
		Size: 1.2 MB (1202046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1d93a3e38e95a376c71494a9b760c3874601da3ad347a9397e5584a2fdba3b`  
		Last Modified: Sun, 10 May 2026 14:30:08 GMT  
		Size: 8.2 MB (8203592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b5d68446e4a2a25f4140c2073abfa1f378e16bf8336f3f58606a91b20d9af9`  
		Last Modified: Sun, 10 May 2026 14:30:06 GMT  
		Size: 1.4 MB (1402374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b4166483991e8893bbf63a352298792c54bd94c781e40f75ac232b27f4550f`  
		Last Modified: Sun, 10 May 2026 14:30:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4ab377a5216f4b915710db64b9dca4fa85382b9e3963c6a789da9f27fd014d`  
		Last Modified: Sun, 10 May 2026 14:30:07 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac658e00f7a11c2a828872a0ebb46687ef8495f773e6df90c66714f41c745d44`  
		Last Modified: Sat, 16 May 2026 12:13:30 GMT  
		Size: 47.2 MB (47241949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ef84f77fbfb48f11c9b13288db6929df754e386746d49a75cc0c033e460692`  
		Last Modified: Sat, 16 May 2026 12:13:22 GMT  
		Size: 9.9 KB (9891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388bb31799e7da41b79e34d797b42eecde454cf6666a7158db8540ec89a45742`  
		Last Modified: Sat, 16 May 2026 12:13:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30a610f438246b8b4c0d3637114da37a16086374fadac0b5042e3591ffa8e95`  
		Last Modified: Sat, 16 May 2026 12:13:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633aecae93b029ac7e18ec15d06ba35545846746e2ac3c902a644feb882d44cb`  
		Last Modified: Sat, 16 May 2026 12:13:23 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502430d846ba00283dfd692a81fc9c356c7c76de2c15f5496b34a4f8569af22`  
		Last Modified: Sat, 16 May 2026 12:13:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:1f115b42b307c3af5daa22645955cb4e7b897711b352426f0084c13d18f8534a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a3bdb034bb8554fd9f6433ecb18b409c34e5364c65f47bd9d7fce61a612e0`

```dockerfile
```

-	Layers:
	-	`sha256:08be9e586759f08bfa231cb4f97f29c8f20a839870a18d48042d2fedab356d1d`  
		Last Modified: Sat, 16 May 2026 12:13:23 GMT  
		Size: 5.0 MB (5020604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfab97cd4edf090aff6140ad0060a403fef52a7e9cba9165a18865163b1902d`  
		Last Modified: Sat, 16 May 2026 12:13:21 GMT  
		Size: 53.9 KB (53924 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:97a455b4e457604f41d3a4c04fddea79500cabeb622c0798b45901765bc38c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172623116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fc003e1e53dd411580441a4bf20a334ffcb29f6fb8a5b9adb9001262e6409e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:42:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:42:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:42:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:42:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:42:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:42:39 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:42:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:42:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:42:44 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:42:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:42:44 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Wed, 20 May 2026 00:09:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 00:09:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 00:09:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 00:09:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 00:09:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 00:09:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 00:09:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:09:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 00:09:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 00:09:13 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 00:09:13 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 00:09:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b37ac29d0c70b9a47d32d43f3f12b52ceee585cfe478bccffc27f88e479a80`  
		Last Modified: Tue, 19 May 2026 23:56:26 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d89d6ac91aade27cbc6b6a2c9f186fa9986fe72cf971c739e12bbdac7fbc4e`  
		Last Modified: Tue, 19 May 2026 23:56:26 GMT  
		Size: 6.4 MB (6408690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9597242bbbd30a2cfecf7e380325cc666fae40ac87d5e7ba2c296605eb74a7`  
		Last Modified: Tue, 19 May 2026 23:56:26 GMT  
		Size: 1.2 MB (1230234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5d82aab1a9f0b2cbd54befe87199f060af315884aec08292b5a2ffcd391bd4`  
		Last Modified: Tue, 19 May 2026 23:56:26 GMT  
		Size: 8.3 MB (8258926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f71b9210e742f99feed372b8819799a0a19a7503c440230fb98bd3dc1858cac`  
		Last Modified: Tue, 19 May 2026 23:56:27 GMT  
		Size: 1.4 MB (1398206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9317aa6fea148dfafc8cd83e82d7e6004fec9ea6a2abf3a7955c1ec90de225e8`  
		Last Modified: Tue, 19 May 2026 23:56:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c471cd0f761654e57b035ca9852bb1f48213837e3bb3d2adfb8b5c36e6865923`  
		Last Modified: Tue, 19 May 2026 23:56:27 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d240189f657802d43f9e831a0c3be3dbf3e7205440285506a7171fc597733e7`  
		Last Modified: Wed, 20 May 2026 00:09:47 GMT  
		Size: 125.5 MB (125460239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c12644c73b5ada7affa9bf9dac86638998c06ad8e55ac1c474dd855a37b361`  
		Last Modified: Wed, 20 May 2026 00:09:45 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a322c9fadc013a1da9a1f2c17b45457aea850513d1cfe1dfe9acce60d55e34`  
		Last Modified: Wed, 20 May 2026 00:09:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c2cafb844ddeea25c9363a97d78ba5dbc1894db4f9f04b78d4a859a40546d`  
		Last Modified: Wed, 20 May 2026 00:09:45 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383d8ebfc1d2fbd3bf346eaf268fdce6b01b27a46f81da7e4d0b6329d28ff30a`  
		Last Modified: Wed, 20 May 2026 00:09:46 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadc6be95da5c26f8249badaad0c5a8df5db4aa77d5ed2c93f81bd6b9fba4077`  
		Last Modified: Wed, 20 May 2026 00:09:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:4194bc4ca5237f5eff7d84ba90093bdcd86201daeae2b221679cfc7c0e1a20c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2520907a5b0e3fb35d09d010c949fcb929fb83fb7a4bedf2c8c031974497dde6`

```dockerfile
```

-	Layers:
	-	`sha256:ea813fb3d46c9c944f9e122271517cde692215a1c0e0a46c4472b92fefcc3d21`  
		Last Modified: Wed, 20 May 2026 00:09:45 GMT  
		Size: 5.7 MB (5659269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c434d76a3ffce90dda86950806f3170f2e5a884fdb5b6b0eac124b117e2e8ee`  
		Last Modified: Wed, 20 May 2026 00:09:45 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json
