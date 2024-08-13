## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:b6ca52c34674311d3514d7fc6810e96132e32bb12ae0c504bb6c730f2546f1fe
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

### `postgres:14-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:95c6dbe36bbe193c1eedcbed98a643cc5b92295a20f4c768d1335ecab39114d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141780285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8631df12d463f5d1638b60d9e6700c7af3829c23640e49c0ab3e3ae15ee1458`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6836cc443a423a15f871d8f3a9a8d2a81ad2c15d88b69fb6e794ead69909c9`  
		Last Modified: Tue, 13 Aug 2024 01:21:48 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adc7c1370c17f14e9130546de21129358eadf0edbe1c71f624d1eb98b0776ca`  
		Last Modified: Tue, 13 Aug 2024 01:21:49 GMT  
		Size: 4.3 MB (4308154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73d1083100da73d930fe438037208ba1c819fba092e0ea2f09b213d1a403ea`  
		Last Modified: Tue, 13 Aug 2024 01:21:49 GMT  
		Size: 1.5 MB (1472175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7445cae8f83dcddfdd5c3ded55b169f8bfe7c74f9c1b9468b2d950158716d4ee`  
		Last Modified: Tue, 13 Aug 2024 01:21:49 GMT  
		Size: 8.0 MB (8044453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a04b097b75f96bc8349311e38cbb42b6aca97d493c1c7ff519b2776337d160`  
		Last Modified: Tue, 13 Aug 2024 01:21:49 GMT  
		Size: 1.0 MB (1038349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e216b5a78d11eaf0fe546d913882cf2360363bd6fd2ac3fc1d129eb8ec39075`  
		Last Modified: Tue, 13 Aug 2024 01:21:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d170699dc2fcc5be71720beec0d2daa30156128451c345953a2b244d41b3120a`  
		Last Modified: Tue, 13 Aug 2024 01:21:50 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70925a2b5a847e48977c0cdc4d0aaa6d4d7f216f3adb4432a7c263789bfde857`  
		Last Modified: Tue, 13 Aug 2024 01:21:51 GMT  
		Size: 95.5 MB (95468508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699b2f89b466033a65fcdbe2c7282df03a6ba72c84c07e7ff9e2bea7be45d813`  
		Last Modified: Tue, 13 Aug 2024 01:21:50 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe665e64168b14828ed5fcd3c6c043abf1956802011013fee8e20793bdc5460`  
		Last Modified: Tue, 13 Aug 2024 01:21:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb909071756c96c2c8ba688b485f9de859f500f15fc113a34e1540cef2f69933`  
		Last Modified: Tue, 13 Aug 2024 01:21:50 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce2e69012d44fe222a28f170dbd7273f5400140319bb73ee3247010874ab2b2`  
		Last Modified: Tue, 13 Aug 2024 01:21:51 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae38a72cd5ebd68232934f534e8a1ebf057c01cd3fa92b77579f12a5e7422f1`  
		Last Modified: Tue, 13 Aug 2024 01:21:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:3d29de3f5c6ac05c186ebc06769231ade683ec6c885193fac0383bde5ea3d9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181741e102419062c398f6bb4cc54607b3f6cea5b9d8522370713b05871101af`

```dockerfile
```

-	Layers:
	-	`sha256:ee0f5f13d275943efebfeceb6d03dc2c5c7388d0fc08fcd6e886b985b677d586`  
		Last Modified: Tue, 13 Aug 2024 01:21:49 GMT  
		Size: 5.9 MB (5882243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd47a1e1c3b02aac91c87324858cbffe4b4c0eff65527bba2b1a7af73043d3c`  
		Last Modified: Tue, 13 Aug 2024 01:21:49 GMT  
		Size: 53.8 KB (53841 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:77c55b5fd26e6b2dec7bf3f929b49141a53d08c0268a10959cffa4f44f567942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134622013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee38748ac35516c636d19f916ac454239edfedcea6742315e94ba9539175816`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:24 GMT
ADD file:56b9d2d0e0360f64ade3cbe073b446e10c8e6bd253b761c16b5f319a8103d181 in / 
# Mon, 22 Jul 2024 23:57:26 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
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
	-	`sha256:b420fce592aa8c3f2470dc6e051e366a1db8fa18529862010e2b83de585c8e7f`  
		Last Modified: Thu, 08 Aug 2024 21:12:09 GMT  
		Size: 91.2 MB (91151036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5003f5b1b40bc6feeec5afc23a9fa2703abaa9d477f8a91a621d932c9bc4904d`  
		Last Modified: Thu, 08 Aug 2024 21:12:06 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d71c68e477278fc788090cdbe096d28cd1b52bfab2376f0b84f21bf10cea397`  
		Last Modified: Thu, 08 Aug 2024 21:12:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0c0635fc551d1eb4e2010210084956fc611c77f454744b74460f2eed72be3d`  
		Last Modified: Thu, 08 Aug 2024 21:12:06 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50d22c07aee3feee3482d5b269c35c1911a2436313d5c4f5f5785cc4b7c2547`  
		Last Modified: Thu, 08 Aug 2024 21:12:07 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa78a4d72f7b7adc7772389471f9ec3d534a19615b1a37d9bc3be7986f41f76`  
		Last Modified: Thu, 08 Aug 2024 21:12:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:9515c9e1c22e0e3a1ce62103a6808cda2e5d54f3bd14521d593680dab7a9e20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dacd513084337ed028fcb44ea48febc4cc929a2976832852b1f41982eb0da13`

```dockerfile
```

-	Layers:
	-	`sha256:c4c7c2508155b1c77b9c8eaaf6ec0046fd0dca7ac6e6d620981205683e12434f`  
		Last Modified: Thu, 08 Aug 2024 21:12:06 GMT  
		Size: 5.9 MB (5892231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c05ea58c598452c31438a615404c73f715fc6fe101d1e06e48cda52d377abc5`  
		Last Modified: Thu, 08 Aug 2024 21:12:05 GMT  
		Size: 54.0 KB (54038 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:4c2751984b61c8fb3ddee06f82889bbf390e0f4e2b5163e3c0ed291969770226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129750239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e357b6f2213a95fedbc34c269cdc6c85ee56fcc0cf15830e5cfae07953a5d01f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:30 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Tue, 23 Jul 2024 03:03:30 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
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
	-	`sha256:1fbc7a8b444971bcf51a7118df8da3921ffd6f5959122abe06e45c91eba909a3`  
		Last Modified: Thu, 08 Aug 2024 21:40:59 GMT  
		Size: 89.1 MB (89146809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf160d15ca759216723988857a9eaa70c6d239a1ecccca4f7ee3ffe535549e2e`  
		Last Modified: Thu, 08 Aug 2024 21:40:57 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd20c02d5d4f69bc8375e2225bf80f12b58aa2c1fec7febb3dde971e9df64f0a`  
		Last Modified: Thu, 08 Aug 2024 21:40:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299895478eff919b2745db4c74f7241467aeb7b93e5ce5d3ef7ab82e79519905`  
		Last Modified: Thu, 08 Aug 2024 21:40:57 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038c1b715cc0d60f88b2b0fa6df1b255d601c89b19884150c7ae80a14cab7fa5`  
		Last Modified: Thu, 08 Aug 2024 21:40:57 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc5e515874b7286235cb9e403d95e0e4bb6396648a811cfa4963c3fb49d011a`  
		Last Modified: Thu, 08 Aug 2024 21:40:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:f9bdebcd139a84fb1fddc4f11093b9d503a8391a3a9b6c4cc8e68dcf14cd64de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9b97e22551fe748e5c68f56faa9614e5c592298335c9f2d65d193adcf1fbbf`

```dockerfile
```

-	Layers:
	-	`sha256:82cf1f6d84ba26dea5f365afb20165528f30e5603fbaeacccb9edf70719bda9e`  
		Last Modified: Thu, 08 Aug 2024 21:40:57 GMT  
		Size: 5.9 MB (5891860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c4b8b2745a841503c69f0174c2a1f6a12e05e3cd8e784b25ced01496bb8890b`  
		Last Modified: Thu, 08 Aug 2024 21:40:56 GMT  
		Size: 54.0 KB (54029 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3deeb8e71874a5844a8b7a84cf7a4dec20f2ce313dafeab3f9b8fd2692acc0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138187967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76daf0bfe509055701cff5bf37790c564b21faa798c9bb853d4fd74b8b9a3989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
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
	-	`sha256:343fb90cf09c979f36f524dcb3ce1b40b113b3ab657d62d4937dfc98a926957f`  
		Last Modified: Thu, 08 Aug 2024 19:37:42 GMT  
		Size: 93.3 MB (93303662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca29e1083d611d58d43aacde2917a3713537ad7320b45ddcd5ad56b94719fed3`  
		Last Modified: Thu, 08 Aug 2024 19:37:39 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de208cdbde8a8c8a2043789cd08e67ffed6ee0162a5ebed4d6a035c93828e82d`  
		Last Modified: Thu, 08 Aug 2024 19:37:39 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669fd2afb2315d698581dfb03fbb5319740de079b08cd046dd2d232310cb6214`  
		Last Modified: Thu, 08 Aug 2024 19:37:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f805b7a7b81cbe511239d5625809a6c30fa0b46db70ac3667a9efa78d9863b40`  
		Last Modified: Thu, 08 Aug 2024 19:37:40 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee25207b5e38a41e421a76e6f661253a342cab763b978a5dab96e599428348f7`  
		Last Modified: Thu, 08 Aug 2024 19:37:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:1b5d34fd5e8ebb582871e26d841a1f970512c6ba6c18cb3d29af1f9c62d7b6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab02db0e43ca452034524fa79dacb3cd9778c31976bb7e909e8e6a0d5b3fb8f8`

```dockerfile
```

-	Layers:
	-	`sha256:5d54e2af01974270178b56520f6bfe90d4b93470029c80592cacc8c2eb46fba7`  
		Last Modified: Thu, 08 Aug 2024 19:37:40 GMT  
		Size: 5.9 MB (5888533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:696528115534fe056d8fb15e532f34b9ffb397c360231d8b9c36821ad57b1b0f`  
		Last Modified: Thu, 08 Aug 2024 19:37:39 GMT  
		Size: 54.1 KB (54126 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:9d7ab1f7a74d00ae269ba6f994da6a515017fa72fc8cede978d6ad078c058ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144372713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5305139145ec5de69b932a425ba3a2468193e4a56160c8ba1bc82f392fbdb2d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 Aug 2024 16:52:20 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcbe782b246f9905dcf25007a6ce7a8c47b6740606114d5f068efcb3640c7de`  
		Last Modified: Tue, 13 Aug 2024 01:33:29 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b550e29a0f1a194c81d20b18dd4273c5fc2f6db85fa2f07956a50c15671935`  
		Last Modified: Tue, 13 Aug 2024 01:33:29 GMT  
		Size: 4.7 MB (4719644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9985d521e3a62f45e9fa4e5b6807a488952443347c0782d15c279f2347c9a491`  
		Last Modified: Tue, 13 Aug 2024 01:33:29 GMT  
		Size: 1.4 MB (1447768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733eeca3d8ae590ba6acd3e263397dbdeee97b874592cc3ce132dcaad4811c24`  
		Last Modified: Tue, 13 Aug 2024 01:33:29 GMT  
		Size: 8.0 MB (8044350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfe77c9a4dd5cdf0618f7217dce76680b6921f85ff96d38768cbb7235158809`  
		Last Modified: Tue, 13 Aug 2024 01:33:30 GMT  
		Size: 1.0 MB (1028891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5897c0282d64c3252b92000f41e1c49cb9fbe3b714f68e60e3e6231256a568`  
		Last Modified: Tue, 13 Aug 2024 01:33:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0d73a967c2cadee8c0348829da22f35a31338deee75ec08ae90aae49a89e23`  
		Last Modified: Tue, 13 Aug 2024 01:33:30 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b87d8eb08fb4aaed141b8e67b49ed8ddffaa853a265d7f4205832deff07751`  
		Last Modified: Tue, 13 Aug 2024 01:33:34 GMT  
		Size: 96.7 MB (96697907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5492551a27db4e171602459c40659a74df099e203f2a56a33181da61a53b6a72`  
		Last Modified: Tue, 13 Aug 2024 01:33:31 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f1c3ed25c59422334b15ca60152b621a051120aa95e7a6bcc3a497e4d8984`  
		Last Modified: Tue, 13 Aug 2024 01:33:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd4282a64744ebbf806298c8b7621de9cb2d807600d99df0db9d1b6f1cab554`  
		Last Modified: Tue, 13 Aug 2024 01:33:31 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1867ee4070bc4729bd27028959fe4717898285d8fd81b8b64b7e88e9cd151710`  
		Last Modified: Tue, 13 Aug 2024 01:33:32 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907e38f769785a9006e7a29b0446a3bf938c23d04c82a1df519881f9e4d4767c`  
		Last Modified: Tue, 13 Aug 2024 01:33:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:626cf88ca0ca3a9ddc67f0fe89ad22868b23f8c9fdbb2e3a442b777cc7a2ea69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5943351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362e830162af3a83a6592ba42f8b7ce3cc05f41bd8a28c0cc3f7909b215054fa`

```dockerfile
```

-	Layers:
	-	`sha256:1d670137e0b3ffaa64070dd9922e7cd070c39ea586d0f6a95fba6b0a95087a83`  
		Last Modified: Tue, 13 Aug 2024 01:33:29 GMT  
		Size: 5.9 MB (5889551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea53d8209b1604d6f007dc4d0be46eeb9d5dd8faa45b210c2ddabd70c03c4ea`  
		Last Modified: Tue, 13 Aug 2024 01:33:29 GMT  
		Size: 53.8 KB (53800 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:01aa789d6d86b5a97e8dad4af9a5d566deb277a6d9abc9768f922f883f2724ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (136042466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e041b4383ec34f6ff5433234633c805d6bbc9809e34257330c3f4dad47567e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 00:39:10 GMT
ADD file:aa937b31fe693810c8c6e110de59ba07264dbc020fabac9e1ac045df57efc0c3 in / 
# Tue, 23 Jul 2024 00:39:15 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
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
	-	`sha256:b79f540004d53e92807db475622515d3996607dd3ff33dfaefe9867773f58f28`  
		Last Modified: Fri, 09 Aug 2024 04:07:31 GMT  
		Size: 91.6 MB (91573258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93bb9110d83c9ab4319f83da1d3e24314c35b092878bdc875b51389c90b6e59`  
		Last Modified: Fri, 09 Aug 2024 04:07:22 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c91acbde0d1aced1c608221d451f134f704742c75844a23705eb257a68c72e`  
		Last Modified: Fri, 09 Aug 2024 04:07:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0b9d90f4834127bf5e95ba8dd83ed8c7c1685898d51b5840276f9df6b9c7f`  
		Last Modified: Fri, 09 Aug 2024 04:07:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704714dd2fc45ae756a9981944f02c61d279f3a3760d94bf3c1d869c05555ce2`  
		Last Modified: Fri, 09 Aug 2024 04:07:23 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf038cea8a82516097719cbbab5543f563abbe6cafc7b756c0a9677b7df9c37`  
		Last Modified: Fri, 09 Aug 2024 04:07:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d1cf4b57ec52c6cf7a63b2fa7c9cdbc8e1f41a01bf4ee0a36f15a7b6bd4f0a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 KB (53694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5129c0728d0484bec49f67e40ba76ee84be76b174ca9188dde7a1b85a955029d`

```dockerfile
```

-	Layers:
	-	`sha256:edbd51dc35cbd30ae31885f0fc288d4c21588e1e47883d0b12a3b0b4e6db8591`  
		Last Modified: Fri, 09 Aug 2024 04:07:21 GMT  
		Size: 53.7 KB (53694 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:6ef39bd685ab67cbcef01558ceed6828d217f71c6c0e56c974f6e5156fc74536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152698041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071b9abc516b63461e8f5023aa7b8860255a015aedea69f81bf56ad1bcb40f67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
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
	-	`sha256:8379e466e46c4e2b0561d4ed38daca945957ff29fb0af683a644cb2d50be060f`  
		Last Modified: Thu, 08 Aug 2024 19:53:28 GMT  
		Size: 101.6 MB (101598715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a81a92e151f1708d4bc32cd2e0a5cc194eb86df574bf004bbd0a671a6e6dce`  
		Last Modified: Thu, 08 Aug 2024 19:53:24 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b030a5654a0b90de364a222c008bf190abbcc19ebc90fe96b1a160e94ba3ce4`  
		Last Modified: Thu, 08 Aug 2024 19:53:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8747a999cc1a53bcdba9dc61702edcb9f13fa7f7ed8b0216d88e16c005e8ff4e`  
		Last Modified: Thu, 08 Aug 2024 19:53:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f45b86e1801aeeaf737c5eda6e401bcb8d8ddbd3232980650434f44ccaf3271`  
		Last Modified: Thu, 08 Aug 2024 19:53:25 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f92e32fd6d7490c2e256f4c8df2a72f85045c02030e334ff570d39f8fec5313`  
		Last Modified: Thu, 08 Aug 2024 19:53:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:eacc84e460918aa45716a7de4b9a09d60f5686395f005fe43090b13075024e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5943269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87811d5d011d31b3bf76cfe9af22fabc81ddf425042e0d19e715a6eae8e44f20`

```dockerfile
```

-	Layers:
	-	`sha256:b2769bb1ad9ed85b2f251de7f206426350a9c3baf50f30afd0e7fecc2f6efd7e`  
		Last Modified: Thu, 08 Aug 2024 19:53:25 GMT  
		Size: 5.9 MB (5889375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3128866b9bedc3684b230e2a8359cfe3c622961c263c677f90f00b0dd77e66`  
		Last Modified: Thu, 08 Aug 2024 19:53:25 GMT  
		Size: 53.9 KB (53894 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:30e6335f10ed5108d58610ba9940f074dbf51e0ffaad5715e17ce42265d1c920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146190774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f87fe05b829d347a05b5f991bf0c4d5cf5410fe8799f780e788a91ca07bc3f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:25 GMT
ADD file:c9cf6ed72c109eb68384476670cda2086783dc0a2ea6379cb1a662b3c8509591 in / 
# Tue, 23 Jul 2024 02:28:26 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV LANG=en_US.utf8
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_MAJOR=14
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PG_VERSION=14.13-1.pgdg110+1
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Aug 2024 16:52:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Aug 2024 16:52:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Aug 2024 16:52:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Aug 2024 16:52:20 GMT
STOPSIGNAL SIGINT
# Thu, 08 Aug 2024 16:52:20 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Aug 2024 16:52:20 GMT
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
	-	`sha256:ab016d7f6ffdf727aef10e310786c26f9fdd63302754e4326c18e6a49a394bde`  
		Last Modified: Thu, 08 Aug 2024 20:08:07 GMT  
		Size: 101.7 MB (101749019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b23abe8ac87b26dd2063407bf85a61b3855dcfcf3b8d0e5a5dc6ce65ab87092`  
		Last Modified: Thu, 08 Aug 2024 20:08:05 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764d309faf72ac1e476395dbecdc17e26281a993dc4a51c15a901f070c7f81d1`  
		Last Modified: Thu, 08 Aug 2024 20:08:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790b82e7f5a5de33f1a3b733f2cba74570290e50ae21a1f567417873a3beaf12`  
		Last Modified: Thu, 08 Aug 2024 20:08:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f4ef5fba440a4b4d1d306e220cabfb45c4a3f9fc42fbd3720d4ba9e2915a90`  
		Last Modified: Thu, 08 Aug 2024 20:08:06 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2228cd1716aab82c418dd88bb8bb44c1995e383f4ff27f6de9c9ac52a7468b43`  
		Last Modified: Thu, 08 Aug 2024 20:08:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:01c5d76a9625391daef9aee037031618805ab9a7e944ae8c1bfc03128124fb31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5935067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb8db82286c2680380ca70be16e074a64defa661d95bab152a8267d87eef180`

```dockerfile
```

-	Layers:
	-	`sha256:5791a59d7aca33d2b2ce755a0a3f24df7246103779dc91ce0b0d1b7e1afb4505`  
		Last Modified: Thu, 08 Aug 2024 20:08:05 GMT  
		Size: 5.9 MB (5881220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7527e583ded67dac575d0af0efa4d85c1feae6a975bf2c8e478d9017a5d491bb`  
		Last Modified: Thu, 08 Aug 2024 20:08:05 GMT  
		Size: 53.8 KB (53847 bytes)  
		MIME: application/vnd.in-toto+json
