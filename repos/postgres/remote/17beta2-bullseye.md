## `postgres:17beta2-bullseye`

```console
$ docker pull postgres@sha256:61cee8600c16aa117b4491cb265473d6d242e104eb9db68e4694fd48fdb31353
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

### `postgres:17beta2-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:48e47c8a6182a9d2e8e0b016378a71121930dcab910c34455a48ef08d4599ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (146001979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52b9f1070f3fcc22746d502e535d5f2c0d4fd9b1a67a950135855601a8959b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg110+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65b5b326a1aade2056fbfe176a04e4d93feaab2400d262e2746eaa11bfd2f5`  
		Last Modified: Tue, 23 Jul 2024 07:23:31 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199d5409a68ea199695beef01f663a9ffa2a6cddef2406b2cd3244ed888256f5`  
		Last Modified: Tue, 23 Jul 2024 07:23:31 GMT  
		Size: 4.3 MB (4308186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88beba2e18910bdc261fdf4290e5dbe44cda6409ae8173a5dc0ebd82dac4fd7b`  
		Last Modified: Tue, 23 Jul 2024 07:23:31 GMT  
		Size: 1.5 MB (1472175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93a99ac8e3efe8c740ea13e741eeeb2f741376dac72fc9b8c7a280cd03db9fa`  
		Last Modified: Tue, 23 Jul 2024 07:23:31 GMT  
		Size: 8.0 MB (8044504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f97d954d1d583d5c870b4ccf534edd83212fb3197b99b0167d5ea6995904f4`  
		Last Modified: Tue, 23 Jul 2024 07:23:32 GMT  
		Size: 1.0 MB (1038364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0a96a00eeb3b2046b0c70fb4ce3b34562998870a75502a7669af2a6932797f`  
		Last Modified: Tue, 23 Jul 2024 07:23:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb726804421e25b2e6c732ca96895d69abc2c6754fc921a638956802638d7c7`  
		Last Modified: Tue, 23 Jul 2024 07:23:32 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9454cfa768793515f7f02631c19f0df211b1abb7fa49f07f9fdff56a64d20ff`  
		Last Modified: Tue, 23 Jul 2024 07:23:35 GMT  
		Size: 99.7 MB (99689342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4319dbe84e4286560be1c8faf28915628b62012626f3c0f273d6db907b8804b0`  
		Last Modified: Tue, 23 Jul 2024 07:23:33 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cb0fc6dcac311da69995cc895c838d731a9d34c3079629eadfe0bfa4b311b8`  
		Last Modified: Tue, 23 Jul 2024 07:23:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e40b611b3211c62612418c86b16dee9309465ff8097f9c8c513b13590e50b0`  
		Last Modified: Tue, 23 Jul 2024 07:23:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55069580bcb9aec6e88ea978881837929cdb9ee86f0acb6339fce337f458e2a8`  
		Last Modified: Tue, 23 Jul 2024 07:23:33 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e61c6cd9b0fe6494f2aec4033ed8ef087391e357329d478bfa64193e55760de`  
		Last Modified: Tue, 23 Jul 2024 07:23:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:7ebe8c8a109f4dbbd54786c493eb960b8b8c47a93ba6278f6601a9429feb58c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6058553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88937decd71a5379c6c9b02afbca57130d703abb691bb19a35e1c40bac7b159b`

```dockerfile
```

-	Layers:
	-	`sha256:167d09166c118245b5b37ac5541aef7f02351d627c4d9f8a4a8e1b3254bdc635`  
		Last Modified: Tue, 23 Jul 2024 07:23:31 GMT  
		Size: 6.0 MB (6004913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1184cfa38b3322c2e82c0382bb7a963886bb23cc01305c198564c2b7cc50c67e`  
		Last Modified: Tue, 23 Jul 2024 07:23:31 GMT  
		Size: 53.6 KB (53640 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:369c3cb4f8003bb0a948478661ec7fc67a583694ea9f50f58add23f22aa11faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138942710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13851b33e8485e9e67597569c0cd377d0b643b1e1cc5b10396334d8a40815b34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:56b9d2d0e0360f64ade3cbe073b446e10c8e6bd253b761c16b5f319a8103d181 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg110+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5b04226d50f1c00a6c8950192ad70a2038016868ab6ffb162ad447e35e67a3cb`  
		Last Modified: Tue, 23 Jul 2024 00:02:06 GMT  
		Size: 28.9 MB (28930588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5636fe7fb7fba438c7fff4ddcfee0f950769f1572e054a3d895ee33d576339df`  
		Last Modified: Tue, 23 Jul 2024 10:53:07 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f10f6e1da99de5aa5d3d982890e58c6962a02891f4cce4bb77688d8f33b381d`  
		Last Modified: Tue, 23 Jul 2024 10:53:07 GMT  
		Size: 4.0 MB (3991608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2aa3c40e20f5f3327dffc32b8b1c66f26ef8d4aaf4cd5e576d84da4dba9031`  
		Last Modified: Tue, 23 Jul 2024 10:53:07 GMT  
		Size: 1.4 MB (1449201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05206ec3dc415525ad05c6213ca7c7edff1b0ad3b75090fad05459b03153f947`  
		Last Modified: Tue, 23 Jul 2024 10:53:07 GMT  
		Size: 8.0 MB (8044375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373a46297041ce97551970eea6995ac0dd2be03aeb3954e26627ea46c4c5e62`  
		Last Modified: Tue, 23 Jul 2024 10:53:08 GMT  
		Size: 1.0 MB (1034855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08b1b6c925b6758a3783d57de9a41b23c931ea43a1eebf60c61ec22b81a6344`  
		Last Modified: Tue, 23 Jul 2024 10:53:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1809b06d89cb509ab3e6d5b275c306715b607a92c7dddd920e4109c96bfb21`  
		Last Modified: Tue, 23 Jul 2024 10:53:08 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507b304f1d7418adaf1eaccadb974a467fe818567339283601e9878ed376bcfe`  
		Last Modified: Tue, 23 Jul 2024 10:53:11 GMT  
		Size: 95.5 MB (95471009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1d23d288df454a59b185f581aa3fab5b4953ab7a5acb85cde1f99b45e580bc`  
		Last Modified: Tue, 23 Jul 2024 10:53:09 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2023a23b2b7aa90129a1d8789f9f3d04c4ded99869b761d224b46c5f63affe5`  
		Last Modified: Tue, 23 Jul 2024 10:53:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ee07635d6436f783c6a68eb9efd75ea666086b21cd16d40ab54740214fd832`  
		Last Modified: Tue, 23 Jul 2024 10:53:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec6249d6902cce5f78f199d66bba46486edd82069f2d83b0b5ad11c32e63760`  
		Last Modified: Tue, 23 Jul 2024 10:53:10 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a1e2a9e0517bc758c604068850e7c7dabf8acc586722f261ee227e024140ab`  
		Last Modified: Tue, 23 Jul 2024 10:53:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:0fc8caf1fc47038cd12af5a83ece45b4cb86321378167edf231b3337ff55a020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379631493bb0a20c243626bda05fce7d5bdd20927673d84670ef50ae52265593`

```dockerfile
```

-	Layers:
	-	`sha256:464551645fb23f15e79b9ef14190123a8b2dc7d3d21a926d975906c1042888ae`  
		Last Modified: Tue, 23 Jul 2024 10:53:07 GMT  
		Size: 6.0 MB (6022291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db995df8c67c5d641b987ee262507a11a534de64449077f90a4884120e634328`  
		Last Modified: Tue, 23 Jul 2024 10:53:07 GMT  
		Size: 53.8 KB (53829 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:fc0e3cecd3f1853c59cb344a68f8cc32ca4d417fcc694f42b9a31772cee96992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133993732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf91c21158f6aec0daddadc2559df27aa1964159a34988332c65b6eac3b85eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg110+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2e6e7ca20a0352c0b3bafb3ca859f61024c2e779ae7536db6de630aed4dcfc`  
		Last Modified: Tue, 02 Jul 2024 17:53:20 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd02606fb60b1e7c41d915a6e82586a997958faf0e6a9df7c58a0ab5eb701a0`  
		Last Modified: Tue, 02 Jul 2024 17:53:21 GMT  
		Size: 3.6 MB (3601631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0cc4b66d673a3f76364ce213c89f16acb81be16ea7e2fbb13054be2984828a8`  
		Last Modified: Tue, 02 Jul 2024 17:53:21 GMT  
		Size: 1.4 MB (1439220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5cda429c5354ba571e4c080fa09a8d24a4296284c4f54c6e07c703ee25218e`  
		Last Modified: Tue, 02 Jul 2024 17:53:21 GMT  
		Size: 8.0 MB (8044454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd1b7742bdd4e2db871e83eb520892a4d6d285ce5a4d4290a8595b94410e47c`  
		Last Modified: Tue, 02 Jul 2024 17:53:22 GMT  
		Size: 908.7 KB (908665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9acb133d0a997f6df46e8779f6b8506c44680bc4e54393c883e8c3cc0732108`  
		Last Modified: Tue, 02 Jul 2024 17:53:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562b330fb0e12e87a5b80f32082ec214a0724a118a421491612e8e4f8aaff0f4`  
		Last Modified: Tue, 02 Jul 2024 17:53:22 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d72ade89d0f69deed6261f2d0368beea31c854bd502c1b110ba20c9d92761f`  
		Last Modified: Wed, 03 Jul 2024 04:55:07 GMT  
		Size: 93.4 MB (93395980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762e6520757855c581240c23504af13d04e32351aa79a14127ed257487300812`  
		Last Modified: Wed, 03 Jul 2024 04:55:04 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8303e71e0e98b75e78a24e177f4ef2831f59b7e085df3cddc72f67c3d19eac87`  
		Last Modified: Wed, 03 Jul 2024 04:55:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc5fe000aa075c121d70d57b0f85aa5b74400d3180c74b6a9107ad2dc0ed406`  
		Last Modified: Wed, 03 Jul 2024 04:55:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b2611ddfda1a964b6dc5bc25297c3d8734fa200b2e44fed69f14bd5d7d36bd`  
		Last Modified: Wed, 03 Jul 2024 04:55:05 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8757d9b63c47affb05fac8ffaa19a8c6040d0ce70860a8d5a91069419ec63cb8`  
		Last Modified: Wed, 03 Jul 2024 04:55:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e5c841dc2e44994a15c2101229b7ff48dacc06a98d31da5e49a5ca233ca640ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6045482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec62d92bd34c3ca5c9737d0a780ac8fc2cc843186f0c836a29c758ad22a0593`

```dockerfile
```

-	Layers:
	-	`sha256:f0c5f988dfeec6ab1896920ae44666fee5e763c6674b908d6cb5ecde66defce9`  
		Last Modified: Wed, 03 Jul 2024 04:55:04 GMT  
		Size: 6.0 MB (5991662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fa90fade6a46708a4bf3ae529bdbea509171e3db8e07e17f4051ed8d45a611`  
		Last Modified: Wed, 03 Jul 2024 04:55:04 GMT  
		Size: 53.8 KB (53820 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:704b9befeabc48886e25bd069213ccc1385239c906a30f09f53df95bb5855dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142383374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45aa107b353f32b28d10dff6f967867704d69873e3f2bdbf9c1859596f7db650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg110+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a95b38c9a462df84b4489a2171ee445688f75b70671de3a6b26b68c258aec13`  
		Last Modified: Tue, 02 Jul 2024 19:34:59 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577b2fd44d930b34f7a1109a3f9defc40d20441fdc15b0abc7516b1433b995d8`  
		Last Modified: Tue, 02 Jul 2024 19:34:59 GMT  
		Size: 4.3 MB (4312716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3aa59608f8a37f77bbb96ab9d57642f3e2843065e3d1304f3618cac58426f90`  
		Last Modified: Tue, 02 Jul 2024 19:34:59 GMT  
		Size: 1.4 MB (1404096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030236a974641b5cc088f3fae36a67d14cec55d1b4656295000df59cef3a3acb`  
		Last Modified: Tue, 02 Jul 2024 19:35:00 GMT  
		Size: 8.0 MB (8044228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3ec99abda8e0b1763d3cc6c2758951b459c148eb397046ccdded4b18defc34`  
		Last Modified: Tue, 02 Jul 2024 19:35:00 GMT  
		Size: 1.0 MB (1026638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd34ef2fa9c6fdcb9e5f0c88a4fa038707643ab0015410576116460204f43c8`  
		Last Modified: Tue, 02 Jul 2024 19:35:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bdfd2f82fb824c63b06d34cc6280bb09a3a0315cfe91b3ff0370edd1b9c695`  
		Last Modified: Tue, 02 Jul 2024 19:35:01 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0968c6cb99901453e43fe0e84c715c605f6189b49141980385d055cc96987a65`  
		Last Modified: Wed, 03 Jul 2024 03:56:06 GMT  
		Size: 97.5 MB (97504996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2feadfdeb59d6c2a17a8dbfc5796a495def5ebc98039d0b1d216be3286bfbc`  
		Last Modified: Wed, 03 Jul 2024 03:56:04 GMT  
		Size: 10.2 KB (10242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916b824eee91f72da378dcec068d1bc0bad315163927ececccbcba10d823c0c0`  
		Last Modified: Wed, 03 Jul 2024 03:56:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05478f8b386a5ebf987a2e9962e8586363a8cd1df47fcb0b0083a96cd1f650ca`  
		Last Modified: Wed, 03 Jul 2024 03:56:04 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c645c3a938051b7570469177b803762fa95ec8cfe6ec5ae75836b1f2e0e42cb`  
		Last Modified: Wed, 03 Jul 2024 03:56:05 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73436488f65647dfe5dbed46ca4c39f5ee1a11e68f8bb53e8d047053b2c4c75a`  
		Last Modified: Wed, 03 Jul 2024 03:56:05 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5ef19fce7bb1b5f2c6edac965e898e5fb586355125146fd8bfa1304f0efbf765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6034989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55852d5cda8606dfc169bec318ff3fae29b3b29d47605010916fe978e8e55ab6`

```dockerfile
```

-	Layers:
	-	`sha256:746010d0bad4d51d4ff397a81bbcce7c17e0bbcf59d5a407480e99bd6d3b97e5`  
		Last Modified: Wed, 03 Jul 2024 03:56:04 GMT  
		Size: 6.0 MB (5981076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a459f0bef1108e00eea82418b19312af7157af5f9e10df3cac79b1d0d84a380`  
		Last Modified: Wed, 03 Jul 2024 03:56:04 GMT  
		Size: 53.9 KB (53913 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:793340977275e4b62ccf7c55e60500a6c2399c50a2084a567e54307cd449c3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148780823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516e08d40cf16bd4ff62ce7e24a9c2c1e391f4c1ce4a3b9f8bb921e550a5ce8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg110+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482bad966284c719d67c51b631a266f27a9f82a04a9b67889a5139d80e4c4ec3`  
		Last Modified: Tue, 23 Jul 2024 06:24:13 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295b1751f475be673510d84df386135ac8a02fe4d9087549cd6567086429b817`  
		Last Modified: Tue, 23 Jul 2024 06:24:14 GMT  
		Size: 4.7 MB (4719569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f9c240328ef7194b03239c985875bb702aacc270827442b7806468479a1037`  
		Last Modified: Tue, 23 Jul 2024 06:24:13 GMT  
		Size: 1.4 MB (1447740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e73853f1baa358e7207a74770c238a21e4fd054821dc67ee43d8bc189bea9`  
		Last Modified: Tue, 23 Jul 2024 06:24:14 GMT  
		Size: 8.0 MB (8044298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd296cc88e0b14894034298591ea394038be9d5a51e2e8864af33cbb5574c74`  
		Last Modified: Tue, 23 Jul 2024 06:24:14 GMT  
		Size: 1.0 MB (1028903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a3b5330e4b285a78938ca964d498a883b9be9bbb8db21972cf1fad9c60cadb`  
		Last Modified: Tue, 23 Jul 2024 06:24:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacd361ac68b4b35d4baae7a2d4b57c756b44c7cb7ebd3edab67f91d2a3ae95f`  
		Last Modified: Tue, 23 Jul 2024 06:24:15 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8447abddbb5552f3dabdff8646bf97bb8a89736b34def3b232d023d5d8969fe4`  
		Last Modified: Tue, 23 Jul 2024 06:24:18 GMT  
		Size: 101.1 MB (101105429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9901dd70130e377f6bfe79b48c0b873e8a1988dd800ecc400e35b371fd6da7`  
		Last Modified: Tue, 23 Jul 2024 06:24:15 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8996e895bd3aa4e16fa61dc9eb4aa98474c2c5ca96e6f6f2b0f9781c721ce0`  
		Last Modified: Tue, 23 Jul 2024 06:24:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8704300e910c572ea2a9f98626fa9170dcdbd4264debcd6b68b4b5a25daeae0f`  
		Last Modified: Tue, 23 Jul 2024 06:24:16 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1d12f2fa9c1d0059469744b1dc5492bb6f0ce1d9fa7cb6cd28fdbdb09243c8`  
		Last Modified: Tue, 23 Jul 2024 06:24:16 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2097c807939015399c73392ef27dc808cad02331eebccb11146019ffd82c7812`  
		Last Modified: Tue, 23 Jul 2024 06:24:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:21ea921a0224859614c603a65682502cebe27eedab40c86ad19b6d3437d417c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6073234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd09eb5f63fcd380f60521711b9d145036beefe89b0ea5910b46c8139db02e`

```dockerfile
```

-	Layers:
	-	`sha256:1df6b6022f09ea2a1bfe6ce35162f9c3ddd19e99fe29c085a9ac10668654a7a8`  
		Last Modified: Tue, 23 Jul 2024 06:24:14 GMT  
		Size: 6.0 MB (6019624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0829c57423ea79f99ec05ebf3dba1730c4497c4c5cb068e66dbfb9511e74e3e`  
		Last Modified: Tue, 23 Jul 2024 06:24:13 GMT  
		Size: 53.6 KB (53610 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:f29ff240ac28d2b81e5f0bd70a3f55d88bbbc775b4fa581c3f5663fd4174fa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140330072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c21cbe1dffdfdd489359eb95befc02173eb784e2f04d3a603661c5175e8848`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:791d05eca72cc81080afbb76c7f3f02a74893142203b6aada9e3170404049223 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg110+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:59602b870d8ca1e13dffda9de0c5f866f86ff35c1e595ea481bb1b2c48c18b8e`  
		Last Modified: Tue, 02 Jul 2024 01:30:52 GMT  
		Size: 29.6 MB (29639850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0af3c2bdc29247df82504a8376a9246ba8e4b295975db3b2edb47c77bb6e92e`  
		Last Modified: Thu, 04 Jul 2024 17:17:09 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb036a51139841c158077b90b64f408af8acc8a98ff85eccc38d8bd13094868`  
		Last Modified: Thu, 04 Jul 2024 17:17:10 GMT  
		Size: 4.3 MB (4308315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebaef4d952d909468119521805355a750f15dfbd6077b7bdc7a1fc15e2eb0b0`  
		Last Modified: Thu, 04 Jul 2024 17:17:10 GMT  
		Size: 1.4 MB (1359313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28bf3a07a4667cf1d9f0ece7eb23e1c8fdd19e9d73f1e5c66b8685c7e372e3`  
		Last Modified: Thu, 04 Jul 2024 17:17:10 GMT  
		Size: 8.0 MB (8044621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5539b74fd11d162a93dec15082b621a8d080c1cc9109fa5ee0a9219fc56004`  
		Last Modified: Thu, 04 Jul 2024 17:17:11 GMT  
		Size: 1.1 MB (1090268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41073eb9ba42620efe833f4eca573e7f3d36dc2c6c4d883515909e4d8ce372a4`  
		Last Modified: Thu, 04 Jul 2024 17:17:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b199fffbb980ebdd3c3425414376f29d34cfe16e4c3ff9d4ba52180325280b0`  
		Last Modified: Thu, 04 Jul 2024 17:17:11 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a7d604298a934e63672e4c627728017ac217ac8d609ed35cd6d45b15a8bb12`  
		Last Modified: Thu, 04 Jul 2024 17:17:21 GMT  
		Size: 95.9 MB (95866613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dc49a2b8001f46089a07a733c3b61275fe6420eb2b3ff908974faaccd4c868`  
		Last Modified: Thu, 04 Jul 2024 17:17:12 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3365b136132c5ee1c24a6035f4f75b62b0b8218134b3c52485bd2419e11462`  
		Last Modified: Thu, 04 Jul 2024 17:17:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931c11fc8e076526a6354bc21361643b93e89a7a6ae837bb02e815da9b1fa500`  
		Last Modified: Thu, 04 Jul 2024 17:17:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb46f91f6ccb96f6e962d45ba6ea01834461999696446c227f0fb4624b61a6`  
		Last Modified: Thu, 04 Jul 2024 17:17:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1e99e9c36008a301067103fe88147e330bf93daef683a1c230c05e5a9a730d`  
		Last Modified: Thu, 04 Jul 2024 17:17:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:41e527789c55df75fab6c9e2b476172bcb6a9f79c2ca5d0ecfe25fbfa843b3bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 KB (53484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7907ca63c19f496c051473818d51a6db7933d8ba575daae3bb652fe5baeda3`

```dockerfile
```

-	Layers:
	-	`sha256:d1f9dca4ce8951da766be87a2bba3b69eb28c92eef278e1308c4006c44ed2095`  
		Last Modified: Thu, 04 Jul 2024 17:17:09 GMT  
		Size: 53.5 KB (53484 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:0b748e8cb3d9a13c9c4c0d08ce0abcb372602d06fa6e68e79307975158f1b0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157039315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876c00c9bcbe31aaad0392fe2734c545e525689dafa29e285aca4a798ef256c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg110+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a92aeac617d879925b9a88d57f1c8664df54f3425c22018b491d90ecd546c9`  
		Last Modified: Tue, 23 Jul 2024 23:16:23 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6011eaa530ee4bbf244680e54c17d0e3fbbf42306a6aa669be940ad1f8ea311c`  
		Last Modified: Tue, 23 Jul 2024 23:16:24 GMT  
		Size: 5.1 MB (5137826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d96478163bd229bf7e8a8d48c4206a53baea289c564c955adb2f0ddae5da308`  
		Last Modified: Tue, 23 Jul 2024 23:16:24 GMT  
		Size: 1.4 MB (1393639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1deb0412097ea36dfece1de41c99f4c43d276b619fcde3629962ab7fa52377e`  
		Last Modified: Tue, 23 Jul 2024 23:16:24 GMT  
		Size: 8.0 MB (8044537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad760215c33555bd2edfee360447473f37dde1c4d28365229c93857f1f1c8fa8`  
		Last Modified: Tue, 23 Jul 2024 23:16:25 GMT  
		Size: 1.2 MB (1197556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3399a9f34d32e48471c3c520768cd8a61cafd5d7db969e0edfc8916abb59b7a0`  
		Last Modified: Tue, 23 Jul 2024 23:16:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba053f93a2baa0751ced12a029af4e4ca8e2aa1d9577508b34028bcc26d256f1`  
		Last Modified: Tue, 23 Jul 2024 23:16:25 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d717cfc8f30d9aa6bab86540af56760c3be7f8b793a35d1ecc33743d4dcf25b`  
		Last Modified: Tue, 23 Jul 2024 23:16:29 GMT  
		Size: 105.9 MB (105939469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0384c0ed370054a19f182c4c00bbc390d0a59e994bb039ab3c16f9e2588fed`  
		Last Modified: Tue, 23 Jul 2024 23:16:26 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b60fe09ffb427cf987db5c9e7392d48387feaaee85bd689d1ee4966ce9fcf96`  
		Last Modified: Tue, 23 Jul 2024 23:16:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e8aee0cf9fd9fa3d3a457394b1c29c6baa253ecb01000550dc308b22da2f0e`  
		Last Modified: Tue, 23 Jul 2024 23:16:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff9428c7240e46943a5106212434f9bac643eec14f1a2d59b2feb1b14a9bb9b`  
		Last Modified: Tue, 23 Jul 2024 23:16:27 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26557e55f57262385030b9036187b10da69d60b1e3f0b698a3f0325119cc73d`  
		Last Modified: Tue, 23 Jul 2024 23:16:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:22b231f0b03907614abd12a32cd0602737f438d57f56a3474dfbf087775b4a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6065727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300bb1210629cbb16fafa313051e953597f51e00ac5b68a913f0181a1a9203af`

```dockerfile
```

-	Layers:
	-	`sha256:455742e992ca1561ce7a75064d14604012a58bafc477ef381c0cc5c8623b12f7`  
		Last Modified: Tue, 23 Jul 2024 23:16:24 GMT  
		Size: 6.0 MB (6012039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ad82532fc6e1a5d56272944b10a2a03a532341295be7aaf028216ea03628790`  
		Last Modified: Tue, 23 Jul 2024 23:16:23 GMT  
		Size: 53.7 KB (53688 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta2-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:e8772442dfb39ff66cf0fbb9c2696b50ff15b90f12f8768971ef40f4758211c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150391890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2d9dd490de8827833b6f8227db9e0cd574b46229540a882c163ebcf2ea8c99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 02 Jul 2024 00:03:06 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV LANG=en_US.utf8
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_MAJOR=17
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PG_VERSION=17~beta2-1.pgdg110+1
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 02 Jul 2024 00:03:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 02 Jul 2024 00:03:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 02 Jul 2024 00:03:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 00:03:06 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 00:03:06 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 02 Jul 2024 00:03:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8771162ecc10e12f01f45f9ccddbbf657cdd824892741f9af6235c6298dfbfa`  
		Last Modified: Tue, 02 Jul 2024 08:31:49 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027d70b91265eba8e1cf67143cef12b0305899f9916bbe77326d91864caaafe2`  
		Last Modified: Tue, 02 Jul 2024 08:31:49 GMT  
		Size: 4.2 MB (4200291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82375d2943cb36dee7c35b28207b8dc8067042c708d3dfa37386f300a61b9dc4`  
		Last Modified: Tue, 02 Jul 2024 08:31:49 GMT  
		Size: 1.4 MB (1437935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef2faea4953f180b7e4e90f396bd5bd761ccc5af39b936d801c176cdd16ce44`  
		Last Modified: Tue, 02 Jul 2024 08:31:50 GMT  
		Size: 8.1 MB (8098828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ffc6b3171073e1e24f61e22a41cb6e18c8dfd6bd42f4ccbf3ee3b2bc8006bd`  
		Last Modified: Tue, 02 Jul 2024 08:31:50 GMT  
		Size: 1.0 MB (1015273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abc4cf0b3c180f548c052758dbdf0329c57cc5230411ec33452b00e12b5bd77`  
		Last Modified: Tue, 02 Jul 2024 08:31:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d94840c3fe2e2d8e04af86488d611897fd8bea8fb31d35052f0b3e64a136328`  
		Last Modified: Tue, 02 Jul 2024 08:31:50 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c740016bfcdb49f7ce28fab938fd78d1195cbfb76cc914a31e9d3d867d0cdc`  
		Last Modified: Wed, 03 Jul 2024 03:24:29 GMT  
		Size: 106.0 MB (105956128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5039b45a392cc7abc5423fa9521813fbe80f75b64564e994850add25fd5954de`  
		Last Modified: Wed, 03 Jul 2024 03:24:27 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a294a5375fbaede3eb5611652f1d08a25a40cf7d0c67922421446352dbcc1de`  
		Last Modified: Wed, 03 Jul 2024 03:24:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bc2bae7d7e44b980a25e28fcb3c7c38ab82fae8cbddafb973987b2114203f6`  
		Last Modified: Wed, 03 Jul 2024 03:24:27 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6035ec79055f4fb02744244e820dc61f0a3dbd6c753b226e27e877fa02e0889a`  
		Last Modified: Wed, 03 Jul 2024 03:24:28 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0036b3d7d4d55eb85b94117272a29a39f1aed2fe824e98ae9b59adc6bdef762`  
		Last Modified: Wed, 03 Jul 2024 03:24:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta2-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2fbdd1d9626f2a21393503ba5de26e5f00912dfddeb0eb92bfaed2d77f428aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6027421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd895a4ff27cd0ba8ae2f5859dafde6b082f27b636efe501857f045c325c37e4`

```dockerfile
```

-	Layers:
	-	`sha256:6ddf792d013e200d6b743153e9e2f2b2834f1fed04e6cdb6bbaa6e7e988afb2c`  
		Last Modified: Wed, 03 Jul 2024 03:24:27 GMT  
		Size: 6.0 MB (5973775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48c84b12d1ef17032301ff3b8619777574b5dd2653150391491882a762d90504`  
		Last Modified: Wed, 03 Jul 2024 03:24:27 GMT  
		Size: 53.6 KB (53646 bytes)  
		MIME: application/vnd.in-toto+json
