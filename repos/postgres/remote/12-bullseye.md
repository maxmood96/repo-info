## `postgres:12-bullseye`

```console
$ docker pull postgres@sha256:8e26d4fc490c46c20613639eb04c235b2be80e1b372f41fd247aaef91b77cd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `postgres:12-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:2928c2c422554b31c6871bee6fb9dfa65b900558e5b3ec7e0e3b5c00d1ef766b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136181234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e79589dc2312f9b90d85773258d58248f0e3c0a41a0c203db69d0954cbf5dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 07:38:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 07:38:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 21 Dec 2022 07:38:32 GMT
ENV GOSU_VERSION=1.14
# Wed, 21 Dec 2022 07:38:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 21 Dec 2022 07:38:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 21 Dec 2022 07:38:48 GMT
ENV LANG=en_US.utf8
# Wed, 21 Dec 2022 07:38:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 07:38:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 21 Dec 2022 07:38:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 21 Dec 2022 07:40:15 GMT
ENV PG_MAJOR=12
# Wed, 21 Dec 2022 07:40:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Wed, 21 Dec 2022 07:40:15 GMT
ENV PG_VERSION=12.13-1.pgdg110+1
# Wed, 21 Dec 2022 07:40:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 07:40:34 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 07:40:35 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 07:40:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 07:40:35 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 07:40:35 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 19:36:51 GMT
COPY file:bf069237372db04c7f7fa02783a028485929406470fe90a88fce22131d247679 in /usr/local/bin/ 
# Thu, 22 Dec 2022 19:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 19:36:51 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 19:36:51 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 19:36:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048d3078d4461044565684a572e14d077ac73a94c395c3b9431212f52d0b4d1e`  
		Last Modified: Wed, 21 Dec 2022 07:41:50 GMT  
		Size: 4.4 MB (4414883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d23b4fe6c1e88d82420d4293c4b662c2bff80475bd9b19f86352cacfec2009`  
		Last Modified: Wed, 21 Dec 2022 07:41:49 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846f6946dd5c1c5216690945e5a871e80689a08828845b7f4910a7f81ae9b3f`  
		Last Modified: Wed, 21 Dec 2022 07:41:49 GMT  
		Size: 1.4 MB (1418487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f7157f330d4f9b3b9da4dbdb99fedf6275309e8e0336e2ccb7f511a6158df3`  
		Last Modified: Wed, 21 Dec 2022 07:41:48 GMT  
		Size: 8.0 MB (8045228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eacfb0464b22d24273c047815de12fbdce41fd9e70c1c6294e9a8a9fa74d32b`  
		Last Modified: Wed, 21 Dec 2022 07:41:47 GMT  
		Size: 1.3 MB (1261163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c197e2b597bd8a013bdcd6519bc53ac0e1e445ec201e1f47ea64967d4005c7a`  
		Last Modified: Wed, 21 Dec 2022 07:41:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c45766499511d5ff8c53b50514aef2dd1d590e36b3be3b9c6fbf6cd3f06ba4a`  
		Last Modified: Wed, 21 Dec 2022 07:41:47 GMT  
		Size: 3.2 KB (3205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60393f4009248f9bc544b01afbcbaf9873c818e7b30b472e1b21937505809f3d`  
		Last Modified: Wed, 21 Dec 2022 07:43:29 GMT  
		Size: 89.6 MB (89625284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6949b18592f41ef5cfe8b0b070971382976fc6c4e70e854bfdd83f887213a0`  
		Last Modified: Wed, 21 Dec 2022 07:43:17 GMT  
		Size: 9.0 KB (9028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57f7e79b401947174ecb9d01a67c4199ab42d1bc2e3749518f2870b1f8fe12b`  
		Last Modified: Wed, 21 Dec 2022 07:43:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bfff74eae21bc7a553fd56f67ae6a3e83dfd8590a28baa4596712fafae4cdb`  
		Last Modified: Wed, 21 Dec 2022 07:43:17 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a60db9abf2d5f81281de5d7e2a1bfcce8930940c2f48b00eba99811b07ef373`  
		Last Modified: Thu, 22 Dec 2022 19:39:06 GMT  
		Size: 4.7 KB (4732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:191218a1f9018bd31d3b1048f7184fe6b1ce5db20ab81f015fd7999f5da626c5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129426024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79da682951b05c0604ae3debd6e1ee74c6ba9a2e74fc9e76a93abf609b243250`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Dec 2022 01:49:08 GMT
ADD file:89f7788ae38bc6c172614b734ff10cba90c89ee09ca0f1acccc185c1bec630a1 in / 
# Wed, 21 Dec 2022 01:49:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 04:39:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 04:39:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 21 Dec 2022 04:39:17 GMT
ENV GOSU_VERSION=1.14
# Wed, 21 Dec 2022 04:39:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 21 Dec 2022 04:39:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 21 Dec 2022 04:39:37 GMT
ENV LANG=en_US.utf8
# Wed, 21 Dec 2022 04:39:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 04:39:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 21 Dec 2022 04:39:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 21 Dec 2022 05:27:47 GMT
ENV PG_MAJOR=12
# Wed, 21 Dec 2022 05:27:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Wed, 21 Dec 2022 05:27:47 GMT
ENV PG_VERSION=12.13-1.pgdg110+1
# Wed, 21 Dec 2022 05:42:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 05:42:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 05:42:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 05:42:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 05:42:27 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 05:42:27 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:48:55 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:48:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:48:55 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:48:55 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:48:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6addfee759f2774f92392906ab5b50ba2f4a14314858c502e856f7d7de2a7e07`  
		Last Modified: Wed, 21 Dec 2022 01:54:03 GMT  
		Size: 28.9 MB (28898607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d9844532a4a69a542a08935cff5107e5ac4c1c4783b4f064b5c481d8dc240d`  
		Last Modified: Wed, 21 Dec 2022 05:57:53 GMT  
		Size: 4.1 MB (4096395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393ef085cc55ef83971676a67a0efd4bdf7dc87f66ca85d5b2cf31ef2fc77105`  
		Last Modified: Wed, 21 Dec 2022 05:57:52 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f86729414037fa928f03edfd7bb8fb73bd654465784ec30cf4117e8b59b476b`  
		Last Modified: Wed, 21 Dec 2022 05:57:52 GMT  
		Size: 1.4 MB (1382534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad1318edd8085d0f3ce47a684cbaed87fca9439d366fba6e6e6c967ee88789b`  
		Last Modified: Wed, 21 Dec 2022 05:57:52 GMT  
		Size: 8.0 MB (8045112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b986fce4be1224f480cda174a1247c6a1de45aedc09b81670c718db704a1c4dc`  
		Last Modified: Wed, 21 Dec 2022 05:57:50 GMT  
		Size: 1.3 MB (1257253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f8bdc5227e821802c8f505457ab2d6ab2494bcfefc7ceca71ec1563301df1e`  
		Last Modified: Wed, 21 Dec 2022 05:57:50 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074dbf582857b80715bbdd19403c0897c72f7c13a83ea60d2a5ff72d666c10e0`  
		Last Modified: Wed, 21 Dec 2022 05:57:50 GMT  
		Size: 3.2 KB (3170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eeab695b9ddc1695be65725b3b1caf744a3c5eaf1cfae8d1f774c164c50c26d`  
		Last Modified: Wed, 21 Dec 2022 05:59:57 GMT  
		Size: 85.7 MB (85726965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba5205c1d4eb1a2de324c54d45042a13e3db18d55e233dff61dce2bcc114f2b`  
		Last Modified: Wed, 21 Dec 2022 05:59:42 GMT  
		Size: 9.0 KB (9033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10323a1c540fcb36fbaba2439498d4b3cc2ae7f266d8ae3e868ce46bcf7e69a6`  
		Last Modified: Wed, 21 Dec 2022 05:59:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6f621e305a959ede62c46b79c21602a252891c31ca995c2a2636ac98686fce`  
		Last Modified: Wed, 21 Dec 2022 05:59:42 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806f2fee48961afc8a55d09db71b17aaaf2f98df0780cb532170fe90e43e2917`  
		Last Modified: Thu, 22 Dec 2022 22:51:04 GMT  
		Size: 4.8 KB (4780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:eaf94672b1c0342b86e86ddd913a5e013394eccb88087c9a7235b37301209371
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124192069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3862ab3c9edfe6f3b637e116f10811836dc18704566ee2940ef45bc225892257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:25 GMT
ADD file:d62015d4eb206b606ae0bc76253de55403ede851d6fae0277e76bdaed196a848 in / 
# Wed, 21 Dec 2022 01:58:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:58:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 05:58:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 21 Dec 2022 05:58:27 GMT
ENV GOSU_VERSION=1.14
# Wed, 21 Dec 2022 05:58:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 21 Dec 2022 05:58:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 21 Dec 2022 05:58:44 GMT
ENV LANG=en_US.utf8
# Wed, 21 Dec 2022 05:58:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:58:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 21 Dec 2022 05:58:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 21 Dec 2022 06:40:55 GMT
ENV PG_MAJOR=12
# Wed, 21 Dec 2022 06:40:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Wed, 21 Dec 2022 06:40:55 GMT
ENV PG_VERSION=12.13-1.pgdg110+1
# Wed, 21 Dec 2022 06:53:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 06:53:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 06:53:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 06:53:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 06:53:43 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 06:53:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:37:21 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:37:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:37:21 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:37:21 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:37:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8686edc9eb6f431c8c17a5eddc7bd38917d3b2d7835970d4fdb2ad0db464766`  
		Last Modified: Wed, 21 Dec 2022 02:05:08 GMT  
		Size: 26.6 MB (26559455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd624c2cf0f5f17bd0bd2201bf6d31e2bd5733f6b98f5b07d5fa9acbd0edeaa`  
		Last Modified: Wed, 21 Dec 2022 07:09:12 GMT  
		Size: 3.7 MB (3717136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d33ea93146ba955d0ebd7023ada4f6b71ca023343f8fe8ab3d40d849e93a2`  
		Last Modified: Wed, 21 Dec 2022 07:09:11 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d822d8617b15a1f9b11b6b43a002f6f6948141cca9a2d03e54a1223df597a1`  
		Last Modified: Wed, 21 Dec 2022 07:09:11 GMT  
		Size: 1.4 MB (1375342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767692ba9e7c4f47bce21fd80afbbe0c6f31adb5b2029a0601e2dba26ee9dafd`  
		Last Modified: Wed, 21 Dec 2022 07:09:10 GMT  
		Size: 8.0 MB (8045153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893e9c8ffe08574eba7b2f9e307ad0987d0a994388f9bbcf26264619f11b7135`  
		Last Modified: Wed, 21 Dec 2022 07:09:10 GMT  
		Size: 1.1 MB (1131150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4946c9b3c9f51dc55210624a59df54279a3eeb175c37b3e03f5540699d93ad2`  
		Last Modified: Wed, 21 Dec 2022 07:09:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9972b1b96cdd3906cc70e674c1723e8b8bd8ff31cf8328e039023516ec08d1`  
		Last Modified: Wed, 21 Dec 2022 07:09:05 GMT  
		Size: 3.2 KB (3171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f7cb18b9d7772cb86188e61bb0cfbf5458ea3d12a45cb108fa0d862a70e7db`  
		Last Modified: Wed, 21 Dec 2022 07:11:13 GMT  
		Size: 83.3 MB (83344682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb02160d67bb1781f66f67a9952745bef4dd421a572eb4db580fa0ec81a9d70`  
		Last Modified: Wed, 21 Dec 2022 07:10:59 GMT  
		Size: 9.0 KB (9030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92e2ade35b74dc54ef677e6833038e5e2eb66f10313260d9a08403b04044bbc`  
		Last Modified: Wed, 21 Dec 2022 07:10:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89839adba88aab52a9a46b8984240e650fd288b8953d91afc586ab2499ab67f7`  
		Last Modified: Wed, 21 Dec 2022 07:10:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8dc10a581f84b9b1bb3dd7b3025097997c37912f5d1f95ee85172a525028d0`  
		Last Modified: Thu, 22 Dec 2022 22:41:24 GMT  
		Size: 4.8 KB (4777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c0f4924b1067a1677822b4851e00a0749b08d07f634ac98a34d2c0e63ea9645d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131282942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad790cb2a9e8dd4904d91f24e487bbe233546e6d9b1f1631506fa6bf621e5af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 14:13:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 14:13:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 21 Dec 2022 14:13:30 GMT
ENV GOSU_VERSION=1.14
# Wed, 21 Dec 2022 14:13:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 21 Dec 2022 14:13:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 21 Dec 2022 14:13:43 GMT
ENV LANG=en_US.utf8
# Wed, 21 Dec 2022 14:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 14:13:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 21 Dec 2022 14:13:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 21 Dec 2022 14:15:00 GMT
ENV PG_MAJOR=12
# Wed, 21 Dec 2022 14:15:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Wed, 21 Dec 2022 14:15:00 GMT
ENV PG_VERSION=12.13-1.pgdg110+1
# Wed, 21 Dec 2022 14:15:15 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 14:15:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 14:15:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 14:15:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 14:15:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 14:15:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:46:54 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:46:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:46:54 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:46:54 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:46:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b00aed68edca6043a6b10a0712ee95c1043e63dd0202b2c0369b49d7c228a32`  
		Last Modified: Wed, 21 Dec 2022 14:16:40 GMT  
		Size: 4.4 MB (4416284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59669461a286b4f6f07bd61c8077922651d7be6a3738c6f861b44aa0790097d`  
		Last Modified: Wed, 21 Dec 2022 14:16:36 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149b1a15c79bc2f5b904bbc966c7f743c8bf9e36fa33804cdbac1d1a1d02347f`  
		Last Modified: Wed, 21 Dec 2022 14:16:35 GMT  
		Size: 1.3 MB (1346592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaed8586a762cff256fcd7eb074f21c6b32a0ae7aa4639793d7e14f4f5f041a0`  
		Last Modified: Wed, 21 Dec 2022 14:16:31 GMT  
		Size: 8.0 MB (8045165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda43cdf029d9ac8077556b3a5c2553d89b19195e18b6efdf23ca04ad0a1d634`  
		Last Modified: Wed, 21 Dec 2022 14:16:30 GMT  
		Size: 1.2 MB (1249176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b59b78702f805885aa725fc7bc47c5ef1ec779d62b769731d6e08bf73c4ee08`  
		Last Modified: Wed, 21 Dec 2022 14:16:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e2146685cade8159718dfc69f1f63f88977e8931e9a0012849a4ea6b891d6d`  
		Last Modified: Wed, 21 Dec 2022 14:16:29 GMT  
		Size: 3.2 KB (3197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e3ece9f91134813149301f42097fc9d784ef890a7f88a977bd849f147a6757`  
		Last Modified: Wed, 21 Dec 2022 14:18:01 GMT  
		Size: 86.2 MB (86161671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48756183746b06a0dd1a36397515718c3ba9c35914ab650736e9474fc5aff4e`  
		Last Modified: Wed, 21 Dec 2022 14:17:51 GMT  
		Size: 9.0 KB (9029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5e311a9b34502d96d298f22c53971cf8faa965b82229cd21fab6805cd8953b`  
		Last Modified: Wed, 21 Dec 2022 14:17:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36abcfaefad1863a0e158bc616e79253c2fd25ace18d2b7f51dc35d0e8d3d445`  
		Last Modified: Wed, 21 Dec 2022 14:17:51 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfd047258afd9e2482cfca0d355099bcb9ece97248d63ac7c63dfe8069795af`  
		Last Modified: Thu, 22 Dec 2022 22:49:10 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:a3ec522aa8998b72f973d15a0b0c4c2203080c57471ad7b4e30995a0e1101901
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0b02aff21b4acfc594de0901ea62cdbeae0a9dd2991b0c69d728ac97225797`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:22 GMT
ADD file:5f553fdf893bb3198d173c48f4531e9bfdbab61798c1aa8217fd80e9d686d7ae in / 
# Wed, 21 Dec 2022 01:39:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:12:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 05:12:09 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 21 Dec 2022 05:12:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 21 Dec 2022 05:12:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 21 Dec 2022 05:12:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 21 Dec 2022 05:12:26 GMT
ENV LANG=en_US.utf8
# Wed, 21 Dec 2022 05:12:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:12:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 21 Dec 2022 05:12:33 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 21 Dec 2022 05:53:02 GMT
ENV PG_MAJOR=12
# Wed, 21 Dec 2022 05:53:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Wed, 21 Dec 2022 05:53:04 GMT
ENV PG_VERSION=12.13-1.pgdg110+1
# Wed, 21 Dec 2022 06:05:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 06:05:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 06:05:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 06:05:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 06:05:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 06:05:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:41:24 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:41:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:41:25 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:41:26 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:41:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3228cb514e81f042720b7fd118ace0f279d1a4bc422b7e24189514a574dfa546`  
		Last Modified: Wed, 21 Dec 2022 01:44:46 GMT  
		Size: 32.4 MB (32375745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e943556fe87a1766f9e859d53a63f31edf70a74bbc20c5f1b2cdcdb4fcd66165`  
		Last Modified: Wed, 21 Dec 2022 06:19:49 GMT  
		Size: 4.6 MB (4607325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3a7510a47b3aa4d67dff1a8001ac1d80ce2377ce24cb721216ea6338960448`  
		Last Modified: Wed, 21 Dec 2022 06:19:47 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe6599d1fe0947220ed77f34225a5a6492e5518c85c38c745c6c8ec042b057e`  
		Last Modified: Wed, 21 Dec 2022 06:19:48 GMT  
		Size: 1.4 MB (1385103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4828ace64097adc59d877ed70b5e408134e15173cc7e9826699b28dc639d4939`  
		Last Modified: Wed, 21 Dec 2022 06:19:48 GMT  
		Size: 8.0 MB (8043331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c651e90361949e8913c5798f0b072bc3f842bec7438cd6662b7169e2c679e237`  
		Last Modified: Wed, 21 Dec 2022 06:19:46 GMT  
		Size: 1.0 MB (1027950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d1a8797e7cf8f16814713c4a69615d768c10a16f688ceb4e28a7f75b42f4c8`  
		Last Modified: Wed, 21 Dec 2022 06:19:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a104e3b07bcaa6b4b14bc3498c138dd16796bc7f04f1da4c26e6240ec67dcb`  
		Last Modified: Wed, 21 Dec 2022 06:19:45 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e141f1a7066446b4c80c1158a15a3e51589cba2a3518c5e48827edf4cba0d11e`  
		Last Modified: Wed, 21 Dec 2022 06:21:39 GMT  
		Size: 90.3 MB (90280956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ee60f87193f24be79af2fbb4e849aebaa138734e3b47568fe52fc126137861`  
		Last Modified: Wed, 21 Dec 2022 06:21:27 GMT  
		Size: 9.0 KB (9031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8b5b4823c966c56cd821a0a6944d6615e41179f8d44e257e768b5c26e60eed`  
		Last Modified: Wed, 21 Dec 2022 06:21:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c67cb695f0b3d0eec83e4a21e48e9b8c6b17ddfc0a394e182486ec6185b87`  
		Last Modified: Wed, 21 Dec 2022 06:21:27 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bcc7a3de1ad023f71035c47eb6626e07f4bc1d59a7292bd65452c89a88e979`  
		Last Modified: Thu, 22 Dec 2022 22:45:04 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:84469cf6326418f3a5adc07c9be93caf33358d62d38997413329d54e6582b07f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130602285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d2d3423387c7f2ee079acc1cb8327a046e9f934ae870a31690ce6c1ff4f3ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Dec 2022 01:10:32 GMT
ADD file:45a0ac3f00e914341df42a4d2a56b9081a224ee58e1167fb05ca87662d42f24c in / 
# Wed, 21 Dec 2022 01:10:37 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:04:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 05:04:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 21 Dec 2022 05:04:09 GMT
ENV GOSU_VERSION=1.14
# Wed, 21 Dec 2022 05:04:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 21 Dec 2022 05:05:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 21 Dec 2022 05:05:14 GMT
ENV LANG=en_US.utf8
# Wed, 21 Dec 2022 05:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:05:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 21 Dec 2022 05:05:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 21 Dec 2022 08:07:31 GMT
ENV PG_MAJOR=12
# Wed, 21 Dec 2022 08:07:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Wed, 21 Dec 2022 08:07:37 GMT
ENV PG_VERSION=12.13-1.pgdg110+1
# Wed, 21 Dec 2022 09:02:36 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 09:02:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 09:02:48 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 09:02:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 09:02:57 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 09:03:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:36:23 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:36:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:36:29 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:36:32 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:36:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5410793baaff16536eff1e5ac655d98039bd44f581c42d6ceb254202d1196477`  
		Last Modified: Wed, 21 Dec 2022 01:18:42 GMT  
		Size: 29.6 MB (29619894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09f277b7889b89adac84d9e1b9956cc24a2085d4e6c118d6a99b7e60e68d133`  
		Last Modified: Wed, 21 Dec 2022 09:58:51 GMT  
		Size: 4.2 MB (4196241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30654bcaa1f87927c16aba1fb1b0407ff819f7101045827de280189a07e79ff`  
		Last Modified: Wed, 21 Dec 2022 09:58:46 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7031b7739c6d2442e7da252059510abd5e4644354840d8185aa49a72387d11`  
		Last Modified: Wed, 21 Dec 2022 09:58:47 GMT  
		Size: 1.3 MB (1298057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14cf68323001d07aa99d1140f5f6385d0789c815996ad93763582b68101892ed`  
		Last Modified: Wed, 21 Dec 2022 09:58:52 GMT  
		Size: 8.0 MB (8043750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075e3c38aa4c2021982b1d182374f481fa964c1bf02df4f776259c6c35a28b6b`  
		Last Modified: Wed, 21 Dec 2022 09:58:45 GMT  
		Size: 1.1 MB (1089511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b6c83bd4796287b2500a6bdfb4edc3b35c9467616561b2a5a08f1c4f95d38b`  
		Last Modified: Wed, 21 Dec 2022 09:58:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c99a29ee3c9edce84a530ad1bde7d777096de77581ed2a60d08160162110cdd`  
		Last Modified: Wed, 21 Dec 2022 09:58:44 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a024b8266e5519c97465ef618a0e8dc358d76f129f63547e6c1f81a03aae94`  
		Last Modified: Wed, 21 Dec 2022 10:03:29 GMT  
		Size: 86.3 MB (86335805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbd2c2e41f2fab557dad4835f84ad1daa3d5b9847da5391605cd80f823abcc4`  
		Last Modified: Wed, 21 Dec 2022 10:02:33 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b5bd52acadf0689254a3aeb42f1c1bdd97d687b363c5c497e32374b24b30ab`  
		Last Modified: Wed, 21 Dec 2022 10:02:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565eb45f8e22eec0ec759b70d97cb581d0ccbf9eae8de55f8a7cda3a8cb5e8cd`  
		Last Modified: Wed, 21 Dec 2022 10:02:32 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb29d0f43961e2d3be2d605867fc06e0fe2cce5be09904943ffdba7790a46d2`  
		Last Modified: Thu, 22 Dec 2022 22:38:04 GMT  
		Size: 4.8 KB (4775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:6e7d2e6dd81b9e2557bc1dc18f80659206b82a5a733336cf484de87bc1a3808a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145101707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f48eec8da6f149e8526ccfcc2d112aabea89c466df44a105b47d872f5fbddf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:41 GMT
ADD file:5ab731e5c1e145738476449b6b0748f44822bb2cd6c53ae5bbf6ae6bfec83383 in / 
# Wed, 21 Dec 2022 01:17:43 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 07:16:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 07:16:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 21 Dec 2022 07:16:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 21 Dec 2022 07:17:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 21 Dec 2022 07:17:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 21 Dec 2022 07:17:23 GMT
ENV LANG=en_US.utf8
# Wed, 21 Dec 2022 07:17:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 07:17:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 21 Dec 2022 07:17:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 21 Dec 2022 07:52:33 GMT
ENV PG_MAJOR=12
# Wed, 21 Dec 2022 07:52:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Wed, 21 Dec 2022 07:52:34 GMT
ENV PG_VERSION=12.13-1.pgdg110+1
# Wed, 21 Dec 2022 07:53:32 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 07:53:37 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 07:53:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 07:53:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 07:53:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 07:53:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 20:26:19 GMT
COPY file:bf069237372db04c7f7fa02783a028485929406470fe90a88fce22131d247679 in /usr/local/bin/ 
# Thu, 22 Dec 2022 20:26:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 20:26:20 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 20:26:20 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 20:26:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ba010cdd67bb149ba042a834d84020887fc3f8ca9d8e51b31f3104286cafb9ba`  
		Last Modified: Wed, 21 Dec 2022 01:23:22 GMT  
		Size: 35.3 MB (35268748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ea7bbcf65d221b50ab217090cd14e20270605edb39c25bc8b31feeb018d33e`  
		Last Modified: Wed, 21 Dec 2022 08:16:06 GMT  
		Size: 5.2 MB (5222792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e739742de4cf1cfc18dd35de6a2d89cf84f70a25c11a98f0eaf36f49f361da3`  
		Last Modified: Wed, 21 Dec 2022 08:16:03 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225b144e8741c3aa1654b9e756c1163012a7133cfa71acb3a176ff4916e6d300`  
		Last Modified: Wed, 21 Dec 2022 08:16:04 GMT  
		Size: 1.3 MB (1317490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9390a7a5c73370370acc5df34e33fdfa728cd180ecc00857322d40647264ac`  
		Last Modified: Wed, 21 Dec 2022 08:16:04 GMT  
		Size: 8.0 MB (8045183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ed003d23bc0f7b75bad91e29d839b1f9812da83cc13c9a0b2f51da4c74c2e1`  
		Last Modified: Wed, 21 Dec 2022 08:16:03 GMT  
		Size: 1.4 MB (1420094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90632af66009497caf6143ce29a90a26cc55e850ac4dfa7137e20e59d2a02ab1`  
		Last Modified: Wed, 21 Dec 2022 08:16:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21743c7d509464ed602260cf3266a2f6d24a7a3ec37f5f2a11defa35d2e1ca7`  
		Last Modified: Wed, 21 Dec 2022 08:16:01 GMT  
		Size: 3.2 KB (3205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407db0f307ecfcec1a98a4e6dd9afae13dc1f635c9f6052ca71c5ff7b3a3915e`  
		Last Modified: Wed, 21 Dec 2022 08:18:38 GMT  
		Size: 93.8 MB (93808157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1d57a17df197f72d67320d485d3832e53d38e512ee64ccfc3960aa529c348b`  
		Last Modified: Wed, 21 Dec 2022 08:18:14 GMT  
		Size: 9.0 KB (9023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f537cb37dec19fb6dd83c4d2fc58b1a9c46768c93db7abbdd936a647cbeabb`  
		Last Modified: Wed, 21 Dec 2022 08:18:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143737baa8fbfa781ffa1a5b5103786bfd9476e8c73620080541d9533cbee4bb`  
		Last Modified: Wed, 21 Dec 2022 08:18:14 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4166c3c01837b0756f562c1bfdf83830e6d1780e8ed5be58203ff79b2641f1da`  
		Last Modified: Thu, 22 Dec 2022 20:47:36 GMT  
		Size: 4.7 KB (4737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:1e4f9dc97467a4dfede7e2b08c94df2fe482743be82657335cb7e2ed99bba269
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139935553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dac77fbd07315eacf1a16e262006988f55c1697a7f636eecc27f4424056c892`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 07:50:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 07:50:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 21 Dec 2022 07:50:11 GMT
ENV GOSU_VERSION=1.14
# Wed, 21 Dec 2022 07:50:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 21 Dec 2022 07:50:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 21 Dec 2022 07:50:31 GMT
ENV LANG=en_US.utf8
# Wed, 21 Dec 2022 07:50:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 07:50:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 21 Dec 2022 07:50:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 21 Dec 2022 08:26:03 GMT
ENV PG_MAJOR=12
# Wed, 21 Dec 2022 08:26:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/12/bin
# Wed, 21 Dec 2022 08:26:03 GMT
ENV PG_VERSION=12.13-1.pgdg110+1
# Thu, 22 Dec 2022 20:13:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 22 Dec 2022 20:13:36 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 22 Dec 2022 20:13:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Dec 2022 20:13:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Dec 2022 20:13:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Dec 2022 20:13:38 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:43:34 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:43:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:43:34 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:43:35 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:43:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e0213fbd22db4d64f0d95b778a412ccc89ee69cb2ad61fcbfa108a6ed08a3e`  
		Last Modified: Wed, 21 Dec 2022 08:42:36 GMT  
		Size: 4.3 MB (4302292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632f331a99fae204bb82d8c753c51b887553cfa26915d1a3d3eb5ec9d76b2328`  
		Last Modified: Wed, 21 Dec 2022 08:42:36 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a279e9e3bfabe081fc8a8c13ec8c94cc8938ec09b50e3d1c74558a566e7313b`  
		Last Modified: Wed, 21 Dec 2022 08:42:36 GMT  
		Size: 1.4 MB (1381607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b86abbd23b530b5a8a19b73a405979da5bc3796641f3eb102bb4cae9294daa`  
		Last Modified: Wed, 21 Dec 2022 08:42:35 GMT  
		Size: 8.1 MB (8099235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4d9df5901b486724acc6ee053bfd87d60736a90c2494af6bc26dd0dfd8aaab`  
		Last Modified: Wed, 21 Dec 2022 08:42:34 GMT  
		Size: 1.2 MB (1237953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4839b18488c11ed1608dbdf8dfbc28ad3bbab88ed48050cbe9b86f95ac8b52`  
		Last Modified: Wed, 21 Dec 2022 08:42:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070f720510ae5f370dc5b6e7dd21bb6f542ff746a59e24630fcdf5ff8ac1c97a`  
		Last Modified: Wed, 21 Dec 2022 08:42:34 GMT  
		Size: 3.2 KB (3202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b17a758b1ee16d698fc32efa66feae98027a4320a673b27709ad29e52a821`  
		Last Modified: Thu, 22 Dec 2022 20:17:04 GMT  
		Size: 95.3 MB (95265410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266b62dca30d82956e7742de6f5f9222df32b94cccd3e68b7d3b9ec5fb04ec12`  
		Last Modified: Thu, 22 Dec 2022 20:16:52 GMT  
		Size: 9.0 KB (9029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3296c7424c23b8b832e5e367a53b36bad1a23f81d64c5dfda9bc32fc7ed11`  
		Last Modified: Thu, 22 Dec 2022 20:16:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae145d993aa572ee0dd929ee47f157baefd382bb2a92419c2fefc04576a8bb8e`  
		Last Modified: Thu, 22 Dec 2022 20:16:52 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a6e1f8bd4e3f79325bfe40fa35fcb9f3fec4939ccb2aa2a112dc39626aa1dd`  
		Last Modified: Thu, 22 Dec 2022 22:47:01 GMT  
		Size: 4.8 KB (4780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
