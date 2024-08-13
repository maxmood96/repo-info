## `postgres:16-bullseye`

```console
$ docker pull postgres@sha256:bbdec45fdcf5c9c963e6714caf87aeac01432f6afb390def50c4e986e312c331
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

### `postgres:16-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:9bae4553dfa5fac6317e9f83ae8c7ccaab085af77b59fe3f746df491cc4fb345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (145043153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86b56d49ef121152fbd40b1a150132c64cf6c4ccbac764ae72d87c34a134438`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b4dbb3a27781820f60c660b4f6e28e1076849b98bd8488307c55a972a41469`  
		Last Modified: Tue, 13 Aug 2024 01:21:37 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36a30a3e7442a340bdee100b98b19f2e71b057aec38b0c256e77537fcb0a6a`  
		Last Modified: Tue, 13 Aug 2024 01:21:38 GMT  
		Size: 4.3 MB (4308186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a7a170470bb44d6e7e291281f9e0d59aea454203334a0fe0923f6dd1c43b6a`  
		Last Modified: Tue, 13 Aug 2024 01:21:38 GMT  
		Size: 1.5 MB (1472180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f34ed4e0599cc5c18e61e2f16c84be46d22194b816a551f0b446e9b992dc24a`  
		Last Modified: Tue, 13 Aug 2024 01:21:38 GMT  
		Size: 8.0 MB (8044473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689827df65025e2bb135abc17cb3d44c69f131af82d0573c75ebeefe961d6588`  
		Last Modified: Tue, 13 Aug 2024 01:21:39 GMT  
		Size: 1.0 MB (1038366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1fd47a76a5fb21e97fe08f5c7907cba4bacc5e3c767ab5ca73d6b5a801bb0d`  
		Last Modified: Tue, 13 Aug 2024 01:21:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fe856bb7990c2f58d2f7adce976afdc07fb78c53eee84c0b3e49670a25db7c`  
		Last Modified: Tue, 13 Aug 2024 01:21:39 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb261d88fe21b2aa766a64489bfa48537ad4c70425873735ca225ba9c287ea5`  
		Last Modified: Tue, 13 Aug 2024 01:21:47 GMT  
		Size: 98.7 MB (98730910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dc4f7477475b10a51ddb36d4e95c75937aa08cbbe8d91d5886d34c3d38f56e`  
		Last Modified: Tue, 13 Aug 2024 01:21:40 GMT  
		Size: 9.9 KB (9912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aae6ec3e823d2015517414fc0c6edbfcef42ca8eeb57883e17d136d3a10905`  
		Last Modified: Tue, 13 Aug 2024 01:21:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7feb9aaae79a773d51b026cfdb957b71228f6dd7cd6c63674c50c5286ad3cc`  
		Last Modified: Tue, 13 Aug 2024 01:21:40 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8188f195113f410ece4d1e843d0881888b32298031886ad1923909a43795ac`  
		Last Modified: Tue, 13 Aug 2024 01:21:41 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eae44fb420765315631a9786bcae2449e2dc572e9cf13640a4b06441e3e0337`  
		Last Modified: Tue, 13 Aug 2024 01:21:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:91bdb59b5d00da470db41e147b68cb3caf22d2a9442e64402924ffe1bfd7e66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6051033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0d737b4fe28bcab883390c731ccd7c7272a6195f1bcb4c737cfab74d63fc7d`

```dockerfile
```

-	Layers:
	-	`sha256:c2b58f0666fffc9b371d04535ed48c8c124e4a6e46c309dd8145f11388a79a9e`  
		Last Modified: Tue, 13 Aug 2024 01:21:38 GMT  
		Size: 6.0 MB (5996894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef92c17b39506ed8bcc44ee68e8accc3883892a1e9f57d082e41b8594a27b0d`  
		Last Modified: Tue, 13 Aug 2024 01:21:38 GMT  
		Size: 54.1 KB (54139 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:af4bcaefee4c0e3e940abe7357ffb26ce93690944717e9467e486fc3ed2790a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137969930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81958c1ee6c8489848a36ba0fb16dc2f41b05f50f99678cfbd812961b49fcb89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:24 GMT
ADD file:56b9d2d0e0360f64ade3cbe073b446e10c8e6bd253b761c16b5f319a8103d181 in / 
# Mon, 22 Jul 2024 23:57:26 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5b04226d50f1c00a6c8950192ad70a2038016868ab6ffb162ad447e35e67a3cb`  
		Last Modified: Tue, 23 Jul 2024 00:02:06 GMT  
		Size: 28.9 MB (28930588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc751e343fdac6420d03ca6aba7b7203c64f459884877bbda5a9f08cb4562a2`  
		Last Modified: Thu, 08 Aug 2024 19:36:05 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9ad34ad9ea0805efb5831c8fd7352fffebdc7730a8f33e88979aac5cffda36`  
		Last Modified: Thu, 08 Aug 2024 19:36:06 GMT  
		Size: 4.0 MB (3991607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0e2b6fe97724233a2c948d81554a249e031ccbbebf471555d14f939764af64`  
		Last Modified: Thu, 08 Aug 2024 19:36:06 GMT  
		Size: 1.4 MB (1449196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e748d04946305900cc338534ed8baedc7c066d55d6542db003d6f48136d78e`  
		Last Modified: Thu, 08 Aug 2024 19:36:06 GMT  
		Size: 8.0 MB (8044379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ec16bf3b5687c7f7c9ca5456176ef460917e9e423c154cf7647060be441b86`  
		Last Modified: Thu, 08 Aug 2024 19:36:07 GMT  
		Size: 1.0 MB (1034825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a648f7c543f33bf6cee210828f43d0d593b9cd466a8ce9372462f93d4453cab`  
		Last Modified: Thu, 08 Aug 2024 19:36:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dbe19ec3123a5b23efa019792214d8583302c72298c0db655c694a26c7cd05`  
		Last Modified: Thu, 08 Aug 2024 19:36:07 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b574eda73608027b0204e58e9192a006a7a76f8b2109228e880fb899d7c2922f`  
		Last Modified: Thu, 08 Aug 2024 20:10:11 GMT  
		Size: 94.5 MB (94498566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe75d4956668b18bd89dd5c6c9c8c6371a39e06a3954e4c3333aec911568e3`  
		Last Modified: Thu, 08 Aug 2024 20:10:08 GMT  
		Size: 9.9 KB (9928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e076c4d1c6758b71ccfdb45b4e7c0560eacd2d2e35712d3d3d226b75feefb80`  
		Last Modified: Thu, 08 Aug 2024 20:10:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa08abc092bf179b55f6f0d16be527d708db6ba7598e8000379afcf32b642dd0`  
		Last Modified: Thu, 08 Aug 2024 20:10:08 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93c35491701582a9ea2a2535d3198f64d4eb5947fb25ed0b79e9839c415b69e`  
		Last Modified: Thu, 08 Aug 2024 20:10:09 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41039249e4255f0c11a80132e56db77a7992bb10068b831bdbe5e334a071431`  
		Last Modified: Thu, 08 Aug 2024 20:10:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:cf5421391efc4b6ddb5856789fc3b42340bc3c705c00913a50ac40bb6dba06fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6068631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cadd4dc39a325b39aac1aac5b44d293f002d62b293261a989f101f4cc1e092`

```dockerfile
```

-	Layers:
	-	`sha256:a0d5b579df8a288d018ba5e33e154d13fb74114cb8bb91db46d9b722cd4195fe`  
		Last Modified: Thu, 08 Aug 2024 20:10:08 GMT  
		Size: 6.0 MB (6014288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d542c512b9f5358e8a29731fb1cb430dab9ae4a7c9ec7e3d316013e66a4dd7a`  
		Last Modified: Thu, 08 Aug 2024 20:10:07 GMT  
		Size: 54.3 KB (54343 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f7b37195e1f6e3c31ce0c88f9d678a4af711a8fcddcf80e6afad063ab0a22e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133078274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02255fbc96b0594a25b6bad4b75328b7ec9badc08d1be184acd3dff630e5d3dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:30 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Tue, 23 Jul 2024 03:03:30 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38586b406d1175bce94533c1289f9387d030d69502ac6b919088364d88c7d42`  
		Last Modified: Thu, 08 Aug 2024 19:49:30 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6a28b85ad7270ba48736e6d556aaf3a07f463d6c3af709d2128ab0f4b0c5eb`  
		Last Modified: Thu, 08 Aug 2024 19:49:31 GMT  
		Size: 3.6 MB (3601632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e53f3a2f52a512d058ea91cedc199b09ddc0582c146e0f39357d8f792830f70`  
		Last Modified: Thu, 08 Aug 2024 19:49:31 GMT  
		Size: 1.4 MB (1439216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eade04358061f1f5dea64022212c4785136d407ba3db976ebb5f5644eeb3535a`  
		Last Modified: Thu, 08 Aug 2024 19:49:31 GMT  
		Size: 8.0 MB (8044431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20259319c8168bd6130b3aed2bc975a6dd59098bece8f40a3d1490f3a6e5468d`  
		Last Modified: Thu, 08 Aug 2024 19:49:32 GMT  
		Size: 908.6 KB (908648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d2fce58d7cd7c1ff5cf3fecbeb1ad21607c81b676b72726af2d9e67cc10bd`  
		Last Modified: Thu, 08 Aug 2024 19:49:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a54a07bb72d0752936184e53bd07a844452c85cb35fbe5ffb968feba7f5665`  
		Last Modified: Thu, 08 Aug 2024 19:49:32 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031f33c143705131df0d4646a2e00f4fb44be8e2e832f22a3cf07649c2eab4e3`  
		Last Modified: Thu, 08 Aug 2024 20:29:13 GMT  
		Size: 92.5 MB (92474456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dba0f016989acd354544d3ebcef75e06c0895737bc4c3e02b20884ae9f68b89`  
		Last Modified: Thu, 08 Aug 2024 20:29:10 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076b7cf615f02978b7f974ea7834f5e50f7ae579a370d9f540c78733927bf998`  
		Last Modified: Thu, 08 Aug 2024 20:29:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaa17a3553a8099fca57c212c2a1fd79b0187155888b8409911b59812c56511`  
		Last Modified: Thu, 08 Aug 2024 20:29:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7e5495e1623ab42077ce5f698beb63a2423f8ec6bdcbdcd3aacbb0175b36bf`  
		Last Modified: Thu, 08 Aug 2024 20:29:11 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5cf8338a01e8e61de7e0e2800b1ef98816b5e8653270df3dd7da46f8577202b`  
		Last Modified: Thu, 08 Aug 2024 20:29:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c4ba2a7cb0169760d095812cc9d1a1331943114e02c22d9c1dfa3a64260974e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6068253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f20e4e81c7d94302339b724d9ea0be3e7f33d0e23e4f8b42e9bbc318607d67b`

```dockerfile
```

-	Layers:
	-	`sha256:c8a36aa799e5509f21da952014ece6dbe764275e400ddd156f6927e46b4f5047`  
		Last Modified: Thu, 08 Aug 2024 20:29:10 GMT  
		Size: 6.0 MB (6013917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79ad5685c000832a450520fb33acac6d34534fad7527b552689938a2704839ce`  
		Last Modified: Thu, 08 Aug 2024 20:29:09 GMT  
		Size: 54.3 KB (54336 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:918a0f7a665d0acec7ece85254c0ec1553bd956b65a01b3e4ff5c6cecf4e80c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141430877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b750a0dbf190f6b0bce3ad0acb9ab454500fa0ce986492eb16f6584b30694d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309ca2cf1b25840e628e60904222bb263015d45a8b9bcaf63173b00d0be8b17e`  
		Last Modified: Thu, 08 Aug 2024 19:12:27 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983150f419761397f47a4fbaf44ab524b5d5954109b24801ccb9954e3e0c78db`  
		Last Modified: Thu, 08 Aug 2024 19:12:28 GMT  
		Size: 4.3 MB (4312718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a715785956281410724cd8c90a7ae85a63bc6e0b0f8f2a21d0223269d8a16222`  
		Last Modified: Thu, 08 Aug 2024 19:12:28 GMT  
		Size: 1.4 MB (1404104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327d4ed77f4da5adca0f374aea3febfa084fb2e142f780a51470532dc01f9e47`  
		Last Modified: Thu, 08 Aug 2024 19:12:28 GMT  
		Size: 8.0 MB (8044438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaea14ef4e48f9e2f6398ded3fb1f9cc3dec41a047f90cc1a504d48256a2047b`  
		Last Modified: Thu, 08 Aug 2024 19:12:29 GMT  
		Size: 1.0 MB (1026583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709addd730f5c48c130fbbd846c5109e72ffaf942c489b38589e8137d8c4b6e4`  
		Last Modified: Thu, 08 Aug 2024 19:12:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3662dce6c42f2378c996f3ab98d67d5be50f100770db5c76cfc7a8bb0c19bf`  
		Last Modified: Thu, 08 Aug 2024 19:12:29 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fe8e67c5416f0d5ab45edaa9db585ef122e9854a450955193b12e82fdbbbbd`  
		Last Modified: Thu, 08 Aug 2024 19:20:56 GMT  
		Size: 96.5 MB (96546186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba89da6efa7eeb6d2347bd4ca9fff58d95df03c1041882d2bd71cdb2ab50f716`  
		Last Modified: Thu, 08 Aug 2024 19:20:53 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c19502d651e6356b1aed039f095263ed141c5424bfd62205dde87b6632fa70`  
		Last Modified: Thu, 08 Aug 2024 19:20:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d100bc1b5abe575890428a71097ac507517c95e2e2bf138db412bbaf7c37c9`  
		Last Modified: Thu, 08 Aug 2024 19:20:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09ae052c38e1a2ff9fce3a52e820b98b7d11d7e14525eafbbb0c8ea2623b9b5`  
		Last Modified: Thu, 08 Aug 2024 19:20:54 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9944b6fb1ec36add36355028fc70dab27a0eb7a643ac12b6e669c62677287690`  
		Last Modified: Thu, 08 Aug 2024 19:20:54 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:f08cb665a1634ea246e82c90bfcac15c2a392fc662902f3c99427afec2578766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6057633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7181610ceb63f706e25e865cb236751a0f100dbf7546ced93d9ba59f992cc8`

```dockerfile
```

-	Layers:
	-	`sha256:e0910e81114c6daba00cb64e9d643aa99dfe50bd9a56ed5eb32a4d97ab3f0238`  
		Last Modified: Thu, 08 Aug 2024 19:20:53 GMT  
		Size: 6.0 MB (6003196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bb8e01ba8e681d5a55c8242f28168a3ebfac7ac7662e0fb6521962af347545d`  
		Last Modified: Thu, 08 Aug 2024 19:20:53 GMT  
		Size: 54.4 KB (54437 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:1087cd0783f57aa13d07fe83bddd9f9451601ec35bc7aa314d358044b5a4989f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147772563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383b7eec4b10f0aa10b34cb0d189bdbc2074047cd4786e2fd15328f776f1dfe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 17:20:28 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3c46da0c94d263a1be67d16e9839f90bb11fe96eed063e74237a1d04f10a0b`  
		Last Modified: Tue, 13 Aug 2024 01:34:00 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037e524836ced04b40de57f965d3c60adf8163795e747d5ef7010b1d84d90ba3`  
		Last Modified: Tue, 13 Aug 2024 01:34:00 GMT  
		Size: 4.7 MB (4719624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322dde7b7f78e2b22b3fb335e6285a3e930a84cdd4bc07b713919d58b5198c5d`  
		Last Modified: Tue, 13 Aug 2024 01:34:00 GMT  
		Size: 1.4 MB (1447770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3a04eb23775b119d5ecaedc2421e4b2a722f50cd3fe92d6876183f1ac890f5`  
		Last Modified: Tue, 13 Aug 2024 01:34:01 GMT  
		Size: 8.0 MB (8044373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bfba397aed253d3014b00898f2c8aa34e7eb26cfdb99d7ef972537556dc78b`  
		Last Modified: Tue, 13 Aug 2024 01:34:01 GMT  
		Size: 1.0 MB (1028909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788dfb3b8ad46348788b755608d20f8b5375a49d13854f7e21975c6f5bc2a217`  
		Last Modified: Tue, 13 Aug 2024 01:34:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a9a8992d535a128b24de8e92003c61b7a961341a35c4dd35156b16a3c42aae`  
		Last Modified: Tue, 13 Aug 2024 01:34:02 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7902aa6d4c6f029756ca6cdb954ddc0d82eba855853e0992f2cc7ce3cc80f3`  
		Last Modified: Tue, 13 Aug 2024 01:34:04 GMT  
		Size: 100.1 MB (100097343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d40319813b6977a2751f576b32d4623867c4bf9f2ae90823c4f64e67d70e0`  
		Last Modified: Tue, 13 Aug 2024 01:34:02 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537da48fb298e5b2d2f4fd560ccc15404365264dbb4079a0ed5358545220a4c4`  
		Last Modified: Tue, 13 Aug 2024 01:34:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e9c11eb71afc0443bbbf74df8cd4ae9963668a508e3a8a5d74be17cf26b20d`  
		Last Modified: Tue, 13 Aug 2024 01:34:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3230dd74ba51a2714f791bba10e0ca465def53126d0a6d19eb3b1d0ec991d5fc`  
		Last Modified: Tue, 13 Aug 2024 01:34:04 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8929eb0fa709efdfe6b1361b8f09affe3cb38e23e66989413dcda590a657256`  
		Last Modified: Tue, 13 Aug 2024 01:34:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:95d888a5b406c17483e54ae37296780dec94a7f1e4cb1ecfa5d5f9d562d5e285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6065695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525f384f4500ac510e49cd3d328fc5c32fb45c68124806914c1c5e18d467d2f0`

```dockerfile
```

-	Layers:
	-	`sha256:739b0a7becad8c24039cefcd046ab41032d29a22be4ff6add4576f979136abc1`  
		Last Modified: Tue, 13 Aug 2024 01:34:00 GMT  
		Size: 6.0 MB (6011595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd297ba8e8a4a5a11b1f5b13358a09be2c18ea7c2e1ebd623afb3539166aa5cf`  
		Last Modified: Tue, 13 Aug 2024 01:34:00 GMT  
		Size: 54.1 KB (54100 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:6270eb42040dc74de9e77295e50d67cfa9fba609232a35d306da2026b84a02d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139374012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1abde574112a8b97ec837e1b0ed7fe6d489e48c8b411c30c1af8c64cb6b725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 00:39:10 GMT
ADD file:aa937b31fe693810c8c6e110de59ba07264dbc020fabac9e1ac045df57efc0c3 in / 
# Tue, 23 Jul 2024 00:39:15 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83b27ea307774a387b0a5203cb6aa8f117e44bb5321ed6c8de8b0a0c43d895ca`  
		Last Modified: Tue, 23 Jul 2024 00:50:32 GMT  
		Size: 29.6 MB (29646085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c212a741d5916a3a66b0aaacae2f58fe4cc5b8cbca99c126ee3fab02b159446`  
		Last Modified: Thu, 08 Aug 2024 21:26:02 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761d4d319c5ad548ac64adb44ee679e9a43b4d1f852605d8095d34741ee2da01`  
		Last Modified: Thu, 08 Aug 2024 21:26:03 GMT  
		Size: 4.3 MB (4308273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac7f92f95bf9a849c2748b8cdb90a7fdb16badaffc8a6510195054fe4993b14`  
		Last Modified: Thu, 08 Aug 2024 21:26:02 GMT  
		Size: 1.4 MB (1359322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d567d541c1f3892b82118ed629d4a7e32814045df3cf9396110a9d3888197a2`  
		Last Modified: Thu, 08 Aug 2024 21:26:03 GMT  
		Size: 8.0 MB (8044861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6405c1cb12d9f460f4e8a41e2f82aef57708cd8578ebe94174d6acfb1431ba6`  
		Last Modified: Thu, 08 Aug 2024 21:26:03 GMT  
		Size: 1.1 MB (1090282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f7a983b9adbe231e5f9eda03e3ddcd998ddf345e67cfc32a9459593b3c0c64`  
		Last Modified: Thu, 08 Aug 2024 21:26:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e9aa86eec75c3d79b85b9218409659c7f29712ab4679b05c5e3dee3f780d80`  
		Last Modified: Thu, 08 Aug 2024 21:26:04 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5891ee3ddb92c8aff3ba36cd670ba70a123d8b5203f122fa96d6de2d320cfc7`  
		Last Modified: Thu, 08 Aug 2024 23:44:23 GMT  
		Size: 94.9 MB (94904408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e61dc53848b09df94e18cb710fb93c79e85ca99a6718b4ddbe669442942bd`  
		Last Modified: Thu, 08 Aug 2024 23:44:14 GMT  
		Size: 9.9 KB (9931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a73c178fb31249412033eba0db5783c76c2ea430bd98c9e42ccd840ce4b9f53`  
		Last Modified: Thu, 08 Aug 2024 23:44:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d9e5a7b175c1cdeacbc62f27d4f2a54c417066a75bca6faf12d394604d567d`  
		Last Modified: Thu, 08 Aug 2024 23:44:14 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4206482df649b097535e0b085d201c6d9f9b0ad41b872d730137536b14e8c0`  
		Last Modified: Thu, 08 Aug 2024 23:44:15 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ceadb037e2b00e7bf81fb7e4dc514cf00b2922bd39da7a456926bc79711a73`  
		Last Modified: Thu, 08 Aug 2024 23:44:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d6c983478ddc0f9f86a8bf68678dd4d11a4ea0fe4706ac58ab3bcb3aab34bfa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 KB (54002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac855794189fe79974ebad8fe2f933d7889297ab688d4f07f1ec31bd0f85d2bc`

```dockerfile
```

-	Layers:
	-	`sha256:e022b3af56198a7e681e4454d845c8976d47ac347782e5e539fb9bb7a8b6438b`  
		Last Modified: Thu, 08 Aug 2024 23:44:14 GMT  
		Size: 54.0 KB (54002 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:a6332a7af8945867c296f868a06bc4c453c1b09177965c9844badb021eb9d29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156026461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a33d9ca5b4e65d2304ae15809e8d751c26fe5ea973095845149b433125ebb54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f5dfe246b83efb45af1ebdb6da492980cbd513f847d4df0cb90c3ee357f0af`  
		Last Modified: Thu, 08 Aug 2024 19:23:29 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eed4557a01721adf4eb30591e2dc8a4dd5a8a560b47464215f0cbdc0bbe811d`  
		Last Modified: Thu, 08 Aug 2024 19:23:30 GMT  
		Size: 5.1 MB (5137833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94408b0af187f60a58f09a29802bd98f8f69ab1fa550790fa9c39d52c87d39ed`  
		Last Modified: Thu, 08 Aug 2024 19:23:30 GMT  
		Size: 1.4 MB (1393666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc64e2d374a2bc96a75deb9e57283e98d5bbf5a481099d4be71b2a3f684bf750`  
		Last Modified: Thu, 08 Aug 2024 19:23:31 GMT  
		Size: 8.0 MB (8044634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b683947c64460b26449cbc4e2b52ee4fc2980cab15b338153dd6f16d3d886060`  
		Last Modified: Thu, 08 Aug 2024 19:23:31 GMT  
		Size: 1.2 MB (1197604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6633ed72e8f9a7976068da2f18cf68b2f4656033a559eebafc37c18a940f9a0a`  
		Last Modified: Thu, 08 Aug 2024 19:23:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15abf089b8f264eb3c9159b9a91d7d2b882cb2e7412bc07d92dc4639b415f3e`  
		Last Modified: Thu, 08 Aug 2024 19:23:31 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dfe45256b24a271045df3d0fb71ff45d6e7dbdd64c5fe435feca828291dc84`  
		Last Modified: Thu, 08 Aug 2024 19:34:16 GMT  
		Size: 104.9 MB (104926757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddd313f3da6c7e9f758d884bf217bd84b892014f84a46b6b982e622109d22a4`  
		Last Modified: Thu, 08 Aug 2024 19:34:13 GMT  
		Size: 9.9 KB (9916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fffc791de9807af849a1d4170f026a05bd808fbf838e249208de6db3ea625c5`  
		Last Modified: Thu, 08 Aug 2024 19:34:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a267d4cc5bad61e49293f686cba9f4eaff94cd57992aa2435cfb2a9556430673`  
		Last Modified: Thu, 08 Aug 2024 19:34:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e605167bd5a7c113be4c8a87df4c34583513493d3ff16c5fe8439f7c4a0eb84`  
		Last Modified: Thu, 08 Aug 2024 19:34:14 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c92d95552249ddc435ba6831511f38297b4eb9c34489052e7635628aba118f`  
		Last Modified: Thu, 08 Aug 2024 19:34:14 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:64fec2530ecb9088675c654b6b1a913bad03dcb700fc26536d39a95ba7cae1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903da4a543f19a8311dc276f8064294b0afd93d939914c30cba6674ab4be7222`

```dockerfile
```

-	Layers:
	-	`sha256:c34911f9a11f1674ac9af58405eec40bd5c9d81e89d679477069abfc07854049`  
		Last Modified: Thu, 08 Aug 2024 19:34:12 GMT  
		Size: 6.0 MB (6004032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60887ea0dcc3b651c02c913c1dcf88e0686ee0d841f8306ef0b134116e1f8260`  
		Last Modified: Thu, 08 Aug 2024 19:34:12 GMT  
		Size: 54.2 KB (54200 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:26b623ce6efc09a7243b07d90bed9281f80dc0a1052e333f59e007986464411b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149430880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9d459216ab543298cb9c644ef7689a68e2430a6903b5311fc43177126ebabb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:25 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
# Tue, 23 Jul 2024 02:28:26 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_MAJOR=16
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PG_VERSION=16.4-1.pgdg110+1
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 17:20:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 17:20:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 17:20:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 17:20:28 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 17:20:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 17:20:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:de4a305fc1af45cc7ae97020dfe639e8990f6d00b7e0ef222c4cdd720f0fc373`  
		Last Modified: Tue, 23 Jul 2024 02:33:12 GMT  
		Size: 29.7 MB (29669018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14257ede12b72a53fb9f923c5c46affdde160049b18ae4ec0bb2d779a42623aa`  
		Last Modified: Thu, 08 Aug 2024 19:20:12 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6306c74c3258778a9c08bda7d1a349499603fb8e15a3587b67ade668205add`  
		Last Modified: Thu, 08 Aug 2024 19:20:12 GMT  
		Size: 4.2 MB (4200304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1736efec3ce64cf78b850741c6111eeb0f41f0b5dc9160cac45d24df5c25f99a`  
		Last Modified: Thu, 08 Aug 2024 19:20:12 GMT  
		Size: 1.4 MB (1438006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d689e6b0f800c918821c4697907bf64a17d0267475185937cd80b9b2b763c7`  
		Last Modified: Thu, 08 Aug 2024 19:20:13 GMT  
		Size: 8.1 MB (8098794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88be6225715070b96de4f7ee5bedc608cb9548da5606d13f0b4cd917eb2d7a36`  
		Last Modified: Thu, 08 Aug 2024 19:20:13 GMT  
		Size: 1.0 MB (1015253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd020af405c05cb57de7e7fb0a104d22d2e25b3b1ecec8234b00d8b3e759797`  
		Last Modified: Thu, 08 Aug 2024 19:20:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28002d62da530efdcc989be51edde86250c6a154c882fe66b340d0d01f80b20`  
		Last Modified: Thu, 08 Aug 2024 19:20:13 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98c7d363bf56dc0e54b175fb29e4987132120f2ca28fb52bbab1d85d68461ce`  
		Last Modified: Thu, 08 Aug 2024 19:47:10 GMT  
		Size: 105.0 MB (104988737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333b1b3c5139ce87d5578ca795a8ddb1a0e4a6abecc44995da0f30274ddece99`  
		Last Modified: Thu, 08 Aug 2024 19:47:08 GMT  
		Size: 9.9 KB (9916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cd2d83b512c50b87d1b0bf1c1a9f0d91ccf42932dfdc6c594c36601e82a499`  
		Last Modified: Thu, 08 Aug 2024 19:47:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcd798f5390e90d0eea8afd6fd48b91c5f7e30047eed9954a3b102df8ab30fe`  
		Last Modified: Thu, 08 Aug 2024 19:47:08 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb387ab899eceb12b6a8c2bf83cfce2f61768b6bcdacfaf09da5349db0a4106`  
		Last Modified: Thu, 08 Aug 2024 19:47:09 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10cbd121be0527d2dc0d96aab0af108b01b7793b97a3d03199464e734f43e4`  
		Last Modified: Thu, 08 Aug 2024 19:47:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b801a92dd4e4e11bf53b9c269265ef22a49f78f63322350d175ef6bf77e7b0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6050017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0debb46b609569689410ed695c938d479f8c2bf58e0052efba61a78f19ac633e`

```dockerfile
```

-	Layers:
	-	`sha256:f11e3c220d47f373a457d49a0e6bb6b49a32ac49ef537424ce267098907411d1`  
		Last Modified: Thu, 08 Aug 2024 19:47:07 GMT  
		Size: 6.0 MB (5995871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e56f0ba90418dace0fb717b7a0b2bd07c8f043532a1a500ad4807f83ef1b6da`  
		Last Modified: Thu, 08 Aug 2024 19:47:07 GMT  
		Size: 54.1 KB (54146 bytes)  
		MIME: application/vnd.in-toto+json
