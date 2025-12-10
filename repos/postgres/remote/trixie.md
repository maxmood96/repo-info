## `postgres:trixie`

```console
$ docker pull postgres@sha256:38d5c9d522037d8bf0864c9068e4df2f8a60127c6489ab06f98fdeda535560f9
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

### `postgres:trixie` - linux; amd64

```console
$ docker pull postgres@sha256:1f822adace8140adb2b217f843777a075c88661e97bc73592f0f7fcc9c779442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.2 MB (162204356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5caf683a8bb369ea3f8aee80ff184d4da0b975f403bfca4f0cb72957bdf35d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:02:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:02:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:02:28 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:02:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:02:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:02:33 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:02:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:02:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:02:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:02:37 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:02:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:02:37 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Mon, 08 Dec 2025 23:03:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:03:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:03:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:03:11 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:03:11 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:03:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:03:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:03:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:03:11 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:03:11 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:03:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab3dfaacd572bed9363ba4dcf22f792b3ee62852f65170bd00351449df6bb22`  
		Last Modified: Mon, 08 Dec 2025 23:03:42 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd6fcdc9495a48a41cd17bc7a804bdc37abeb47b3953177240af3ce23ee7046`  
		Last Modified: Mon, 08 Dec 2025 23:03:43 GMT  
		Size: 6.4 MB (6436651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b004922a6f455482d488028f0e718ff95803e76bbdf5b7006a5bab63726da46d`  
		Last Modified: Mon, 08 Dec 2025 23:03:42 GMT  
		Size: 1.3 MB (1256613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fdf866b594e6ccc864d9148c91d2d71726b39a21013f88757ab4e4a1d68d24`  
		Last Modified: Mon, 08 Dec 2025 23:03:43 GMT  
		Size: 8.2 MB (8203790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ff19dd627cd160c9bb07f3d82b59fc8c0b6a19e534303bb301be6ae5ee3512`  
		Last Modified: Mon, 08 Dec 2025 23:03:42 GMT  
		Size: 1.3 MB (1311501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854c622dacffbddfa75e9316706394884e033501d37423355bcfa617cc97ffa7`  
		Last Modified: Mon, 08 Dec 2025 23:03:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f106a4619ad3ff22ad36895bdd16ea5e3f722a095d07ca0a4c3dc573ce9e9c38`  
		Last Modified: Mon, 08 Dec 2025 23:03:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c063aa26ba0a87153bf6404bd3bb7b7ba00e9cb113b8edb1835c7fde2f7a3d82`  
		Last Modified: Mon, 08 Dec 2025 23:03:51 GMT  
		Size: 115.2 MB (115189552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a285618a7ed14009748955c43b6048cf222cbb9213400439d0383348e5e4bb5`  
		Last Modified: Mon, 08 Dec 2025 23:03:42 GMT  
		Size: 19.2 KB (19182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807997f7ba635f71bfc55943789db79fbe11521a89505131746466abcf89fb7d`  
		Last Modified: Mon, 08 Dec 2025 23:03:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e628b821ef168b7e6190b8c4d2ebe15819433421a6a54ef4c2144db69d538`  
		Last Modified: Mon, 08 Dec 2025 23:03:43 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc30afa27629728d317454a99510459a4692c080424e3fbff2a2fb736a6b14f`  
		Last Modified: Mon, 08 Dec 2025 23:03:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:1b4a9a1672bc4ba61a1ad167d7dc48ab02484ca8363cdd87083c77993c1e0041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6008930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398fedf0cf725682870aaab4cf887667bc55888d4a3406e1a1dd00ebefda8f31`

```dockerfile
```

-	Layers:
	-	`sha256:16ace5c5243a9c5c7b6506ee54e843d034df90743105a12d0fe17c93a69bd709`  
		Last Modified: Tue, 09 Dec 2025 00:10:47 GMT  
		Size: 6.0 MB (5956473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecdba68ba16c729cd4c9b28f9a87990ef9bcc866b1da9819a52135c059cdb746`  
		Last Modified: Tue, 09 Dec 2025 00:10:46 GMT  
		Size: 52.5 KB (52457 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:0a0cf95bc4e606297653695b5afe0ffc87fd5c1a58b04a02f6fb0fa463a9211d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91396854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fee9376d9743282873911c55ce7e9a4eeba7c1b03fbb5a52ea13c5d8229e6e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:23:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:23:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:23:53 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:23:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:24:02 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:24:02 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:24:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:24:09 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:24:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:24:09 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:24:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:24:09 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Mon, 08 Dec 2025 23:37:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:37:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:37:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:37:01 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:37:01 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:37:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:37:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:37:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:37:02 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:37:02 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:37:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12a9c8a020f018e0e46319b6e31c6efba95dd50d89b0f503d362a5c163fe6ef`  
		Last Modified: Mon, 08 Dec 2025 23:37:27 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bea23ea05023332ef7c93dceb15ed2528c2ce70c9f02c67a22dcd7cca646a6`  
		Last Modified: Mon, 08 Dec 2025 23:37:27 GMT  
		Size: 5.9 MB (5929035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c33016daa904894421a795cb256da859280708f00cfbf6ff8b0f4fad7d834b6`  
		Last Modified: Mon, 08 Dec 2025 23:37:26 GMT  
		Size: 1.2 MB (1227393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc83618002188a9911ef68eb8f5204c6d3625ee7280ef36098307b27bf8695e`  
		Last Modified: Mon, 08 Dec 2025 23:37:27 GMT  
		Size: 8.2 MB (8204190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c955a5cd21dd16a69d44d97f5aa10c2335a25aba0b9292864985762aea7444`  
		Last Modified: Mon, 08 Dec 2025 23:37:26 GMT  
		Size: 1.3 MB (1317172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8827bbac4812f8c1c96caf46ae69e83b18ba706c54e4dc50b8d2bcd52cf434`  
		Last Modified: Mon, 08 Dec 2025 23:37:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6fc96b11f17115a15d3591c149464fa7a9c83da75e650cda6fadca7fda3f88`  
		Last Modified: Mon, 08 Dec 2025 23:37:26 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8680a9fd053d8eb0b123736fafb283a71908a0fe5b3d41d7d634de66f8de2331`  
		Last Modified: Mon, 08 Dec 2025 23:37:31 GMT  
		Size: 46.7 MB (46745131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b833fe8f56f70aa1e9d094818afd972342148f3b902ff1aac55d95571f9159`  
		Last Modified: Mon, 08 Dec 2025 23:37:26 GMT  
		Size: 19.2 KB (19172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b656478b4bf9946f39dab564dc44732b94af08dc5f58b04c93497f38404b78a3`  
		Last Modified: Mon, 08 Dec 2025 23:37:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050a35a307bb936ecd68b929b3e1fa5b5e02966bbc09c7fb37cf7ea4a2a3bc89`  
		Last Modified: Mon, 08 Dec 2025 23:37:26 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e415805357a0e7efb9197dc1dd0dac4a859c528f73bb04060767423568f8e64e`  
		Last Modified: Mon, 08 Dec 2025 23:37:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b444c9e9314295cfa1d12be70040effc89baabbb50f4f598ca36c3cd7b729493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5172295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23055beb807d4a03c3c92928d2732989efbc1d93a476b49e409696ced836b90`

```dockerfile
```

-	Layers:
	-	`sha256:facfc9d9e09aa8f4133d7a0365cd217468ee34c46b5ca4040fd83cb4ba05e305`  
		Last Modified: Tue, 09 Dec 2025 03:12:25 GMT  
		Size: 5.1 MB (5119616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60c8909c28817efa48edc3d2612f9a39dd29aaa1140498b36ca6b93b7c3d0685`  
		Last Modified: Tue, 09 Dec 2025 03:12:26 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c37ab7422d37359805f1502aec006987a2ca4621a0df70a9183999d711966cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87718171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3755a9eb54e59b6a319504f1cb4366cd4a0cf42fdb2532fe57145399fe75c386`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:29:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:29:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:29:33 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:29:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:29:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:29:39 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:29:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:29:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:29:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:29:45 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:29:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:29:45 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Mon, 08 Dec 2025 23:42:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:42:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:42:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:42:07 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:42:07 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:42:07 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:42:07 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:42:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:42:07 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:42:07 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:42:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8384381be4dbd74f49a208f5073ae741958692fac1fe0a61dd4608865ed9c12`  
		Last Modified: Mon, 08 Dec 2025 23:42:43 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c468668f04e0b0e0084ce7fc81ed441f1791a513d3b8ef1d1613f34fd05eb6c5`  
		Last Modified: Mon, 08 Dec 2025 23:42:44 GMT  
		Size: 5.5 MB (5496835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f914533e6f77402c1845ff6191e5ff00e6fbe146970bca1506efe7784af8344`  
		Last Modified: Mon, 08 Dec 2025 23:42:43 GMT  
		Size: 1.2 MB (1222281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f990e4a3bb7c571383f45ed3c3152cecdeb25c008b22e026a1c8f3b0613170`  
		Last Modified: Mon, 08 Dec 2025 23:42:45 GMT  
		Size: 8.2 MB (8203955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478222388c2ccaed3fdd85b9509cc754218ee4fd54bcdaceb031feb19306fdcf`  
		Last Modified: Mon, 08 Dec 2025 23:42:44 GMT  
		Size: 1.2 MB (1172470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627831e51df961ab2d80d08f481c4eee345f9a123b9e4bbc6ba91049f64fe77b`  
		Last Modified: Mon, 08 Dec 2025 23:42:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce9ffa631226ee263a6916db16ad145cd44d153272bd3e841aba40e08e2f29c`  
		Last Modified: Mon, 08 Dec 2025 23:42:43 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3240dd3da96217362af656d350df742a37c0d9566bdb50d78125872000239891`  
		Last Modified: Mon, 08 Dec 2025 23:42:48 GMT  
		Size: 45.4 MB (45382842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330c37cef1c331f7f60f107c6054fb6b4e159452360d7004a9bdf53a15a70fa4`  
		Last Modified: Mon, 08 Dec 2025 23:42:43 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbcb5a5d0dd46e4d7ffa315105e79b105ed0b993d8ff3a4dbae025271a04b04`  
		Last Modified: Mon, 08 Dec 2025 23:42:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01a70347c09c27747fd4275492de7050fe2cb47504d17df8c2f890aac3696f9`  
		Last Modified: Mon, 08 Dec 2025 23:42:43 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350e983efd3dfdc656a308af269c482f575db09011ee22665f087b2e3c6147c7`  
		Last Modified: Mon, 08 Dec 2025 23:42:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:eaf343e527f71568ac3fbe386b40e558f7ba5ff5b76c252b0af07c2893a049e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5171600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddeb1bc91565fdf95cbbd9696536fb42756288283c4956502157fbe2c22b66f`

```dockerfile
```

-	Layers:
	-	`sha256:0a03840d0c917be863ffdac409bb4ea31a1d1b483c6ba3771a43776613adfc05`  
		Last Modified: Tue, 09 Dec 2025 03:12:32 GMT  
		Size: 5.1 MB (5118921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa97ed0fcb41db775558cfc28859470aa3151319118724ce786f0479bd4bd00`  
		Last Modified: Tue, 09 Dec 2025 03:12:33 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b3fb246181422c5eab3e5206514c8247e933b75a2216bd91f4d4c22bec981f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160813484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea2be1a63386598797b669c4a754e91ed8d3192324327ecc90724a097b59e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:05:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:05:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:32 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:05:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:05:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:05:37 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:05:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:05:41 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:05:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:05:42 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:05:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:05:42 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Mon, 08 Dec 2025 23:05:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:05:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:05:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:05:59 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:05:59 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:05:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:05:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:05:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:05:59 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:05:59 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:05:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5f40a380634133dae33caf44e9c609ccf5e3d91e0312f98a757b0e73fca41b`  
		Last Modified: Mon, 08 Dec 2025 23:06:30 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e40a57e2e21143c19f79967de7957aa209fbc008238290cf82904d63ca906b6`  
		Last Modified: Mon, 08 Dec 2025 23:06:30 GMT  
		Size: 6.2 MB (6232093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a343def39f69fe3ac58b6e2740c350e746c147c1e193b385aefca4faef2aee`  
		Last Modified: Mon, 08 Dec 2025 23:06:30 GMT  
		Size: 1.2 MB (1209472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1d2e88aba6d09e73bad7ba53e5488b56f055b40fc575763a29120ae63b854b`  
		Last Modified: Mon, 08 Dec 2025 23:06:31 GMT  
		Size: 8.2 MB (8203932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e3fdde08bb890bf71b9d729e29da13114093f25d67ca0a414031b36b3259de`  
		Last Modified: Mon, 08 Dec 2025 23:06:30 GMT  
		Size: 1.2 MB (1220475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbae34e361862bd027155674f8be808c17cefc31b52486a3f2885b9d7ab62d2`  
		Last Modified: Mon, 08 Dec 2025 23:06:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dc7a9c9c2333ca3dde8635bc1f1453eab10686a5b6913e307c2bd32ef83979`  
		Last Modified: Mon, 08 Dec 2025 23:06:30 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815699e3d986698e9ff3469f27ffec59b0881e734e94fe1a29eb59b53e1722f6`  
		Last Modified: Mon, 08 Dec 2025 23:06:39 GMT  
		Size: 113.8 MB (113779127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cdec9b84ac6773d81096f61e26e2a41058e4a217909a742004c74caa53a5ba`  
		Last Modified: Mon, 08 Dec 2025 23:06:30 GMT  
		Size: 19.2 KB (19185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f53bf850cb2291496f0f29c460ebb645dfb00c52a1345c2222c69383fe851a`  
		Last Modified: Mon, 08 Dec 2025 23:06:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d9e0d9c17a32dfe46dea540e1cb529d1a54c52734a0b3d669e3795025916b0`  
		Last Modified: Mon, 08 Dec 2025 23:06:29 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86b8c8487b73cd00dff6ac78811cb97ee9e5ba18842f42b3a718e708d7d18aa`  
		Last Modified: Mon, 08 Dec 2025 23:06:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:8e490fc629e891dbe44a15100f658c5b4e0c6bd9008a28ec2051b14d94bda9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4106f3525612a1d6c23cb7e47331ee8c81f463402c71355a8cea75ba874a8200`

```dockerfile
```

-	Layers:
	-	`sha256:749f2f909262557e6f5bb6e39d352553eb61375284b8c04429a91f6226e46367`  
		Last Modified: Tue, 09 Dec 2025 00:11:01 GMT  
		Size: 6.0 MB (5962846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:515817144d43fb449179fa001d106fe4582da7f180a8a647986eedc10d2dc0e5`  
		Last Modified: Tue, 09 Dec 2025 00:11:02 GMT  
		Size: 52.7 KB (52736 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; 386

```console
$ docker pull postgres@sha256:c84595a367a3fe5a4d9dce011490da38c462190e6ac7afb7d2a4c49436c80656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97511610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c04e3cccf37b123eda503f22d795820fc033cc633c7ea855b721da7c183f77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:00:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:00:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:00:48 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:00:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:00:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:00:54 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:00:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:00:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:00:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:00:58 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:00:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:00:58 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Mon, 08 Dec 2025 23:10:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:10:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:10:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:10:31 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:10:31 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:10:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:10:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:10:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:10:31 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:10:31 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:10:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bd4d2cc3f1d94e986238e00a022e87d097e339dcfe7219aa57ff0d1447f9d0`  
		Last Modified: Mon, 08 Dec 2025 23:10:52 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f4761500ded88636b1abddd7aa1e80fee6cb340b90849f4bf35c20c6f9a63`  
		Last Modified: Mon, 08 Dec 2025 23:10:53 GMT  
		Size: 6.6 MB (6629616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca927154d3f98868aa7473f12096304e5b1c1bffdd16d30a84a89837a09f0b16`  
		Last Modified: Mon, 08 Dec 2025 23:10:52 GMT  
		Size: 1.2 MB (1225707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f7c391bc9b7c705800612fef985cf2a7f5b9b50d1d82daef18ae42d65d491d`  
		Last Modified: Mon, 08 Dec 2025 23:10:54 GMT  
		Size: 8.2 MB (8203987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3161f0ecc3f84b9800a16d1d308b0ecb6a271b8ddc52787a27659478162bed45`  
		Last Modified: Mon, 08 Dec 2025 23:10:53 GMT  
		Size: 1.3 MB (1308159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2fac7adfeb94bb36364d3dd49314ddb209f56214fe0679c9af30e0c5e0d902`  
		Last Modified: Mon, 08 Dec 2025 23:10:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5acb73154771cfb607b114fc9e79c78cf19760ed1f694b68a9dc078658b5609`  
		Last Modified: Mon, 08 Dec 2025 23:10:52 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49bb5ed391da46d1f7beed00bf1e5536cbceb92e612f99b7378b9a52a465d63`  
		Last Modified: Mon, 08 Dec 2025 23:10:55 GMT  
		Size: 48.8 MB (48821317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc321425472dcfce3797fb94a727202a9e8110cc8987d151c788b3ea09045bfc`  
		Last Modified: Mon, 08 Dec 2025 23:10:52 GMT  
		Size: 19.2 KB (19181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c437fdcb761074797b5f09bbaca31662d26f101ce1152e0a9894cd2ad561d4df`  
		Last Modified: Mon, 08 Dec 2025 23:10:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a4ebf88ac2f750b44f2b4d71b4330e6dbe37e67bc1c7d592b02dad1ae9bab0`  
		Last Modified: Mon, 08 Dec 2025 23:10:53 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1082e8b811ada0204860b24687dee8ded5ba53bf2d5a77ae3a67a1abfcd69e9a`  
		Last Modified: Mon, 08 Dec 2025 23:10:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:016af73cccfaf9e7740432a857b09e7cb8a5ccd4ffb53c1167498d26398ef2cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e613b3463ddf27c8daee4aafebdf5a795c924382bcd6a06f29f8ece75e1d48`

```dockerfile
```

-	Layers:
	-	`sha256:f376719af34a2991598c86bc52fec8c50394963199f511e8b200736e82e9d965`  
		Last Modified: Tue, 09 Dec 2025 03:12:42 GMT  
		Size: 5.1 MB (5114949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a8a3073bd54e0fc531bffc330c4e92ae7b0e394c6c3efa75d6c81ccd6c88e4`  
		Last Modified: Tue, 09 Dec 2025 03:12:43 GMT  
		Size: 52.4 KB (52391 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:f8584b9ffd9073a79868641e73db452c3f08adec775dbd7982713ddeb6babca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35c8f97e14a8b530d2cc9efd784a160850d49e3208ec70e7f4f4dc09ae0b0f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:58:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 09 Dec 2025 01:58:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:58:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 09 Dec 2025 01:58:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 09 Dec 2025 01:59:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 09 Dec 2025 01:59:09 GMT
ENV LANG=en_US.utf8
# Tue, 09 Dec 2025 01:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:59:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 09 Dec 2025 01:59:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 09 Dec 2025 01:59:18 GMT
ENV PG_MAJOR=18
# Tue, 09 Dec 2025 01:59:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 09 Dec 2025 01:59:18 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Tue, 09 Dec 2025 02:00:04 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 09 Dec 2025 02:00:04 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 09 Dec 2025 02:00:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 09 Dec 2025 02:00:05 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 09 Dec 2025 02:00:05 GMT
VOLUME [/var/lib/postgresql]
# Tue, 09 Dec 2025 02:00:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 09 Dec 2025 02:00:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 09 Dec 2025 02:00:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Dec 2025 02:00:05 GMT
STOPSIGNAL SIGINT
# Tue, 09 Dec 2025 02:00:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 09 Dec 2025 02:00:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e1e14f4d7b041df9ac5fc8de0576537ea278840427d10e9148c696adb70b27`  
		Last Modified: Tue, 09 Dec 2025 02:01:24 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3745b8a53abf95c5c0de5c32dfcb3b3374ddf07ef91fc46c33e5a7e1f1067d0`  
		Last Modified: Tue, 09 Dec 2025 02:01:24 GMT  
		Size: 7.1 MB (7075970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce494898a07197b6881a493ab77d6aff68197d81a66bc208117b16f056aa1f9`  
		Last Modified: Tue, 09 Dec 2025 02:01:25 GMT  
		Size: 1.2 MB (1214722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1cb5cce5854f2b159fd846f364b0dae1a7331a6356d92a487d5c5a537f77b9`  
		Last Modified: Tue, 09 Dec 2025 02:01:24 GMT  
		Size: 8.2 MB (8203970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c04d390fdc287bfc38e367f6ac75664b0147a2e4bff0ec697269892c4c096b4`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 1.4 MB (1394831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe9c5eb03727d2f38c3eb284ce3f107244d3441c38b3c9186ff8d0f4b13e481`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec249543bac7d8464c12595e55a8805f97a5535503ed82d2633b4a943e1b120d`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075032cccfb790c0ed082f126c84442ca74c5bdc4d202e4036df942ffe15d96d`  
		Last Modified: Tue, 09 Dec 2025 02:01:36 GMT  
		Size: 123.1 MB (123110309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff91dbdc7544ae997d64f517a27dff2a67763b8b1047046c32d30c272c3f8e2`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 19.2 KB (19183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b8ee199ace51032e6f7c7063473a3ea2b34d5dfd8a6beae9484ec066c53ad4`  
		Last Modified: Tue, 09 Dec 2025 02:01:24 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c484f2ae57398b17c97a8fe07a090e265dd273f3b40062f0fd0d8b4015025eee`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b024872ad16c6e21d98694f2a61c7648c94ca84ee9dd56b5aad86819870519`  
		Last Modified: Tue, 09 Dec 2025 02:01:23 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:41da20ded011f79e3e673f71eda09761e553fc45de2e804ac1f3d04d46729214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6015655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ea2c6fe694ad48701e955f4875c009eb368944fdeea1a9428bc8faa4943f33`

```dockerfile
```

-	Layers:
	-	`sha256:bbb1203f78e591343d6e470f5a27b7e03c5e6f35d6dcb7948d3079186cf34795`  
		Last Modified: Tue, 09 Dec 2025 03:12:49 GMT  
		Size: 6.0 MB (5963121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec1955218b1297b16272a16fadd0c155eaa35848695c0a2d076387449ec08f2`  
		Last Modified: Tue, 09 Dec 2025 03:12:50 GMT  
		Size: 52.5 KB (52534 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:c670f6c3df8365e80ad2072cfb2ca2dfbf74035fe35bfa4c2838c698adf13dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92795659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9227c47011c9b6dad8b163b6eb62d450c61eebe11fceaaa7d2dcd61f884844`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Wed, 10 Dec 2025 13:55:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 10 Dec 2025 13:56:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Dec 2025 13:56:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 10 Dec 2025 13:56:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 10 Dec 2025 13:57:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 10 Dec 2025 13:57:58 GMT
ENV LANG=en_US.utf8
# Wed, 10 Dec 2025 13:58:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Dec 2025 13:58:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 10 Dec 2025 13:58:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 10 Dec 2025 13:58:38 GMT
ENV PG_MAJOR=18
# Wed, 10 Dec 2025 13:58:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 10 Dec 2025 13:58:38 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Wed, 10 Dec 2025 16:00:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 10 Dec 2025 16:00:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 10 Dec 2025 16:00:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 10 Dec 2025 16:00:58 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 10 Dec 2025 16:00:58 GMT
VOLUME [/var/lib/postgresql]
# Wed, 10 Dec 2025 16:00:59 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 10 Dec 2025 16:00:59 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 10 Dec 2025 16:00:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Dec 2025 16:00:59 GMT
STOPSIGNAL SIGINT
# Wed, 10 Dec 2025 16:00:59 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 10 Dec 2025 16:00:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7509a6e61e937d2861e580aee3645ccc284662e5ff785c3a9eb5fea93cf517b`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd637312070c560044a9b139cf8983fb8e39b5f60b3c51a2c557980815f7101`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 6.3 MB (6291355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7b1b0d8d9bb5d10b5a2d66ecee216d2f1cae8a593baa99e14a05f9eed3afbb`  
		Last Modified: Wed, 10 Dec 2025 16:03:48 GMT  
		Size: 1.2 MB (1201916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cfccc2a828efdeee76cdfc0241a7a2253c5d5e7ec9c2770454a9f217a9c55a`  
		Last Modified: Wed, 10 Dec 2025 16:03:48 GMT  
		Size: 8.2 MB (8203580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87922f2a83f8c445248a001ee77716a207d176d413c183b77f66b22eb3c3aae`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 1.4 MB (1402222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f877525412689d6256ebb5cd6dd6649d1f971ed1a240aa789cd7554715346e`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4086fc5e0163b1fdce9acbb9093daa90b18ab170c9c52c4e31bea0af44599c`  
		Last Modified: Wed, 10 Dec 2025 16:03:47 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc73849f46f79031f7e13e8247d53ba7efcc7cc590521c0883268a48db981422`  
		Last Modified: Wed, 10 Dec 2025 16:03:56 GMT  
		Size: 47.4 MB (47393664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798f297133c5908c6d3c04ce62e26d7dffaa990a3c2fa06f09fe87a042512ddd`  
		Last Modified: Wed, 10 Dec 2025 16:03:48 GMT  
		Size: 19.2 KB (19192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b821e2e5a18cf712b978a1aed6e1d60ea5944421754f38c6b018288ba6a5d0`  
		Last Modified: Wed, 10 Dec 2025 16:03:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161d61d9eb96e745cfea30f580efba7d1f5f3511fe6a2d7fae238821980cd745`  
		Last Modified: Wed, 10 Dec 2025 16:03:48 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44666be8bc5d040960e9aee5807fe452f7885c8d651056b0343c89d9c7f47fc7`  
		Last Modified: Wed, 10 Dec 2025 16:03:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e9f4c93c24d4a025aab068829d2831e8ab8954d5875f50e916ad6ccfeb0c88a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5162418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddf249622e3451926df2fa748d6f212a680073782d3e6f3d86b2f662994c85e`

```dockerfile
```

-	Layers:
	-	`sha256:2338cf937c9b56feaef486c9303a38746d5df7c85f039d63ffe250b143d2cae9`  
		Last Modified: Wed, 10 Dec 2025 18:08:57 GMT  
		Size: 5.1 MB (5109889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7724078b03ee9a62371a97546ea4ea0f73b2c0bce85d2ce36c91d29adee98f8e`  
		Last Modified: Wed, 10 Dec 2025 18:08:58 GMT  
		Size: 52.5 KB (52529 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:trixie` - linux; s390x

```console
$ docker pull postgres@sha256:8efbf21eaa79007a6abf3ff84aa20b1224b4dd3fddcdd2c0d302f748956d71fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176851947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb0b2179302a78e32bd56af072d85996314c59a9cd86f1b1d5394cd864d1a29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:37:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 08 Dec 2025 23:37:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:37:29 GMT
ENV GOSU_VERSION=1.19
# Mon, 08 Dec 2025 23:37:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 08 Dec 2025 23:37:34 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 08 Dec 2025 23:37:34 GMT
ENV LANG=en_US.utf8
# Mon, 08 Dec 2025 23:37:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:37:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 08 Dec 2025 23:37:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:37:39 GMT
ENV PG_MAJOR=18
# Mon, 08 Dec 2025 23:37:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 08 Dec 2025 23:37:39 GMT
ENV PG_VERSION=18.1-1.pgdg13+2
# Mon, 08 Dec 2025 23:49:50 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 08 Dec 2025 23:49:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 08 Dec 2025 23:49:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 08 Dec 2025 23:49:50 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 08 Dec 2025 23:49:50 GMT
VOLUME [/var/lib/postgresql]
# Mon, 08 Dec 2025 23:49:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 23:49:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 08 Dec 2025 23:49:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 23:49:50 GMT
STOPSIGNAL SIGINT
# Mon, 08 Dec 2025 23:49:50 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 08 Dec 2025 23:49:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f041c2eec05398a39b8c49210328a00b614b14de35ace426628985d227a9635`  
		Last Modified: Mon, 08 Dec 2025 23:50:29 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30fe1a3a638e04c652fceed85dd6390ba5dc837da4c6481c544357b2f305a8`  
		Last Modified: Mon, 08 Dec 2025 23:50:29 GMT  
		Size: 6.4 MB (6408802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bd7cef9980726135977e2c0a06826353e5e8b8364dcfc3bcb0cf79b1079a27`  
		Last Modified: Mon, 08 Dec 2025 23:50:29 GMT  
		Size: 1.2 MB (1230052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dec2b6c612ef4be19ee2d5b6088f5037ccd20cc28777198aa04a724b82e828`  
		Last Modified: Mon, 08 Dec 2025 23:50:30 GMT  
		Size: 8.3 MB (8258856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718a19ed116e1b175b8b30fac5a4aa1f152fd3e4dbc95eff575656963adfd336`  
		Last Modified: Mon, 08 Dec 2025 23:50:29 GMT  
		Size: 1.4 MB (1398065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe1e316f58f319c21fb986a009c0bf8d935dd31cd666ebc4235816c66422a67`  
		Last Modified: Mon, 08 Dec 2025 23:50:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eb3d21caf86390b9d9b7499c063d1a557498afa42e7fea130acf0c8f758df5`  
		Last Modified: Mon, 08 Dec 2025 23:50:29 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55745e5b6164008bb3da4a90e8c3dc12269e40f01a0862003191482b5af12769`  
		Last Modified: Tue, 09 Dec 2025 03:19:38 GMT  
		Size: 129.7 MB (129692013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e941f9698e0ea6eae01c925281c3cfa0bfee3ac7d133889a0391213e04a9ca`  
		Last Modified: Mon, 08 Dec 2025 23:50:29 GMT  
		Size: 19.2 KB (19183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ea7950d0160ce45c6842b2d86e577e2ae4be9b4f51e5d4e28b0e003f31340`  
		Last Modified: Mon, 08 Dec 2025 23:50:29 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faaff9bead8a989c3839fae8e3dacfed99355ef28937ed7b5259a86293d567c`  
		Last Modified: Mon, 08 Dec 2025 23:50:29 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e0043e0793ca858f9bb512653f19e0364b571d780ad807371a09306a1c8a45`  
		Last Modified: Mon, 08 Dec 2025 23:50:24 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:1dfb8534fe816723ca6392d187d9828b343f8d3afa024a0b45c3d66f6ec253a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6025601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a55f81d6f12ea2b35148a25bae38daff647e215aaf98afb59eef49a790f5af`

```dockerfile
```

-	Layers:
	-	`sha256:3ab15ece57a40c98366818e4eb10632c895de944a578524bae83b7e7abde6a70`  
		Last Modified: Tue, 09 Dec 2025 03:12:59 GMT  
		Size: 6.0 MB (5973143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd81f040a023e7bb3d58f60c7601d5c0525e1f214bc6e3bc146eff53ed8850a`  
		Last Modified: Tue, 09 Dec 2025 03:13:00 GMT  
		Size: 52.5 KB (52458 bytes)  
		MIME: application/vnd.in-toto+json
