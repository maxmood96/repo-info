## `postgres:bookworm`

```console
$ docker pull postgres@sha256:7b7d96cf76dab8a1a7a6d4cb7956f5c1f21a3fa039c09044cf10d0d722ecdc83
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
$ docker pull postgres@sha256:c7351f458a646cea42dc5354bba18d1bbe79a4f312e299ba11750ee6406dc427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157128207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa0acade686565f8b76b53a4a5c3cf8f3e25bac424094cfe670ea0bad702606`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:33:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:33:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:48 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:33:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:33:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:33:52 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:33:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:33:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:33:55 GMT
ENV PG_MAJOR=18
# Mon, 16 Mar 2026 22:33:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 16 Mar 2026 22:33:55 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Mon, 16 Mar 2026 22:34:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:34:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:34:10 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:34:10 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 16 Mar 2026 22:34:10 GMT
VOLUME [/var/lib/postgresql]
# Mon, 16 Mar 2026 22:34:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:34:10 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:34:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:34:10 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:34:10 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:34:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308071462adeead29755aa392d093fe050ca61248538fbe49841434009ba1303`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb61875e3d87aa1b0c336f72303fc4bd5af58a61a5b1c57f37583957c706a73e`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 4.5 MB (4534214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b29bd3e087342c434293cec3dcfd43419809e098e77b09ec0677c1b5642ba21`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 1.2 MB (1249541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1a80f7ea9bf2e78899467d2f9de6cce724539ed38d70e7025886439567c5df`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 8.1 MB (8066484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46706ee5d448c952935bf108f87839ee216b593259da33cca99586559afe6c6c`  
		Last Modified: Mon, 16 Mar 2026 22:34:30 GMT  
		Size: 1.2 MB (1196402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14008c33708c61917d31b583701528a15c2b4397ce0d5b26455ccb3a7cc7582c`  
		Last Modified: Mon, 16 Mar 2026 22:34:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e63d36f0d5fbf2e6612d230bd9a647e81ced751d892eda783ef8c0967915d4`  
		Last Modified: Mon, 16 Mar 2026 22:34:30 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fb7f61decccae552e700798f296bcc0386d890616b418023ccc45a316a8364`  
		Last Modified: Mon, 16 Mar 2026 22:34:34 GMT  
		Size: 113.8 MB (113815543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d1eb966d5f28c28130d8f3b7733da89c5fc235b422c14a30e095ffef85100a`  
		Last Modified: Mon, 16 Mar 2026 22:34:32 GMT  
		Size: 19.2 KB (19229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e87119e4c7ba939f3ffa8e9b226ab44a78154da66ef5a3bd9a8621ca7348628`  
		Last Modified: Mon, 16 Mar 2026 22:34:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247caab38ca6b3c31630467712c2e87f60622cf979b789f600663c300513ec29`  
		Last Modified: Mon, 16 Mar 2026 22:34:32 GMT  
		Size: 5.8 KB (5835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb01a2d7819c865bb32f6ccefb3f0403a054b11989f6a215a9435eb05dcfdf8`  
		Last Modified: Mon, 16 Mar 2026 22:34:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:035a78047f24e3fe96e5abe785e633d0c59881519c9fc9326422bb6c77071915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693b044a3bb77b2438a4c07374d6d99492f2cf61005a37630571308bc16bd75a`

```dockerfile
```

-	Layers:
	-	`sha256:e83f935543f564da73ea073e28cb86a8ce80ba27fa0a40edadcee27a850ebdf0`  
		Last Modified: Mon, 16 Mar 2026 22:34:30 GMT  
		Size: 6.2 MB (6156497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee3c66c50f1845bf28a49c2ffaf681095d987911b857d51a7cc3fe8b7773b1a8`  
		Last Modified: Mon, 16 Mar 2026 22:34:29 GMT  
		Size: 51.6 KB (51589 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:5169ac9d02afca280e5d88df4669c8c2531feb17b0c86fc18c9068debab07839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87222825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc98f8498631aad89de2cbc12f1c1a0c57213abb05ad76aeb4ba4903e5356062`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:01 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:44:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:18 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:44:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:44:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:44:26 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:44:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:44:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:32 GMT
ENV PG_MAJOR=18
# Mon, 16 Mar 2026 22:44:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 16 Mar 2026 22:44:32 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Mon, 16 Mar 2026 22:56:51 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:56:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:56:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:56:51 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 16 Mar 2026 22:56:51 GMT
VOLUME [/var/lib/postgresql]
# Mon, 16 Mar 2026 22:56:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:56:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:56:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:56:51 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:56:51 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:56:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3f1e11847ee1bf3b5b4789698fd7943a2f92f317682fd98071438c59f096b12b`  
		Last Modified: Mon, 16 Mar 2026 21:51:51 GMT  
		Size: 25.8 MB (25765607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ef36273d9fa45dbd8c73489530f2c34dd7e376d9a5d8a84cd08c1c8bb05ae6`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf471a819b71ced4adaadfbd0a8d906f730733bff405b86518bda82b98a8eb56`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 4.2 MB (4151337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddee39686fcc2064ae9db5f23f121f28375f698e9e16bdfc8c6256e7366ebc16`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 1.2 MB (1220138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f57b7279d9495fef9bcaf240e563d71c30f0da11b13d0207d72c31fd3d4595`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 8.1 MB (8066574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7edbdb63be524b471856abba615bfd5433f8c73fb54c0e34b75b21bff7d983`  
		Last Modified: Mon, 16 Mar 2026 22:57:05 GMT  
		Size: 1.2 MB (1195080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc0561c9ed0bb2939f9453c721bb6a265d9a016aa36776c2cd4259b4bcc3fc1`  
		Last Modified: Mon, 16 Mar 2026 22:57:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6839a059aca6490a2913f6823e9e9714bec8cc887533fed5f2efe420155177e`  
		Last Modified: Mon, 16 Mar 2026 22:57:05 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f144f80af198cf71940c48e68899dc1933e68fa1824a57ba8f0b63d76e18289`  
		Last Modified: Mon, 16 Mar 2026 22:57:07 GMT  
		Size: 46.8 MB (46794286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daad08ee2bfcef387869289afb4b46a754933e0862421190c26fc66306bd6f0`  
		Last Modified: Mon, 16 Mar 2026 22:57:06 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282cd18d288ab4ee17a65c0e61d544170ed200a0a4f83427faa7dcd507f99baf`  
		Last Modified: Mon, 16 Mar 2026 22:57:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ea21fdb2b208e2c9023b52569117821bb0675457e959ae4f7dd773025d708c`  
		Last Modified: Mon, 16 Mar 2026 22:57:06 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73146c3caab124584309cfbb04740921976dbf8754f5cdc80b0e06e7948ccd0e`  
		Last Modified: Mon, 16 Mar 2026 22:57:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:90590a33562527c77cdc39b78d7166c9a0bb71061ad9b94a4cb77237e613b1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315fbfb77372e5ccb8cf2ce038d6fe65450634cfaa935f3fd5a4f67283ab847e`

```dockerfile
```

-	Layers:
	-	`sha256:e141b0c9c53c471a0c76fb44152804437988b86bea8627040d66ba12401e6d2d`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 5.3 MB (5317016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9afb7fdf1693a3df76101fa43a33a133f0213522df6090112fcfcc6b3caa5797`  
		Last Modified: Mon, 16 Mar 2026 22:57:04 GMT  
		Size: 51.8 KB (51786 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:4c28a216384c106e7e4399f6ff796fa79c6c85361e1c56204a579e0cf6025f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83343740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad585e2d8afeedac8a0e038ed01caf160d1664db3ec08e66888c6838428226ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:47:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:47:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:53 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:47:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:47:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:47:59 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:48:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:48:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:48:04 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:48:04 GMT
ENV PG_MAJOR=18
# Mon, 16 Mar 2026 22:48:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 16 Mar 2026 22:48:04 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Mon, 16 Mar 2026 22:59:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:59:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:59:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:59:31 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 16 Mar 2026 22:59:31 GMT
VOLUME [/var/lib/postgresql]
# Mon, 16 Mar 2026 22:59:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:59:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:59:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:59:31 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:59:31 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:59:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:91e7faf28870f2fc83e4505d37fd660d78f56057e7a982a218dee6bf49b341c3`  
		Last Modified: Mon, 16 Mar 2026 21:52:56 GMT  
		Size: 23.9 MB (23941345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ebac59baeb83ab5fad03a70a8a6661013827c91817a08bbf6f0131af5f3d41`  
		Last Modified: Mon, 16 Mar 2026 22:59:44 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96562b40b7134120a0ff72230b9c85389c387463c1f18821aaa4d527fb8af21`  
		Last Modified: Mon, 16 Mar 2026 22:59:44 GMT  
		Size: 3.7 MB (3742700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e097940186b839b2766bb7ce9b648538e1acee1f7c13f7de34dc4a4ddd660e90`  
		Last Modified: Mon, 16 Mar 2026 22:59:44 GMT  
		Size: 1.2 MB (1216037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5340c0caaf0a307289f7b33aef09242feb0efc0c9650b9fd8c1289ab5add18d`  
		Last Modified: Mon, 16 Mar 2026 22:59:44 GMT  
		Size: 8.1 MB (8066434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a8b2eff7b5160c81058e7d15969d78cad0f358fbd0af35e6a095865d99b2c8`  
		Last Modified: Mon, 16 Mar 2026 22:59:45 GMT  
		Size: 1.1 MB (1067300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140cc29335dc1e0656e6491ef80f0076d1fdfb8af1aa54aa5398fe9be1a83d0b`  
		Last Modified: Mon, 16 Mar 2026 22:59:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce05d9c22277da42f8d7f6277e67646e0e850cb3b1d84613a53b13d7cae9c7e`  
		Last Modified: Mon, 16 Mar 2026 22:59:45 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aba225419bbde22ee3ae34794ed04fabe37e34fdd8fdb62c06f6b2d50fd9c2`  
		Last Modified: Mon, 16 Mar 2026 22:59:47 GMT  
		Size: 45.3 MB (45280117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6e61ec25378c7d2b93d5d95cee939021d5c81353e91f10a3a2c5a9ee63d09f`  
		Last Modified: Mon, 16 Mar 2026 22:59:46 GMT  
		Size: 19.2 KB (19226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50dc0a41058488529b0c7412812c1e90b1b3c40e7b55761c2290c57434e5a32`  
		Last Modified: Mon, 16 Mar 2026 22:59:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3be2905568c1a592d6717cded4a60bc892b55521660994a371a2b14751e9523`  
		Last Modified: Mon, 16 Mar 2026 22:59:46 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc4cc45f01b00ca64c462c3fe3d1f16eb05b840c221471cd8f3d75a8c1b746`  
		Last Modified: Mon, 16 Mar 2026 22:59:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:aa85758671f0fe83c3a9b7f2c9753f3a4e58c6decd56e1499948634a2802ffaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33aa1db8014d702fd2aa55902aa7698145bdee4d2a7c919efddec75ccb5fabf`

```dockerfile
```

-	Layers:
	-	`sha256:514242641e078d43f63a673c60ff893bca30ed6c19aa5c4d49b713e0f2deba38`  
		Last Modified: Mon, 16 Mar 2026 22:59:44 GMT  
		Size: 5.3 MB (5316267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f29954f3da5acefae76511e67d89dc2dfabc874d6af5d415b059a59c8bb5c746`  
		Last Modified: Mon, 16 Mar 2026 22:59:44 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:cf9426fa758bf8ab93b83f28dc17ace8a41e4271a63357206b1030d7951908f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155115171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548234d8273148a27302902a5aa05ff60fc44434c3b8d7a253988ffa8476ec2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:35:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:35:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:25 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:35:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:35:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:35:30 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:35:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:35:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:35:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:35:34 GMT
ENV PG_MAJOR=18
# Mon, 16 Mar 2026 22:35:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 16 Mar 2026 22:35:34 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Mon, 16 Mar 2026 22:35:50 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:35:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:35:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:35:50 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 16 Mar 2026 22:35:50 GMT
VOLUME [/var/lib/postgresql]
# Mon, 16 Mar 2026 22:35:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:35:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:35:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:35:50 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:35:50 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:35:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaad140a72db3e18b0fcaeee5c2e666f71791daa167ea8cb228161a3ae973f6b`  
		Last Modified: Mon, 16 Mar 2026 22:36:09 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff374c7356c54c3c65e69ca1933d91243a65ade27e3dfaafe6d035151f54771`  
		Last Modified: Mon, 16 Mar 2026 22:36:09 GMT  
		Size: 4.5 MB (4519542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be10d0485831b243a403e7e1b73469399e8e59c0d26e9853c91935f4911b1dd`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 1.2 MB (1203321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8420628f40d1c859837b172fb6003662efdc550f2a0db952fa6757de4d9389`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 8.1 MB (8066502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ed69009603b4aa627db027bf990bcd749a0691332eabce67cd2be54704c334`  
		Last Modified: Mon, 16 Mar 2026 22:36:11 GMT  
		Size: 1.1 MB (1109014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3779ed79afab2fb0c9df38137fa835d2f69a0eb06e73b3d246704dc690ee027`  
		Last Modified: Mon, 16 Mar 2026 22:36:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45fcd79ff1071987a31218b6a29ff7f9e163f62f3108e5f2d8b209c9054a7ac`  
		Last Modified: Mon, 16 Mar 2026 22:36:11 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a454fbafab6ee7e50a040f6f295df32042b2e2cdc0dc0d1d47d16961c924e`  
		Last Modified: Mon, 16 Mar 2026 22:36:14 GMT  
		Size: 112.1 MB (112070924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3de9652abb2c1bb170eac632846c912d2a5a852cc60f1e65734804f5e9127a5`  
		Last Modified: Mon, 16 Mar 2026 22:36:12 GMT  
		Size: 19.2 KB (19225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159f3aaadd7100016c8fa113405ddd064f8d7ff7c63da56891dbd6cffc030006`  
		Last Modified: Mon, 16 Mar 2026 22:36:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5e596e136b1bc89dcb1ec760b14f65c9bfa30b6f65804a888185a687533c54`  
		Last Modified: Mon, 16 Mar 2026 22:36:12 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfc9ec5cce99d70eaa614b28f09faf114c6d35d3ddd5b834700e46501261e9a`  
		Last Modified: Mon, 16 Mar 2026 22:36:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f64004d44595e46bd424713d6e827722bf505ae657e8ab7edf0263ee14968bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beed9524c25411cbe5ffc88faa1b401051bd3e7640f1f142ac7f59e2a7be5593`

```dockerfile
```

-	Layers:
	-	`sha256:b6e23121e3905f868cc4ec7796d16901c2d817c625eca02bb0c07c6109951cc9`  
		Last Modified: Mon, 16 Mar 2026 22:36:10 GMT  
		Size: 6.2 MB (6162822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d08f69e2f27c1ce26bb2b4c97b3064c29fd1d12a5975bc0a400eeafc1be2f38`  
		Last Modified: Mon, 16 Mar 2026 22:36:09 GMT  
		Size: 51.8 KB (51832 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; 386

```console
$ docker pull postgres@sha256:785f4cabf49e7bb81ce64a7f62994b238131c6a578f5a6a8ca0eccc4061e802e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93997180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a86e7c9c1d8026a76282172fbdb1bd5e1dbbef511b5a4221e53f875b5704516`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:30:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 22:30:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:30:35 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:30:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:30:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 22:30:40 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 22:30:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:30:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:30:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:30:44 GMT
ENV PG_MAJOR=18
# Mon, 16 Mar 2026 22:30:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 16 Mar 2026 22:30:44 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Mon, 16 Mar 2026 22:39:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 22:39:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 22:39:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 22:39:30 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 16 Mar 2026 22:39:30 GMT
VOLUME [/var/lib/postgresql]
# Mon, 16 Mar 2026 22:39:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:39:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 22:39:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:30 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 22:39:30 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 22:39:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f649af5ed0883ac0b5027f768cbd9576b7bc8c76adac1eddeb4035e88b9258fe`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 29.2 MB (29221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454b94f384b75ce9849d8497cdd61757dc65854244bb502b1afcb9f4f1a3409c`  
		Last Modified: Mon, 16 Mar 2026 22:39:42 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37b9ee31d6ea0d57a7d4b1bdbbafa45187ca75effd9061bda4a5c704a2af26a`  
		Last Modified: Mon, 16 Mar 2026 22:39:43 GMT  
		Size: 5.0 MB (4966099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edee3da9df1b4f34802deb95a8c633c2e6a448cfe25eae7b491651abe1077040`  
		Last Modified: Mon, 16 Mar 2026 22:39:42 GMT  
		Size: 1.2 MB (1218659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52bebc1cb742def46cc465d25ffa5c4c982dfeb8cf7d48ec7a64bbc933e1651`  
		Last Modified: Mon, 16 Mar 2026 22:39:43 GMT  
		Size: 8.1 MB (8066453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9000e5f1f2a0c7f957e870030b9676e7200393390e529dc24480eef7c4742206`  
		Last Modified: Mon, 16 Mar 2026 22:39:43 GMT  
		Size: 1.1 MB (1137478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfca9262c4a971b5dc9bddfc224810a4ce8d346eaeab296db682092de35f8a8f`  
		Last Modified: Mon, 16 Mar 2026 22:39:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62703cfc2fb23e8add60bd7be21875c45e91ae02ba45d11033ccd07746c9f6d7`  
		Last Modified: Mon, 16 Mar 2026 22:39:44 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e2acc211c5bec6a07746340d6bc194661c68f0e86f8d5d161386af7fdedb9b`  
		Last Modified: Mon, 16 Mar 2026 22:39:45 GMT  
		Size: 49.4 MB (49356999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d5b97327265034f7c92bc57d5e18801f1c5c700b7c10a7999c96b82e1f8bbf`  
		Last Modified: Mon, 16 Mar 2026 22:39:45 GMT  
		Size: 19.2 KB (19229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb04d8e64c7bf13a78fb9c3355494ec6c32e4ff34dfda1170c366889caa54d1`  
		Last Modified: Mon, 16 Mar 2026 22:39:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea63c7974e9886ac6dbbbe700bfea29bcd3d6162ed51250ce8ef89ca539cda4a`  
		Last Modified: Mon, 16 Mar 2026 22:39:45 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e49ff06cef05691b493542be8dbadb826759bf28ae8cd9291d4de604585b83`  
		Last Modified: Mon, 16 Mar 2026 22:39:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9ab2b2988976a4880ad320528a1692ea58449069e271ffc26e18645b5113c210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e821c5e3700a658f87a0a2a71e19158dc3bb0c73d7a43f172764f2bb1a062be8`

```dockerfile
```

-	Layers:
	-	`sha256:4e97ca3f1941528b75df4b2ced2fd73ba2321c9f115e5edeb002667d7d5fd561`  
		Last Modified: Mon, 16 Mar 2026 22:39:43 GMT  
		Size: 5.3 MB (5311582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eec30412f7f67bdc655e00184a3300e87456b8a25bdbc8941aefae74ec0e277`  
		Last Modified: Mon, 16 Mar 2026 22:39:42 GMT  
		Size: 51.5 KB (51538 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:b07665b2e51fdb272de7218c8d312ebf7dc32b0ff3c55f1f734a5d37e47f8606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156003334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf71fcb2e44ccdf32fd7b5acb1dbc8f2ba3ca377a927115f4e91928f75ee5da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:43:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 24 Feb 2026 23:43:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:44:15 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 23:44:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 23:44:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 24 Feb 2026 23:44:43 GMT
ENV LANG=en_US.utf8
# Tue, 24 Feb 2026 23:45:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:45:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 23:45:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 23:45:07 GMT
ENV PG_MAJOR=18
# Tue, 24 Feb 2026 23:45:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 24 Feb 2026 23:45:07 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Thu, 26 Feb 2026 20:26:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 20:26:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 20:26:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 20:26:31 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 20:26:31 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 20:26:32 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 20:26:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 20:26:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 20:26:34 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 20:26:34 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 20:26:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:00b501106805d55ebe605ff077d09c8c22aa2ccf0dd9ceffb2a21c5319633322`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 28.5 MB (28526197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a6f997a2bae9d6583f7a9d6141815e9b9041dff337d7ac153b3f46c5b805f5`  
		Last Modified: Wed, 25 Feb 2026 00:57:53 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd847e167f615e000df95c8ddbf4ec913956e8de429393c14d6579c8fa3b6eec`  
		Last Modified: Wed, 25 Feb 2026 00:57:53 GMT  
		Size: 4.5 MB (4475211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b6c5cb25f9d256fb91972058d92c97ec72660257a5e4a0567b93d983683e4`  
		Last Modified: Wed, 25 Feb 2026 00:57:53 GMT  
		Size: 1.2 MB (1159230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d89b9e442925e9f99cc7d8126d286c933d9fa2af1dcd629bbe272d3991148e6`  
		Last Modified: Wed, 25 Feb 2026 00:57:54 GMT  
		Size: 8.1 MB (8066656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf9052eb778f8906ff20e40210c947a76e79676a164349c0d43640103061a45`  
		Last Modified: Wed, 25 Feb 2026 00:57:54 GMT  
		Size: 1.2 MB (1182880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6855c7d85646174eb68be28db5ef4c48412e69cc602e86bd03308406068383`  
		Last Modified: Wed, 25 Feb 2026 00:57:55 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b8fcdebfff3d96daa7d06b1c7d79991f36b897615adee4b706b0a3403cc991`  
		Last Modified: Wed, 25 Feb 2026 00:57:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055179cdcceae389edc2b91e9d998265cdc8c01e509a321a627b89cb51925f17`  
		Last Modified: Thu, 26 Feb 2026 20:28:41 GMT  
		Size: 112.6 MB (112563354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662604faee17fda3ed18e1f1228583b5166cf2846bcd0ee724de06200323abd3`  
		Last Modified: Thu, 26 Feb 2026 20:28:30 GMT  
		Size: 19.2 KB (19234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbc2ff90c2823f6ae1ce274943695bc203cbdb4399fbfa17c9c5dadb1b2c91c`  
		Last Modified: Thu, 26 Feb 2026 20:28:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf547e53c1d32b37b305c5f6732ad40cac242a9424facda8618a075ef36011`  
		Last Modified: Thu, 26 Feb 2026 20:28:30 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f479ebcc4d8f109a9ef2fc18c5f7788956ac74c151d28e83bf1083bac6d0d5`  
		Last Modified: Thu, 26 Feb 2026 20:28:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5c476075e4a3691790a5f6af1d8cdf214a4b4d8fb94b359fd0bd8233cdc80457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 KB (51461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d19667feaaa71bf9aaad31cd41ab8ec16d604580a94a4b678bf038c7081950`

```dockerfile
```

-	Layers:
	-	`sha256:9cbceafbd5b3fa7d570f2a0b976d62a69e85437a0ae41fb15f6c45020b4f4d7e`  
		Last Modified: Thu, 26 Feb 2026 20:28:29 GMT  
		Size: 51.5 KB (51461 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:fcd88fa1338014d07e499cffbd1404d2c2f89472f1b115b322861c47f12891e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170031373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a73dbd987d0f9010ba5d3290cf5bf87127bd391f23262c9624cec7f993510a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:58:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 24 Feb 2026 20:58:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:12 GMT
ENV GOSU_VERSION=1.19
# Tue, 24 Feb 2026 20:59:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 24 Feb 2026 20:59:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 24 Feb 2026 20:59:24 GMT
ENV LANG=en_US.utf8
# Tue, 24 Feb 2026 20:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:59:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 24 Feb 2026 20:59:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 20:59:34 GMT
ENV PG_MAJOR=18
# Tue, 24 Feb 2026 20:59:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 24 Feb 2026 20:59:34 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Thu, 26 Feb 2026 19:15:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 26 Feb 2026 19:15:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 26 Feb 2026 19:15:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 26 Feb 2026 19:15:09 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 26 Feb 2026 19:15:09 GMT
VOLUME [/var/lib/postgresql]
# Thu, 26 Feb 2026 19:15:10 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 26 Feb 2026 19:15:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 26 Feb 2026 19:15:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Feb 2026 19:15:11 GMT
STOPSIGNAL SIGINT
# Thu, 26 Feb 2026 19:15:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 26 Feb 2026 19:15:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fc91454a9561e6b11ad598da906c78edd30b499ff2234b49dd32562f2c327c`  
		Last Modified: Tue, 24 Feb 2026 21:01:12 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f53303ce4ed753a310b22dbdd2260f27925694aff49febb2da931d330f89bc`  
		Last Modified: Tue, 24 Feb 2026 21:01:12 GMT  
		Size: 5.4 MB (5368639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee621534fc9f66a74f75456ce763e23a22f0bc8cdc58a4cf5c532ec7ead1e2b`  
		Last Modified: Tue, 24 Feb 2026 21:01:12 GMT  
		Size: 1.2 MB (1208227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90aa3b04a3699b4d451ff19b898207a36991bb24bf9881e1da9dcb3840f656e8`  
		Last Modified: Tue, 24 Feb 2026 21:01:13 GMT  
		Size: 8.1 MB (8066558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943e3810ae0d32fbeb98071444fca03c119b767293f42d9aa091464e3b675fe7`  
		Last Modified: Tue, 24 Feb 2026 21:01:13 GMT  
		Size: 1.3 MB (1283663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbd92721995d8dfe36dd9311ada9eb9d7eb6474ce076a43abffcccfa4a272c7`  
		Last Modified: Tue, 24 Feb 2026 21:01:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e741e6e7c45af4f4d1a256134152099f5565df888582d1592322f7bfe7df5a`  
		Last Modified: Tue, 24 Feb 2026 21:01:15 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b21368867bb42942da649095f9c65ae56ab8c371d92f307e94d0d5ac3258c06`  
		Last Modified: Thu, 26 Feb 2026 19:15:53 GMT  
		Size: 122.0 MB (121996142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2b94bdecd8ac29f50678b7065aae384aa98ed76c7c58429909dbd9119a264b`  
		Last Modified: Thu, 26 Feb 2026 19:15:50 GMT  
		Size: 19.2 KB (19232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad1e36f0527879729dec22696056c6b5c8df978bfd294059380b2a0d1ba9161`  
		Last Modified: Thu, 26 Feb 2026 19:15:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5bf120d2276818e0c70e96662bc26d19f17266c2eb710233a31a6754bbed1b`  
		Last Modified: Thu, 26 Feb 2026 19:15:50 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffc5cafb21a93ddf0df6aea3c2ebb49a4872816419375038664e2c0a88deab1`  
		Last Modified: Thu, 26 Feb 2026 19:15:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b09fa41136e8c056ca8089a97a67a375f0ecdd76263e419fe3327573b6bc3272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0fc278b4a57c4d61ac75c7c76991d416e6a7d5af8198f754274d745e75d1f2`

```dockerfile
```

-	Layers:
	-	`sha256:dfa3ad0cb34d1c4531d1d2f1c8316788167f35bf7295d69e4273e5f71711a80a`  
		Last Modified: Thu, 26 Feb 2026 19:15:51 GMT  
		Size: 6.2 MB (6163882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0506c3f20604d6be77c6863c77432dc70e795da3642ec7645ef7b1f0601672b`  
		Last Modified: Thu, 26 Feb 2026 19:15:50 GMT  
		Size: 51.6 KB (51648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:c486825a30d9a061025aede8cde49568c641e825efd21bf450426a02d54a5c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166446553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08601dbfae07aec44393ddcd1901c1fb8435a9596338a26d812f01e6ba123132`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:03:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 16 Mar 2026 23:03:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:03:59 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 23:03:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 23:04:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 16 Mar 2026 23:04:04 GMT
ENV LANG=en_US.utf8
# Mon, 16 Mar 2026 23:04:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:04:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 23:04:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 23:04:09 GMT
ENV PG_MAJOR=18
# Mon, 16 Mar 2026 23:04:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 16 Mar 2026 23:04:09 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Mon, 16 Mar 2026 23:18:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 16 Mar 2026 23:18:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 16 Mar 2026 23:18:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 16 Mar 2026 23:18:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 16 Mar 2026 23:18:22 GMT
VOLUME [/var/lib/postgresql]
# Mon, 16 Mar 2026 23:18:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 23:18:23 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 16 Mar 2026 23:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:18:23 GMT
STOPSIGNAL SIGINT
# Mon, 16 Mar 2026 23:18:23 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 16 Mar 2026 23:18:23 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37c397d4cf5d96014b5d7732cd538e0df4355c117dfb4919b2b0e1378ca3696`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd735821172fbe4cf93079f7649cf26d2d82cf9774b02e60922c2a0413aca97c`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 4.4 MB (4391203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9e2daece88cc5e28710972e14a1c56b2747e9a96335d8dbcdd197686fa12f8`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 1.2 MB (1222800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30d84746c78b8bd690ce46a69ddd62108696fa7aa2309c0a5ce62038fa06aac`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 8.1 MB (8120745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44539cfb76f7c2597f15d57769a0628faa73a794048554bfc8743dcd6f3d731`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 1.1 MB (1097060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf246121e4f34eb7ab067d2936d11a5991af0bdd7570f0aa9da69970bdf4ba8b`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd39ef00523133f2004b72289d610e6ad2fcc42f94dbc0ab53dc02fa1b6c463`  
		Last Modified: Mon, 16 Mar 2026 23:18:55 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487e7dc08b63dbba74f2a587ce5dc0e77a33da22efcaba4f302252c44c7221c6`  
		Last Modified: Mon, 16 Mar 2026 23:18:58 GMT  
		Size: 124.7 MB (124693418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ecf98e68957e86ce6520a87dc56a2cee50f3b753e3b757d49c13314791e705`  
		Last Modified: Mon, 16 Mar 2026 23:18:56 GMT  
		Size: 19.2 KB (19231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa84725f2ea541b0283efa0241c07a8a0b2f5a4895f5da6cd186191f7f9e3d`  
		Last Modified: Mon, 16 Mar 2026 23:18:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ef824fd5f1ff3e8122171aee63ec3e52cab8432918c084575e0bcf296b2ec8`  
		Last Modified: Mon, 16 Mar 2026 23:18:56 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba29373af5c2c09f0f1b191f070909fa029fa0585d2ae00aa2ecd4126857b2e1`  
		Last Modified: Mon, 16 Mar 2026 23:18:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d73aecaab091392e8a4f087b9da3af090de83f7e489a2b5cffedd8e1a343fc3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abe0a14e4a341de1cc210a598961eb956272adf5a3acd4a6bbe29d22356e40f`

```dockerfile
```

-	Layers:
	-	`sha256:663f3e8965cb7ecb6985866ce8a4817735f9d89d52c13b54a69d86478cc353da`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 6.2 MB (6171155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8065a68bd9cf37431f46fc17f0fdecb75d5f6d0cd6782c583e49b5c8c8dfb5c`  
		Last Modified: Mon, 16 Mar 2026 23:18:54 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json
