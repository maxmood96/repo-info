## `postgres:14-bookworm`

```console
$ docker pull postgres@sha256:1b5fe8df2017b15ee68b986bac6ed401a7f590cbf9fd14541cf829165206ed86
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
$ docker pull postgres@sha256:7c03c52450d5b8cd25bf24b6e577e1838435a67dc46d7f7f282d2eae32269842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152125127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2bfb1a161e66ce69419e7fbdfe1b56a43447313bb75970ef987f2de960a8f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=14
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=14.19-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1aef4bd82d0a32bb2d81f9b5e72820b7e354ab64740f2368251bbc0748aef6a`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed705297d1f34f957d61b8947d31723fcf04a29e40762dcfb6a4247d5459919`  
		Last Modified: Fri, 05 Sep 2025 21:46:50 GMT  
		Size: 4.5 MB (4533761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3be395f43b79626c62d8b8b89af274fc98008cd84c472fb820a0bc01d9ea9c`  
		Last Modified: Fri, 05 Sep 2025 21:46:50 GMT  
		Size: 1.4 MB (1446778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96cad11ae3aeb5b7c91a9303fd24886632bc93cd65b542c180cd7cfd362f721`  
		Last Modified: Fri, 05 Sep 2025 21:46:58 GMT  
		Size: 8.1 MB (8066237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dd11f6ec6c1da31e39d58c45a0d31d48e3c8b09ba823b317ee4d12a60235da`  
		Last Modified: Fri, 05 Sep 2025 21:46:50 GMT  
		Size: 1.2 MB (1196153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be796315476720b3aa7ab541b0033a93e6d4965f5457aeea597fca909064d1e`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caeb79ae47d65cb348dd4f3768d26f4fffb74d4501f64be7d57f7a63cb37528c`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d38d4d65a3dbb4bbb47962092e53a659e0960c1819d1bb6e243a6014625053`  
		Last Modified: Fri, 05 Sep 2025 21:47:02 GMT  
		Size: 108.6 MB (108631576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6167734bf1a1cdafcbd3eb52bd9c37a8a3ad7081e5f8643c9aa5149bb98ca32`  
		Last Modified: Fri, 05 Sep 2025 21:46:50 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dba24e95306bfdece55348c1bea31ed6ff67314f7669f2b9fed7bdae21aa7b`  
		Last Modified: Fri, 05 Sep 2025 21:46:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a458874862eaea68566ea4f264ff9b128671f391259385bdf9179c3147cbbc`  
		Last Modified: Fri, 05 Sep 2025 21:46:50 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dd1b586e9f464a274ec570a726e852765966bf952ecca8ae7d06325e8f0351`  
		Last Modified: Fri, 05 Sep 2025 21:46:50 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac3e4db1ba3721cb6d4a95058caea3a70780dff9b974a911d8726d9847ea8dc`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a8f13209afa12ccf33cd1dd6b81a71594d959c1fa2ed63532c51d010f0f826ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5926152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b46fdcf12869ca6c8c9cd253ab418f0984b05284f7de2e2a07302332d99b4ab`

```dockerfile
```

-	Layers:
	-	`sha256:6fd4ebcb3e9bda1bda32695d1e794ad89518174b79af001054e9d35f7c8d9cda`  
		Last Modified: Fri, 05 Sep 2025 23:08:38 GMT  
		Size: 5.9 MB (5872813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b6a30fd987971c96883978634dd993e0027a6c25b34d91d6196d1f6daf10ce`  
		Last Modified: Fri, 05 Sep 2025 23:08:39 GMT  
		Size: 53.3 KB (53339 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:40c47bebc01a9b0967636a35ccebf47adc1c6a783974efb6583e1d194413bb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145154245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328a415ae597b7fba17fe7522dbd7c6b82b2c810de831c9e40c59c3f7b6c28eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=14
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=14.19-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c204cc5da836181667d42643e5a4502f66f813f7294184efabbfbf26c4569`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b54f9c02ed9ab45a28d68b4bae0c1523507363d8123554705a1b388bf82205c`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 4.2 MB (4150922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7631f27c37988caea10019b4c54f1646e44302e9f512f5ca837a643884f026`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 1.4 MB (1424036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28413f77476a6d765aec2dc321d721484db0c1dae588694afae8542d1b158dd`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 8.1 MB (8066382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4efd9065887d0344f2bce2191e246ecb6130b04125d2594e3e846a02655cd12`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 1.2 MB (1194888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096980a408db4ed54eba8c0230034f3526f4a368c772547d1c5f59575185ea8c`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92a225da56a23cdeb49da5b9f9be14e5cd077b97d46cb65bef79da5887f9c5e`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec2993e82b9e724f4c77261381fb7c7908de61ee2b65ef476e40e1ffc2cbebc`  
		Last Modified: Fri, 05 Sep 2025 22:06:19 GMT  
		Size: 104.5 MB (104534923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb2d60ab9f3def635778692a98db1dd6f3f0fb0de7321c7b232849802be8568`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149c64fa347164f7e2b37620c16f8ab034506a468fe88d373ec0b350cf5ec0c3`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796c43166bc94792152a4b049441944e2687c85b6210200e04990bc20636b4e1`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c725d63be0de3ec8a9b221d9ba46ed24b1d85bea839beb9351e4e3cab818644`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdcf18bc42e0c591000ed624db8a94633f9c6d23a9259f19e0b0744eccd2f9d`  
		Last Modified: Fri, 05 Sep 2025 22:06:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:17ecd200626fe1af4bfc5d84875d43f7f8b7b747372c350aa75655628cedad8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b6840a67f134fead1bbb8823753ee99b481871da4f8a8ee332efa1955c99ec`

```dockerfile
```

-	Layers:
	-	`sha256:1a442b5f418db96eeb738be8c3a5b99e2adbd1332cbf83ed4c487ce66e4a5639`  
		Last Modified: Fri, 05 Sep 2025 23:08:46 GMT  
		Size: 5.9 MB (5888642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ca8559398a7eedcd68e59ddd42d0d4a6e697d64c2923ec14985130dab8669a`  
		Last Modified: Fri, 05 Sep 2025 23:08:47 GMT  
		Size: 53.5 KB (53546 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:0929e092efe307c1fdca0c9519a399c43aa898844a3694ac434143e61bd1772f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140195077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617cd1cfc71dc93bf5363602b148307a87767cbfc732cae6f7df89fb55651aa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19-1.pgdg12+1
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820cfb123948a92acbf96b230a0cdea26476a1d3d429aebc35cc9fc764b4a6d`  
		Last Modified: Tue, 12 Aug 2025 22:38:54 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3b99820b8a61186a81204f61ee925a3f4266ace75a824b4ebff77980b261a8`  
		Last Modified: Tue, 12 Aug 2025 22:38:55 GMT  
		Size: 3.7 MB (3742574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba3f5dbe870838e10b49748bc06c909eaeb5ce71d28f86afbb30fb50686f3d`  
		Last Modified: Tue, 12 Aug 2025 22:38:55 GMT  
		Size: 1.4 MB (1413752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991df6523048151c47c162c5ac7ecfc88bf25eeb426a1400cf0194426f20313`  
		Last Modified: Tue, 12 Aug 2025 22:38:56 GMT  
		Size: 8.1 MB (8066369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201deac0b306fa58e8dd8ac5df3e46479efee68548ea761125fc205f19c46d4a`  
		Last Modified: Tue, 12 Aug 2025 22:38:55 GMT  
		Size: 1.1 MB (1067038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8763abcb4c6fe6a574c1314ae0ac66ef89c57408280beea34653c3d252f5ae54`  
		Last Modified: Tue, 12 Aug 2025 22:38:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c55d99fc111b0443e24a20c7eaa4578a66b6eb57754d56f6704f35122015a32`  
		Last Modified: Tue, 12 Aug 2025 22:38:56 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872644eefd5b9703f073fba95908c7a03a4de3b15de7ba37c55195e48ef2446b`  
		Last Modified: Thu, 14 Aug 2025 21:05:58 GMT  
		Size: 101.9 MB (101946058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5289eff35247967ec0dea759db7ed864c08ac5387834f1527452c7cc267c5ed6`  
		Last Modified: Thu, 14 Aug 2025 21:05:52 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffcdf1c5b70edcbe1c3f62983b6e9072f1e9d3a3942c4524338b41c8a14e0df`  
		Last Modified: Thu, 14 Aug 2025 21:05:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dfecd275762ad3fc9acfd99ca9f7683d7bd441153eee90120e32680ecb6d88`  
		Last Modified: Thu, 14 Aug 2025 21:05:54 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7010afb416dec175b88b071eed60dda88bacbbf7b49e4cb730a5718ee9f7cd01`  
		Last Modified: Thu, 14 Aug 2025 21:05:54 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cc0b4641b050aedde500e9e046712c36b3a8d84a193ee9372ab0506d685125`  
		Last Modified: Thu, 14 Aug 2025 21:05:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b004843cd14386475dc62a39c3c6bf4ffc1e901474a012ced4e881544f13404b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5941448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b1f1b6cc6b67840e3d3b53db914c4029fb075cc189d96f22c89345b4461751`

```dockerfile
```

-	Layers:
	-	`sha256:68bfb0a3bad1ac724b5373d0a8cc0154ada8536e0e564210fe96d300c974b400`  
		Last Modified: Thu, 14 Aug 2025 23:09:50 GMT  
		Size: 5.9 MB (5887905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d569e9f18be20981d05c7cde08d1e947252a18fa083348c52b822d6ce63e205`  
		Last Modified: Thu, 14 Aug 2025 23:09:51 GMT  
		Size: 53.5 KB (53543 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6325b389bd9c0be4b8e2d6897b5d387d91b79a6a2f2361e65a47b5deab19c3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150058049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:777bc3b5f5318dfdfcd3a63692de83af2bcfc9483ae6966e1216b0c1833c72aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19-1.pgdg12+1
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f22bf4a69c67725a5d28659467a9f4119ed414adf8a1d433e11ad80206e7a29`  
		Last Modified: Thu, 14 Aug 2025 18:51:34 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ee65475462ea3e8ee78a207e0ee11b503288d0fc59ca7e79ac316ec6acc04`  
		Last Modified: Thu, 14 Aug 2025 18:51:36 GMT  
		Size: 4.5 MB (4499189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d686f5a8767e8f7119f4019c78e95b41922a788f6adf346700ad86916e3f0d47`  
		Last Modified: Thu, 14 Aug 2025 18:51:36 GMT  
		Size: 1.4 MB (1378836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c4da94471816abaff082b723798940778c0d6e9ba39ca35822ae23757628b1`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 8.1 MB (8066342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dd948fe7b916f24497e0aa4ac3ea5f654f2ec18fecaf144b35e44757fcc0f5`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 1.1 MB (1108732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9e7f843ae66f3ff0fb7f0e9b43b16750e2dff4f3d8bb23e783ba6c4e9faa04`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb81ba96e939b60e2849bd3e78c77085a5b656b0da6722c19eec786712cb1a7`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e576745378bbdce85527927a7e810fbaa38df202cb79d6ca3c2b12319b684b0`  
		Last Modified: Thu, 14 Aug 2025 19:22:04 GMT  
		Size: 106.9 MB (106902590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f0bb56a014518babaddccffeb75d227ca1885b94b145349aa0522c8ed1bcab`  
		Last Modified: Thu, 14 Aug 2025 19:21:48 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17a652536aeb19f6a15869d631619f21921aed84364c00c2dfce6ea7607779`  
		Last Modified: Thu, 14 Aug 2025 19:21:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3acd6aa4ffe88d775e6754decf6364318410735341a2369216af34de785075`  
		Last Modified: Thu, 14 Aug 2025 19:21:49 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc824cd6834d7807304b9e202261e9518738d76a4d736b5144dd20a35589f453`  
		Last Modified: Thu, 14 Aug 2025 19:21:49 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f426dc1f32e1af20f1aeac3f74cb9d1c56179d3d03f3ccea96b891a3ad327208`  
		Last Modified: Thu, 14 Aug 2025 19:21:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5106f59b14041641fa133c97ab03b9e9f16e3188b91c50bbbb3507286ef22b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5932713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2867b3d2ea165ed5292a6bd805cfe1a9dcf43b4877afa961a13f66e03282241`

```dockerfile
```

-	Layers:
	-	`sha256:865a149b08c0ecd6d846921905e4e29f82794ec2601b86c9eebb8f320de9ac12`  
		Last Modified: Thu, 14 Aug 2025 20:10:15 GMT  
		Size: 5.9 MB (5879128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc062d354e37ce903787ee6da067feab7bcc90be9b3b24c4d1ec760e6c5e93f`  
		Last Modified: Thu, 14 Aug 2025 20:10:16 GMT  
		Size: 53.6 KB (53585 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:7ec90d15db257e90ad6bdb8a77b917cea3420a02e99a838bbec0024877081535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160867486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add12ac9c36d6540e417216295cdf77081e9b1af01336d854811c3daa56a4058`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=14
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=14.19-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1352279344c6078b55aaeeda1957e9972504efec3666c541c6889fe23672f`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aace6ac83a617b023b27f20537e4ecc7637885915979c59f31c5681723ae53df`  
		Last Modified: Fri, 05 Sep 2025 21:58:46 GMT  
		Size: 5.0 MB (4965089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20cb8e89fecb1957a33a5e82da95d50c5865163ca8b6a598b7191929343a298`  
		Last Modified: Fri, 05 Sep 2025 21:58:49 GMT  
		Size: 1.4 MB (1422306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338d8b42c11097be7ce70d09a65165fc2112d6d84b5f763d7751b8ea65f47cbf`  
		Last Modified: Fri, 05 Sep 2025 21:58:50 GMT  
		Size: 8.1 MB (8066259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897208314eb47a49a669ae64ffbe38aefb78118c66692da2fb42a718efa226ba`  
		Last Modified: Fri, 05 Sep 2025 21:58:49 GMT  
		Size: 1.1 MB (1137186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812f8629a6fe23067feeb54a98a609e673f5e7959c810c0daa374c03c47a0c6d`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1283fef8f5181472e2fcf0e9aacb9ca0fa5ce4f20aceea89151dd037605c7e8`  
		Last Modified: Fri, 05 Sep 2025 21:58:49 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585b18ea9179d37bef48c06261e270c431e8cca3e521a7903730f62c66cfc62b`  
		Last Modified: Fri, 05 Sep 2025 23:59:21 GMT  
		Size: 116.0 MB (116043671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b81f28784165714f5c988adc80447e97a70ccb79dde5acbb911266095b5dc7`  
		Last Modified: Fri, 05 Sep 2025 21:58:49 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e3905262c81846433bcf3665c442ce675a310fa29330c6c36c89b905a9483e`  
		Last Modified: Fri, 05 Sep 2025 21:58:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12201a4e784f1e0995fe0abe3d399a1d3ba1183d93d001d18cb9120487722dc2`  
		Last Modified: Fri, 05 Sep 2025 21:58:50 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93aa2e3caedcc70c635da12509deb43cafe75642d246b0eb3e74d1b1eb3c3711`  
		Last Modified: Fri, 05 Sep 2025 21:58:50 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b27cdabb7fc1dc76f0ff65eb14d1197d6de5af90086c4a838d7df61fbe7b36`  
		Last Modified: Fri, 05 Sep 2025 21:58:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:930d62e48d2430f78490bbb471f0448d9143111a577fed478b76efaffbf6996c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5940068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20f324b0d617de97a7fc18212fd6335b5776de6ff58e7e89a6b5c5a2c8f211e`

```dockerfile
```

-	Layers:
	-	`sha256:f210b350eb412026d838912e89aab31ff037e6a329eaa792e54983137e101489`  
		Last Modified: Fri, 05 Sep 2025 23:09:03 GMT  
		Size: 5.9 MB (5886773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04f7417f733d3933175d47f74251be7091ddc1df8f10571cd4c99e4952ca4a5`  
		Last Modified: Fri, 05 Sep 2025 23:09:04 GMT  
		Size: 53.3 KB (53295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:625d20907aa355e0ab0bb28be5944e172134bacdbc07d499e3f1f162f2e32388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150947206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6af3d611dd761e30a0b284a39198fa4cd2618e161a691125e0a773d5ec96299`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19-1.pgdg12+1
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83bd2d8e15bdca1c657f4e1229c9515648aa638816bf4ae6a4be5a7afaee3a81`  
		Last Modified: Tue, 12 Aug 2025 20:45:57 GMT  
		Size: 28.5 MB (28516923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29312da7268b11c0e420282a3de73777dd60323a6115c94e4770a3967d1008dd`  
		Last Modified: Thu, 14 Aug 2025 19:34:18 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadf75f6a42f2ec57e669503e79a92f31752f394516ac3907e5fb7ad2261db38`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 4.5 MB (4475161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edb5cc62fc658d056d649cb284f0a020e6a6c0b57162be2680462937f71ab57`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 1.3 MB (1333909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474838f47aaa89f71355146b0a39b988275244759ef97d0cf6e616a991c9027f`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 8.1 MB (8066502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e17ad67a5ccc4d969ff6abab8130942de3726b9e6fad6051c12601f1f8343`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 1.2 MB (1182641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31de7c74bad6aba9b4e3ba53d1a4cfc29234f0d874650d8b3ecb0e3678aa8c07`  
		Last Modified: Thu, 14 Aug 2025 19:34:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cba190353263630bff7d7d1f8db3bf41c59f3df3ef093a60839ff9e4950b3`  
		Last Modified: Thu, 14 Aug 2025 19:34:21 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84159e5038f9e931ba6b0a3ae04097183f6b549f18ff4758d2f1f85f300752b0`  
		Last Modified: Fri, 15 Aug 2025 00:10:37 GMT  
		Size: 107.4 MB (107351698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76aa19e05d837486e5d3cd563389785d9533e4efbc7b6d383a8f2bc20c014e67`  
		Last Modified: Fri, 15 Aug 2025 00:10:27 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca59bb88b6d7bbfa1eae5df680d4f485bf762dc859ca307588566217903fed98`  
		Last Modified: Fri, 15 Aug 2025 00:10:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1c41037ae2bb21df5971d4fbe1ad718a3d8ed92a231b144f8c0569611d70c0`  
		Last Modified: Fri, 15 Aug 2025 00:10:27 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f3ba64453b44a4f9ab12958df85db463e2e414d3ef7ab7ad3f1cf2eea46195`  
		Last Modified: Fri, 15 Aug 2025 00:10:27 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fb64357a2898876e82b21a615cf28e3e432ccd9a3aae203fa1002d5f6ae694`  
		Last Modified: Fri, 15 Aug 2025 00:10:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4b27f9d3ccabef06abcf247f9a6b81426cd9c4efd6b9a6ab921b5be23d9da643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264e57e7190ffafa23f80f8ca68be9b80cc3fe63c4342a2800eb36c5fd9f4171`

```dockerfile
```

-	Layers:
	-	`sha256:437ecdac260011402aac1ea6b7e6cfbc52668d9ead4358f62ff91cdb360ff19e`  
		Last Modified: Fri, 15 Aug 2025 02:08:26 GMT  
		Size: 53.2 KB (53206 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:824a4cd77a9200bf274ee83c0e49d22e7ac32f458235649b2bf7a1c7dd59d573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164752590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfa60ef5c4c6cd0ccc2a700623f3283b492a9dc7137cf1d5bf24cfe6ee74570`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19-1.pgdg12+1
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e71427bc966f27e4c045f76677200cc1cb8d57b75ba0d7ab977498c00e8d6a4`  
		Last Modified: Wed, 13 Aug 2025 11:23:54 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c88c8558d33d220ba0bd06a9aaa623bae8d2dc5226d907b7bea0495002b0d32`  
		Last Modified: Wed, 13 Aug 2025 15:35:10 GMT  
		Size: 5.4 MB (5368151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4541684e1bb8d6caaca0ac9f5d0cf566b2ef5226a534bd35fb5967ecbf66d244`  
		Last Modified: Wed, 13 Aug 2025 11:23:59 GMT  
		Size: 1.4 MB (1368729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f3c9c3e96a7afe0384ff2776211efbadf170ac27ffbd881765dd2568bbe5de`  
		Last Modified: Wed, 13 Aug 2025 15:35:11 GMT  
		Size: 8.1 MB (8066366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5ac7820ef53cc6fce6e86c3e89e9180a62df051f52f4f05f567ba757da2dd9`  
		Last Modified: Wed, 13 Aug 2025 11:24:05 GMT  
		Size: 1.3 MB (1283505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b039814790880fa88c0fe02fdcfc7406c540d2eeccdf1c8012cf811171ba3348`  
		Last Modified: Wed, 13 Aug 2025 12:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05bb5a6b03e6da586b1e62ffbc88e07fc494b048054316cdb970e7f6adacb5`  
		Last Modified: Wed, 13 Aug 2025 11:24:14 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11584be60dc749e6b9285d82c3f9613cdec125601cc8cd2444e83bcccd0712d4`  
		Last Modified: Thu, 14 Aug 2025 19:48:00 GMT  
		Size: 116.6 MB (116572052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b179b45e9050fdf0ade4fcc052994c73f3b638da3a5000a31a1690653fbb13d`  
		Last Modified: Thu, 14 Aug 2025 19:47:53 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08acb8ed33a81d009f8da3d234665026ea8a5fc0dac4839337d90ff0941e14d4`  
		Last Modified: Thu, 14 Aug 2025 19:47:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda2a4af0cd5fd1fadc0f6ef7b1dc78e205163c05c6fad90296353155f3757ba`  
		Last Modified: Thu, 14 Aug 2025 19:47:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedeee7e84a924b4d156fd08d11ab4ec495294d610d0674fb7f96bd9422b4745`  
		Last Modified: Thu, 14 Aug 2025 19:47:53 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fba9c2759d5df6bd9f7e9274a7607bc5a2bd9ffc6d70e6535cdff448d5031f4`  
		Last Modified: Thu, 14 Aug 2025 19:47:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:00a41c336886119af516bbf7173bc8652263821fe4e4b2301e1b4e7a6f3c7819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5933587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2248733eedc4a1d2e00ab0fcd670948d2ee49bda8d8df1d19c0a4b59eea65f46`

```dockerfile
```

-	Layers:
	-	`sha256:6ea0d1e79891ec072d3abdc1643853741fd0ce8b8db2b3826f1658d491816116`  
		Last Modified: Thu, 14 Aug 2025 20:10:28 GMT  
		Size: 5.9 MB (5880194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff83a7e3d930e06db19dc660e89ccc30e21266c28591c9276753355baa7342c`  
		Last Modified: Thu, 14 Aug 2025 20:10:29 GMT  
		Size: 53.4 KB (53393 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:46c2b049858f1565e7e7fa020c22bea716e93dc46dd29679c0d9531795ec1075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161304434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280895a45774a11b2047845c9a2d78a5857fb24aaeb2bc00caee035ba920830b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_MAJOR=14
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PG_VERSION=14.19-1.pgdg12+1
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:25:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:25:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:25:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:25:20 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:25:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:25:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6c30648f10140423dedad94d980ec43d531a9cad0983059ff739bb9b52a33f`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ac9590e0ed955da24f366c054364cf8ba0c10685c2a11926f9130d96dd2ef`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 4.4 MB (4391026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610383596c1fcdd9ad52eec420a313e89a0b3b8e9b9eec4a9c97875fa3199e0d`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 1.4 MB (1412789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968418c0a002c3f87fa669b14de23f59d9a339200e3b6e12866ab5eaefe04843`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 8.1 MB (8120490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c87bf03e6298d0eda03dad7a991ef95e36418ce316b1cab732a6c5aaf20b9c`  
		Last Modified: Wed, 13 Aug 2025 11:43:35 GMT  
		Size: 1.1 MB (1096806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e80fccf7e254e617a490a5e480bf0a7d998d006d09d137c184187e9db82e9c`  
		Last Modified: Wed, 13 Aug 2025 11:43:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0382bed70396ec99ad734fded83f746496510f544ac4570bbc14cf5ca09f924`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf681e2e2cc2dc9b6b5acaeb0ecde0f31ab18bbb531039fd5bc8dff36755c061`  
		Last Modified: Thu, 14 Aug 2025 22:21:45 GMT  
		Size: 119.4 MB (119375127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed463a05158d3629eab4522f4eeffcc8a400cd137b65b2a1195b859bd0497727`  
		Last Modified: Thu, 14 Aug 2025 22:21:34 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4449c291a11b0ae847e09b1b91946b8faaf332b3ae2db248f9d41514f1094d`  
		Last Modified: Thu, 14 Aug 2025 22:21:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a8fc126fa40493dba5e4161b8b9050f9a0954650362569a8535b6200d3ce80`  
		Last Modified: Thu, 14 Aug 2025 22:21:34 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ab457156ac7a54dc5a2aa620596353fa1a042da8df4321c1f8d16dd8ace27d`  
		Last Modified: Thu, 14 Aug 2025 22:21:34 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad58bab883d91799d147db58aee99c3a78ba99b185c2218880c34cd931abab9f`  
		Last Modified: Thu, 14 Aug 2025 22:21:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:50047282ca85cfde22366ba8618956ae5c0c80563d2e436849e62d0ec455c993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a292545dedb2281e14d90f5cdc13caa2a8a1bd6ce18e5f6d922a303b9042dbc`

```dockerfile
```

-	Layers:
	-	`sha256:34822136069c1a5fbe315c4e81271bd12e551bc317de5e28eee914049f5a71be`  
		Last Modified: Thu, 14 Aug 2025 23:10:08 GMT  
		Size: 5.9 MB (5883253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2092cb4c945845343a7ab2251e66e7bdb285fc96111a6157b0c670c3306f8cf2`  
		Last Modified: Thu, 14 Aug 2025 23:10:09 GMT  
		Size: 53.3 KB (53340 bytes)  
		MIME: application/vnd.in-toto+json
