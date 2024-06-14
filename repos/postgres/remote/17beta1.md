## `postgres:17beta1`

```console
$ docker pull postgres@sha256:2b3793cecff53f283ce8571da38cd49e4923b2d5737ca929a69c36354fca1875
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

### `postgres:17beta1` - linux; amd64

```console
$ docker pull postgres@sha256:e19bc91c6f58d7fb454f8495a876658affb8034bfba274a3d9ab0362e93e47c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154395098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28f7e65be7744c0e3ba7f9bfea49ac608b2f4d7593b0116ab0c3bfad8752554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg120+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89fd732072a42913962411751f32b7b0a35fb6233e831e4fa8cafcb36ec0ae56`  
		Last Modified: Thu, 13 Jun 2024 18:23:18 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a4bc4a74221567fe75a93ba3522b0299aa70d06020bdfb3a3e5409c8e85acb`  
		Last Modified: Thu, 13 Jun 2024 18:23:18 GMT  
		Size: 4.5 MB (4533753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087e4d5ec836f18e97310b889f72783056fda7f4d27e872cd225c3c72f29f8bb`  
		Last Modified: Thu, 13 Jun 2024 18:23:18 GMT  
		Size: 1.4 MB (1449915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37efd7003a6c5c191583f6fc801494e2c53b2ead46c84588eb5d015b9eb2157c`  
		Last Modified: Thu, 13 Jun 2024 18:23:18 GMT  
		Size: 8.1 MB (8068895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1677c37acb2d7a6d71d2261df83b8ccd61a749c27fd98b74166acc5650a564`  
		Last Modified: Thu, 13 Jun 2024 18:23:19 GMT  
		Size: 1.2 MB (1196103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06493dfd1b8ba6e432cd4e340e2aee0bd2af24083b3cd624ea24c26cbc75623`  
		Last Modified: Thu, 13 Jun 2024 18:23:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89288f514ad5cff26d194ca72916fcb5c0142a946c5b702fa464cbda2a193d03`  
		Last Modified: Thu, 13 Jun 2024 18:23:19 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ef981eaaa78b22471a7f285622b5f221aad1893918a0cff7409743127e0e31`  
		Last Modified: Thu, 13 Jun 2024 18:23:21 GMT  
		Size: 110.0 MB (109975441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9994d5e745bc420a84496483a4b7ab0bd16959ee060bdbc2c33f9737d3b2406`  
		Last Modified: Thu, 13 Jun 2024 18:23:20 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64afdf6e07b49ce0e8d38c83a86c5e1a4e017bcad3dff8f1e257462eb3c3b00`  
		Last Modified: Thu, 13 Jun 2024 18:23:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf1a41a93b57b338919d154685dfd3635349ba0654fe435de0f086fd6a12b39`  
		Last Modified: Thu, 13 Jun 2024 18:23:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de6df55e46b5ea946ae54b47878d49bc2a9771ea7a2e9d308349acea07081e8`  
		Last Modified: Thu, 13 Jun 2024 18:23:20 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8beeb835f5b79861706650430c01ddedfcaa4bff4d85aff9637a24a754b0ba17`  
		Last Modified: Thu, 13 Jun 2024 18:23:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:bff889436e87150d1a77e6fc0066305919fe3386eab1a30909a0cf4de85989a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e20b6f148e752b184fa9d55c7b7274ae5ec29122f1984829d4b98cb9c21dfdb`

```dockerfile
```

-	Layers:
	-	`sha256:5b282e73b1e96266049bf84cf14aebaf293b2b7cfade5c70216005a1cca32c5c`  
		Last Modified: Thu, 13 Jun 2024 18:23:18 GMT  
		Size: 5.7 MB (5728035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a55ccc29c060e745f8b4122ba6f0a805cfa5a0c1956748be11f10eee4dea2de`  
		Last Modified: Thu, 13 Jun 2024 18:23:18 GMT  
		Size: 54.0 KB (53950 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1` - linux; arm variant v5

```console
$ docker pull postgres@sha256:c2e2b9b4e033ab5af641d4174a20f3900bc8f9c28566a5aed4e6ea81a571a586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147165204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c90f725fd02e8e997be1dd8c2a6f0a03aa391a95bc89468ff9d2989ba21d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg120+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76f93fe24faf9bdd2823e7ed0fa9bf1ae89c6d82d81309c0044fbd05c272b8b`  
		Last Modified: Thu, 13 Jun 2024 20:27:17 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2160d7118cc9f8e23b3033ea807d4e87947c45bfb8bcea73028027aa765329`  
		Last Modified: Thu, 13 Jun 2024 20:27:18 GMT  
		Size: 4.2 MB (4150952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5efce1143a2d44abdd1810dd3dfeb14c4ee36f79dc41476601665c7c40a2f54`  
		Last Modified: Thu, 13 Jun 2024 20:27:18 GMT  
		Size: 1.4 MB (1427070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e623323d67613018c639686712853eb77cd588d64ced98a25fd20512f43b1e6`  
		Last Modified: Thu, 13 Jun 2024 20:27:18 GMT  
		Size: 8.1 MB (8068972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee6b3c3492fbdef9666e4379393f2c59aff2ab2278dcc38c611ebe869696083`  
		Last Modified: Thu, 13 Jun 2024 20:27:19 GMT  
		Size: 1.2 MB (1194853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d2e67789ab63ba29790eec6bd56fe19d33551de322ceaa5f0bbf489a10b4f`  
		Last Modified: Thu, 13 Jun 2024 20:27:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e906e2ab7c56d77757417a3a48d2ba73236b668f3ef3ffe2788196fea729bb`  
		Last Modified: Thu, 13 Jun 2024 20:27:19 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e273225499d68a49938d5807425c3f656f696b0d8db6ceb59a40fc2e93deadf`  
		Last Modified: Thu, 13 Jun 2024 20:27:22 GMT  
		Size: 105.4 MB (105392810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b3bde5ad6808d3d53fbc54f40e666bb686619132fc6eef4f7656f20c85e213`  
		Last Modified: Thu, 13 Jun 2024 20:27:20 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9de1b489f08fb21850fcc7bfafa3b12919ac3f868b1ded3f7f35a5bada5d8d3`  
		Last Modified: Thu, 13 Jun 2024 20:27:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09187a3c8235521bbc36d16c3625766f7fc8ac3ed8bde8f470cbd49cfc9b0170`  
		Last Modified: Thu, 13 Jun 2024 20:27:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b2dbe27b1b1cf6c24b9782b3af9fb3605f20c4edbff4072d097b90091a9312`  
		Last Modified: Thu, 13 Jun 2024 20:27:21 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb13aa642cabbe76c7bf5278d406fafa1d9ceb210eaa68633e1579e971095a6c`  
		Last Modified: Thu, 13 Jun 2024 20:27:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:97c755a9b0d0e82fe7a306d4055228effcf1ec0010276b962fdd4d2521e1341a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5799277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1585b347fc25f8d574eec295ed10c94be627f22ea3c19a62464b3415868ca7f2`

```dockerfile
```

-	Layers:
	-	`sha256:a5a4ebcbf791ca418000650cf7eb1a7f51594af0dfa1152b453be81b357eb230`  
		Last Modified: Thu, 13 Jun 2024 20:27:18 GMT  
		Size: 5.7 MB (5745130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cd07347ad3b09d76456925de654bbf06050977c893a5e158fa4c3f28c3a29a9`  
		Last Modified: Thu, 13 Jun 2024 20:27:17 GMT  
		Size: 54.1 KB (54147 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1` - linux; arm variant v7

```console
$ docker pull postgres@sha256:afd2bb8a3661e082fe0aea3851ffa88ef9e4057b7312305fb9c42123d8a6c73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141837756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64ce5cf740d2a384da22335b1282d56e071c0348df1411c92501bb4a5a8cc8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg120+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493051253236caea97f219fd70aa5f22f8b46248ff1d3c3d3188d73ce0784a40`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6804256b124e139d9f0115e1d42291cc23b80dce76de35fd5698c162eaf1dbf0`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 3.7 MB (3742521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b531feac03289045c14b775e7e96c3ede9f3a2d05e3b6dd1e733009cf1bbb62`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 1.4 MB (1417097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66c7bb29e6b93b045ad24872cfa94249282a9726a9f006f38918a121c5ba9be`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 8.1 MB (8068841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b345cb504203c27252fd77886ea537ccbba6a85470442aae2a7829f01b742d27`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 1.1 MB (1066956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d104bf8bcc118bb31c29d3d8a68c778d2cb3ff3581269130a6cdcbe82a263ed7`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe06d964e32afda897c71c4829462b2d98aa14cf05e4ce8a1821876e9adb65c`  
		Last Modified: Fri, 14 Jun 2024 01:16:02 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cca36a3452942c6a488af3ec9f1eba80634e602fe6e42060475c9bd7f5a6f3`  
		Last Modified: Fri, 14 Jun 2024 01:16:06 GMT  
		Size: 102.8 MB (102781551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c854f4ff8d22e1411345b33b6b0f9ec24171f9c5b8c7c6bbbee4001b79759835`  
		Last Modified: Fri, 14 Jun 2024 01:16:03 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6c925e774a413e4d34f0ac8a0a7f1f02f68f3225a4941372ee49d2607fb71c`  
		Last Modified: Fri, 14 Jun 2024 01:16:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2c9867b67ec9561d4982257c43fb087c5391afe1457263c50caa3bcdffc06c`  
		Last Modified: Fri, 14 Jun 2024 01:16:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f07930f492f020f7ba3423cfabc46c1edfcaf1d4bdf51cb9cae95bbcb6362`  
		Last Modified: Fri, 14 Jun 2024 01:16:04 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738ef88bd549ff24f16e190a05446f8708fc91558389520f2b369a506e0d9ba4`  
		Last Modified: Fri, 14 Jun 2024 01:16:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:04e07e58826bc26ff931c89defb2f5fdcaab19342acc40571e7788a8db309c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5799089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632468b161311330acd3a708ec8fb691a41ab9dc829cdb16413b8a67dc038417`

```dockerfile
```

-	Layers:
	-	`sha256:47eca3ef0f1d8929fb36c26707ef2c4b4400404d932f23391e41aa498200e5ab`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 5.7 MB (5744942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85c7a47de58e6edfbe14bb880a39114d7f4d5d33dffd8fc10218b4db2f715f4b`  
		Last Modified: Fri, 14 Jun 2024 01:16:01 GMT  
		Size: 54.1 KB (54147 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d53daad008883deb00240f5e9f2d5706cd7abb2631b9027a9f9ef2e6cd134e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152590527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ab687da406bea3ab8d0a200fb43ba5dfbf13e85c86aedba4399fec6be5c4c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg120+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059b5c43db4127d3c84a4caee54092e336d3ba62e208c915e1644fb73a7c5e2f`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac4aa6c99e9f11007d4c9ef96a1b0dd6aa1ba9b32bb8f1eed1577047f513928`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 4.5 MB (4499134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f695f6dafe22ec09a8d465915c3f2df31da965a38406fe775765c9a6d6e5af46`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 1.4 MB (1382260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3531e6d72caa83e1e23ae04b0c519b1174a47e2c737f6f4bf8e2822a9acae84c`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 8.1 MB (8068931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8460f5c0f01056e728f9f916df72baeae6eb09bf8e6c86f8964a9822b8008cb5`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 1.1 MB (1108679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c419f8ddd2fbd2e547a8b11791240d264a925a69a36bc442567489c2755fd853`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54f6c55c74f6700f1cea329574b215d9662b08548c98081dabb64ac7caffaf8`  
		Last Modified: Fri, 14 Jun 2024 00:40:59 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cce0b88b6f839ee139d6c3721fb058a50498cd72bc49bcc62e828f33cab9748`  
		Last Modified: Fri, 14 Jun 2024 00:41:03 GMT  
		Size: 108.3 MB (108331295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ddf14c3c2a2ecc0b00b86e082b5ccee2a30fa23ad1662cbd7cd0e581053272`  
		Last Modified: Fri, 14 Jun 2024 00:41:00 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc1bce1b5058ad2e0a36b6e0b90680fd20ad01aacdae56b033d08fddb08bc8d`  
		Last Modified: Fri, 14 Jun 2024 00:41:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1c16bc81cca42d58e9a3513d6bc0909bae93ed4b277962f2e8b240d9e65196`  
		Last Modified: Fri, 14 Jun 2024 00:41:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5b061861d220709faf1ac3baada2d5a67a54e68ae9ee38c7b8ae54cc1f17bc`  
		Last Modified: Fri, 14 Jun 2024 00:41:01 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98df9d1f584f68dfd22f3ece4e23e5804062f2ad3b8d4cc49e1bb3fcce7fb767`  
		Last Modified: Fri, 14 Jun 2024 00:41:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:442c0af0718b19fef6368a4bde2e556cf2ff0819456c1ebd1fd3a4f7c7df0cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5788587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51be4c4944e621652cd19e0cb1bab5d2e314fef6009c874a4a39937d508fcee`

```dockerfile
```

-	Layers:
	-	`sha256:5d134affbbcded55d4e01abeac0af4f90b301752a372c44776cb0eac6a557b05`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 5.7 MB (5734352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d529faba4ae0e379bc61721b20b8783d93f957cfa0e35303e1a421e17c47eb59`  
		Last Modified: Fri, 14 Jun 2024 00:40:58 GMT  
		Size: 54.2 KB (54235 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1` - linux; 386

```console
$ docker pull postgres@sha256:df2666c767f81b895f521fa2101effc5e3fa50855abe175cf07a00ecc6d7cc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162559834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ed30af1e4e20bd1bb3d4fe8335f13e9053e4e9d3f8c3a61228771254190bd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg120+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b446198c5f33bfe3356fc6bc007222dccd917e350cc045c7223f58a7b5fd1e`  
		Last Modified: Thu, 13 Jun 2024 02:14:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59760f570f907543c24ab09cd411014de6d0c2298e5eff0ddd396592c86d39`  
		Last Modified: Thu, 13 Jun 2024 02:14:33 GMT  
		Size: 5.0 MB (4965072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf99053681c1771935b0d5f7bf518648bdc12fe9a99f30ed9062a912c52010df`  
		Last Modified: Thu, 13 Jun 2024 02:14:33 GMT  
		Size: 1.4 MB (1425611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c0e2064320d495e2c12fe207219064d7e3f3ca8aea703e3a0550fb2169ec5`  
		Last Modified: Thu, 13 Jun 2024 02:14:35 GMT  
		Size: 8.1 MB (8068941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f61d74991078062fb8bce7b86255f9cc8ec0eebac456dfb998dc55ae32ad461`  
		Last Modified: Thu, 13 Jun 2024 02:14:34 GMT  
		Size: 1.1 MB (1137167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd98e81eb011a248b16f5013461e00e33f69037492e4bcba537d57a85e95047`  
		Last Modified: Thu, 13 Jun 2024 02:14:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa1b38737aa6b939cceb92568f8bfdaa578a5ea1ff3a9dc5ad96e275f11122`  
		Last Modified: Thu, 13 Jun 2024 02:14:34 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc96588368e6a21d7fbb3d7dc10556be5894c6ed0dd78d7be0bf9e0c6798db2`  
		Last Modified: Thu, 13 Jun 2024 02:14:38 GMT  
		Size: 116.8 MB (116779815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca1aceef974194a4563899ff95c077d78ec7dd12a62e150f28a542e84dcf8c4`  
		Last Modified: Thu, 13 Jun 2024 02:14:35 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707182a427cfe8b82e80418eb5cb7ba73cd97d69cdbb425ba3f4f9581f5c7b34`  
		Last Modified: Thu, 13 Jun 2024 02:14:35 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572acf9c422c6ebe42e788d86bc9ea47f979ee8874193f50f931af5cc2b86c18`  
		Last Modified: Thu, 13 Jun 2024 02:14:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559aa4e3b9d792c3bd4b26cb879e058a2db46588b53b236493c896aa61f2e3c5`  
		Last Modified: Thu, 13 Jun 2024 02:14:36 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0580460976ba1115ea0586c5b81454b5cdd30293006ac642bcae2089f94f2bc9`  
		Last Modified: Thu, 13 Jun 2024 02:14:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:b46ee6f93d0688cadf3279bfed9fec0f60f1c07009ae3f92acac88c5f09a0485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407f01ea3c3c5e9f95d29d94cad007ebcf1259ba2073652204c5f4e08fe14056`

```dockerfile
```

-	Layers:
	-	`sha256:62ccb87bc671d3fb7970c26e89cc84d30e92933829f7127c61367e37d766f07f`  
		Last Modified: Thu, 13 Jun 2024 02:14:33 GMT  
		Size: 5.7 MB (5743209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf49488bab4a3f19940b5b03fbbed76c49fa816aa75c8f260d207a38f3aa802`  
		Last Modified: Thu, 13 Jun 2024 02:14:32 GMT  
		Size: 53.9 KB (53909 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1` - linux; mips64le

```console
$ docker pull postgres@sha256:bdfaeb3aabcf1aba0bc992d9f01b1118aa8de5383afb2d8e6a90fa0b2c941430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149803786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8716e211d3f151e759a57c529d2a7abfd07a8ccd0300c68ba604b5ec18ee2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg120+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e7b3f258eebcc001ec708f4a1a76516209149a6600fe7efcc4ff098596bc68`  
		Last Modified: Fri, 14 Jun 2024 16:21:55 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8e5f8f9151bb03d60ecbc112e2d6c7a2b80904d21657335b33f12fd377c66f`  
		Last Modified: Fri, 14 Jun 2024 16:21:55 GMT  
		Size: 4.5 MB (4475078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25565cdee2e4b4f87abfc7017bea5d3fe7691f8f5f3b43d617c12eb9decfdda9`  
		Last Modified: Fri, 14 Jun 2024 16:21:55 GMT  
		Size: 1.3 MB (1337111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8ff1a8c8de25f916a067e84caa425f8208cca4eda91fae38bc87161b3fe36`  
		Last Modified: Fri, 14 Jun 2024 16:21:56 GMT  
		Size: 8.1 MB (8069075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53a02dd19a7e5d13c8e7436537377195f170768d69611300794c59493c623a0`  
		Last Modified: Fri, 14 Jun 2024 16:21:56 GMT  
		Size: 1.2 MB (1182615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6ddcaf6b2aa995cff1df3ff9f3c343341c17be2ce7207b3863bd4dc4f61db4`  
		Last Modified: Fri, 14 Jun 2024 16:21:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed420c5cffea22518e732e2e3226a44adc6645bae3dfc8dc17fe011e27ea69`  
		Last Modified: Fri, 14 Jun 2024 16:21:57 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9080c5f493003377bc1af11f872b7032edcc4f1dbb3b41688679e5814aa4fd4a`  
		Last Modified: Fri, 14 Jun 2024 16:22:07 GMT  
		Size: 105.6 MB (105575501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d73c8d5ad85eea1bb54fa7188f79c177ee3d3c6d87980345327ece3d5bb4c86`  
		Last Modified: Fri, 14 Jun 2024 16:21:58 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7d433820d0adbc806d31854e7816b9acd7f73a95888bb01cef70cb2b8de4e7`  
		Last Modified: Fri, 14 Jun 2024 16:21:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31283b81029939e0fc74f7883802bacc7c4927166f41dfd1ff23847f28f13991`  
		Last Modified: Fri, 14 Jun 2024 16:21:58 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41e69ae5fa69fb7c6866369e8ccb2f6823a36ce6ae67157824a04ff50fbe50a`  
		Last Modified: Fri, 14 Jun 2024 16:21:59 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998ce339a77cbf992d760ad99def1b1d57b987111f7a1b2bc3b3de158865382d`  
		Last Modified: Fri, 14 Jun 2024 16:21:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:471b341dad868391537c28570b38902ff5a957a0098faae12388b94cbec0426a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 KB (53803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7537453eaad386202cc9f0e269e5fc039ae490ea80b0ce14e59c5cae077e4ed0`

```dockerfile
```

-	Layers:
	-	`sha256:e40ac257c6fde05d608f4c172fd7de4b3a8f7bdf0f206059c83fb7220a9bbe35`  
		Last Modified: Fri, 14 Jun 2024 16:21:55 GMT  
		Size: 53.8 KB (53803 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1` - linux; ppc64le

```console
$ docker pull postgres@sha256:ce79be8b47e9cafe5035eaec9b737f9aee6d642ea6aa14b47ec63467e45cce3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166641733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29798c1bd0a0fe0bb05cb909546cc31d42394f76cb54f76302a48d0c4a788056`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg120+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ce3d2e2dd26ed2ee971fce30509b03a268266ef6661c37ab01b06aaea977a2`  
		Last Modified: Fri, 14 Jun 2024 04:50:50 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0b107b67b75a99675cecac40b78e0a03b27dc41c4e72a49011d730ff9a626f`  
		Last Modified: Fri, 14 Jun 2024 04:50:50 GMT  
		Size: 5.4 MB (5368230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29592030092edd9c2d4f6377bb04280475e56b1a15e8a23fe33476cdcccfba`  
		Last Modified: Fri, 14 Jun 2024 04:50:50 GMT  
		Size: 1.4 MB (1371299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758aab932f37bd7ede2c247f8f364e06293cf29a6abf480c14c410dac0022d26`  
		Last Modified: Fri, 14 Jun 2024 04:50:51 GMT  
		Size: 8.1 MB (8068982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f494893d635f3afc4b0d6f82c1b3c1e22012e631b18d4efdf8b212308cbdce3`  
		Last Modified: Fri, 14 Jun 2024 04:50:51 GMT  
		Size: 1.3 MB (1283497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430ea084ff79461737d3396dad9f8b949252d1052c00c14b93f7f10986c8792d`  
		Last Modified: Fri, 14 Jun 2024 04:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f6a3290a408bdea48295cf53e8024a783f6f98f692b9240df81035056e3a07`  
		Last Modified: Fri, 14 Jun 2024 04:50:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f168d0d268b92ffa81fc046649047c9971ce3245d4df8c9fbe39df81086b64`  
		Last Modified: Fri, 14 Jun 2024 04:50:55 GMT  
		Size: 117.4 MB (117387952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e80f53bfafb78216ca766fb5d204b9391f73300477acb5fe6061945297b1922`  
		Last Modified: Fri, 14 Jun 2024 04:50:53 GMT  
		Size: 10.2 KB (10243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c83522f1552339b3e98cf2cb27ed741690551ad797056705dc50391a3379d75`  
		Last Modified: Fri, 14 Jun 2024 04:50:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b538c06c97cf0dc699eb3509713febf838a0117c1e835f635d93287512a1b7c9`  
		Last Modified: Fri, 14 Jun 2024 04:50:53 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0e925c7b7456e82e92ab67a78f5b5f57bcd3b891077e39fe5c0550a34b8165`  
		Last Modified: Fri, 14 Jun 2024 04:50:54 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff18a20d81951bb04f3e3e5e6d5e1e4022195f893ac6aae335198e68e425daa9`  
		Last Modified: Fri, 14 Jun 2024 04:50:54 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:9641f06db4179e10904f0e32404b04eb4ab71290a047a9f67ec762a4a285057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5789250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5441064df1ed04bbd965b9b8577488ad27137eee5cf1445d624896fc135c091`

```dockerfile
```

-	Layers:
	-	`sha256:7130027e7537c02dca577c4c58958319a1628daa57730dfd300d6776265d2bab`  
		Last Modified: Fri, 14 Jun 2024 04:50:51 GMT  
		Size: 5.7 MB (5735252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0f2d7097389ddeb0afc55ae8fd7e9d0d7a0ecfbdafa3a729988df705f857363`  
		Last Modified: Fri, 14 Jun 2024 04:50:50 GMT  
		Size: 54.0 KB (53998 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1` - linux; s390x

```console
$ docker pull postgres@sha256:64eea0da3835dedee08bcbb802a9d043438f4bf7f1a98cdcf3388ff4791bccd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (159950369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dca409d7228b6823a99453fd49d5d19dbb25c7ff1fee2f4641528ad712b509d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 29 May 2024 21:09:26 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Wed, 29 May 2024 21:09:26 GMT
CMD ["bash"]
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV GOSU_VERSION=1.17
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV LANG=en_US.utf8
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_MAJOR=17
# Wed, 29 May 2024 21:09:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 29 May 2024 21:09:26 GMT
ENV PG_VERSION=17~beta1-1.pgdg120+1
# Wed, 29 May 2024 21:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 29 May 2024 21:09:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Wed, 29 May 2024 21:09:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 29 May 2024 21:09:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 29 May 2024 21:09:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 29 May 2024 21:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 May 2024 21:09:26 GMT
STOPSIGNAL SIGINT
# Wed, 29 May 2024 21:09:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 29 May 2024 21:09:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df718a21529484d825e8d34c404257a0546286e7a7caaafa5e6aa3c284858359`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab19acd660b1d3121eadb9baf4f00251f6bad0be1f21e5546e9a7bbdf7c25f0f`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 4.4 MB (4391035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec53b5378db13907773971770802e5cd432e139b9ca53f853835ada5cff2134b`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 1.4 MB (1415933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f148609caa08348b01404906d68e5fac6a87cf8be9296e80c1478c47b119a32`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 8.1 MB (8123196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4a29b13525c5cab1218d23d20c299a8d1311c5619fb9a8586f2cdba6ec7dda`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 1.1 MB (1096730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b9b3dab45f719c1cfa9a9942b491b3d6577a1e12d3c44ec54edb4ba4bf475c`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce605bd25ed1e30eab9e389d318038b16d3f7fea277774f1e329cce643e81f83`  
		Last Modified: Thu, 13 Jun 2024 12:22:13 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fe62ea8ebfd17686095289ff05dfbd674a794d61eddbb0ac7589e3e24e7de2`  
		Last Modified: Thu, 13 Jun 2024 12:22:16 GMT  
		Size: 117.4 MB (117390453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4a1321fc64b32afb8e653a187d3b1c28594daac1d12f9e487421d229d5e4ba`  
		Last Modified: Thu, 13 Jun 2024 12:22:14 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21dc224cb40fbfbb1df72895f1c65a580a377f9597b29c7780f42acb4238295c`  
		Last Modified: Thu, 13 Jun 2024 12:22:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b50d0f63a5fc858cf9a6c0cf1fd7d914a7374d944865e6e50324d533aad0730`  
		Last Modified: Thu, 13 Jun 2024 12:22:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1215d2b6f6aa26910377699b51ce4d37fe51c3b57afb23d8ffb2dd93af29eaf7`  
		Last Modified: Thu, 13 Jun 2024 12:22:15 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94eba8fd4085410a9e15ce071f57d9553357640e9d1f8254e6ce8d806d55f72`  
		Last Modified: Thu, 13 Jun 2024 12:22:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1` - unknown; unknown

```console
$ docker pull postgres@sha256:6c252ff80baf211dd0a3aeaf97676b987e897a26f0e07d2bbd04bb37ae351fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a477782a438f92b496e69fc95ac53d82ff94e252de07a2e000dc3e77fd3fe6`

```dockerfile
```

-	Layers:
	-	`sha256:c0215386874c91c0a45a4b1e359593cccd7fd49cb98c91c6d1b4452636f6f87a`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 5.7 MB (5727429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f3645d0dd396e06acb44f08814e5eb24e03b7e8f91e157ad92714fa7a7bd88b`  
		Last Modified: Thu, 13 Jun 2024 12:22:12 GMT  
		Size: 54.0 KB (53950 bytes)  
		MIME: application/vnd.in-toto+json
