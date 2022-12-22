## `postgres:11-bullseye`

```console
$ docker pull postgres@sha256:7947d78c23e23641ce443b5578bb9e5dedf509f1a299f30da38c60df8555f62f
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

### `postgres:11-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:6b3ed3f3c4ae4b7523690059c0e5bd5b510d8dd61d14c99dac17572101ae8eba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135270808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f252b4372d3406d19e98ef8d0b1e03feecd761f27718635008bf7f821e1510b9`
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
# Wed, 21 Dec 2022 07:40:40 GMT
ENV PG_MAJOR=11
# Wed, 21 Dec 2022 07:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 21 Dec 2022 07:40:41 GMT
ENV PG_VERSION=11.18-1.pgdg110+1
# Wed, 21 Dec 2022 07:40:58 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 07:40:59 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 07:40:59 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 07:40:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 07:41:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 07:41:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 19:36:56 GMT
COPY file:bf069237372db04c7f7fa02783a028485929406470fe90a88fce22131d247679 in /usr/local/bin/ 
# Thu, 22 Dec 2022 19:36:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 19:36:56 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 19:36:57 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 19:36:57 GMT
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
	-	`sha256:e57cd32f11b85739fb2211b57a9fef96b5da3739d053316516d2d806f16e1a13`  
		Last Modified: Wed, 21 Dec 2022 07:43:57 GMT  
		Size: 88.7 MB (88715557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e41d6cec6c15b00c0f6523c123e303b9259c57ea0dfa26886ae6b3749b4248`  
		Last Modified: Wed, 21 Dec 2022 07:43:45 GMT  
		Size: 8.3 KB (8329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f134a8915595790cc7d3660e995145889d7353e25c0dfcbb65e120832e55c9a`  
		Last Modified: Wed, 21 Dec 2022 07:43:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05312cf36e04189ad4f63db2fd0f0def6b397f8df8a1335dac68c47b425ecc1`  
		Last Modified: Wed, 21 Dec 2022 07:43:45 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18981bd91cb1a6c67245c329478d302d978848f51f9b3645d947c6e0f966b65e`  
		Last Modified: Thu, 22 Dec 2022 19:39:31 GMT  
		Size: 4.7 KB (4731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:a4d344fb67a09ea4658063ac83b4da6b6a752a52c08529705bca5d402653f795
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128448995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d52cb4e4c17f4e81ff7c9f7bafee15bdf75b17345104abe0dbb0da6cf1923c2`
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
# Wed, 21 Dec 2022 05:42:33 GMT
ENV PG_MAJOR=11
# Wed, 21 Dec 2022 05:42:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 21 Dec 2022 05:42:34 GMT
ENV PG_VERSION=11.18-1.pgdg110+1
# Wed, 21 Dec 2022 05:56:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 05:56:36 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 05:56:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 05:56:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 05:56:37 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 05:56:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:49:00 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:49:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:49:01 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:49:01 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:49:01 GMT
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
	-	`sha256:7c3d9f886da4eb16e3e554684befa2f7aa018f442d23de8d433848a4930e3c9c`  
		Last Modified: Wed, 21 Dec 2022 06:00:34 GMT  
		Size: 84.8 MB (84750636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d7ca5968cc063b557729533c19a698d6dea0d8b514e51b40b1f1fbde5c1525`  
		Last Modified: Wed, 21 Dec 2022 06:00:18 GMT  
		Size: 8.3 KB (8337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a84ee9100d02808647d7236dbd81ca4e86b49e26f25518ac8b3a6b1217008f`  
		Last Modified: Wed, 21 Dec 2022 06:00:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a149b1f0d51c772ea25e57549a0106027f941749e5a1acce4b9bc5713044678`  
		Last Modified: Wed, 21 Dec 2022 06:00:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2a2bdd3af2c68ef4b1983dc478d3400e8b9dae50783db31476869c4924d822`  
		Last Modified: Thu, 22 Dec 2022 22:51:22 GMT  
		Size: 4.8 KB (4779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f06734c06caafaa7de0652366407fa6a358fb9f7fc17df2ff04e2a97595b4424
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123312862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec08bfd8a19e18a15a53edd9182aaa4c892833df1f8640edf15b5e71a092e37`
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
# Wed, 21 Dec 2022 06:54:01 GMT
ENV PG_MAJOR=11
# Wed, 21 Dec 2022 06:54:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 21 Dec 2022 06:54:01 GMT
ENV PG_VERSION=11.18-1.pgdg110+1
# Wed, 21 Dec 2022 07:06:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 07:06:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 07:06:42 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 07:06:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 07:06:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 07:06:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:37:32 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:37:32 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:37:32 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:37:32 GMT
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
	-	`sha256:691652f82c5d6f95e0f27b6535e58d2956839e79538165283541ead6fbdd811c`  
		Last Modified: Wed, 21 Dec 2022 07:11:49 GMT  
		Size: 82.5 MB (82466173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d750d0661e81932555603dbc63f66c4e8040b1859ee1f71ae72903f9b242af67`  
		Last Modified: Wed, 21 Dec 2022 07:11:35 GMT  
		Size: 8.3 KB (8329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba6ad891ef20f4fe8927bff875ecbefa03d41f59b45569d4b3ffe0973c06542`  
		Last Modified: Wed, 21 Dec 2022 07:11:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b791d3e0c159bc8f21308e50a6d4e8a521ba440fb26a46e2c428237bf2740bd3`  
		Last Modified: Wed, 21 Dec 2022 07:11:35 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde78d8c9bbc39c3fa98258cfd25da536a5e98f3b495b14b0614de746599412b`  
		Last Modified: Thu, 22 Dec 2022 22:41:58 GMT  
		Size: 4.8 KB (4779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d441b9602a754b6f853ef759bcd10af4a50cdfa118c327c2b3f1c0751162b975
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130351299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecafb05aaa223dc4bb86748a09fc99ac60dbd7273a9155053c5aff37a9fcbda3`
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
# Wed, 21 Dec 2022 14:15:24 GMT
ENV PG_MAJOR=11
# Wed, 21 Dec 2022 14:15:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 21 Dec 2022 14:15:24 GMT
ENV PG_VERSION=11.18-1.pgdg110+1
# Wed, 21 Dec 2022 14:15:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 14:15:41 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 14:15:41 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 14:15:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 14:15:42 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 14:15:42 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:46:58 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:46:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:46:59 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:46:59 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:46:59 GMT
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
	-	`sha256:d864eb7249b8a7c3985aac606dd37fea92275ffd232c711d66218a27b0e00e6a`  
		Last Modified: Wed, 21 Dec 2022 14:18:26 GMT  
		Size: 85.2 MB (85230735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c177520b67e9b3f7becc00051c00dded6f22df16fdf18f8373a4e12c149099`  
		Last Modified: Wed, 21 Dec 2022 14:18:17 GMT  
		Size: 8.3 KB (8325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4e312a845bcb1d76345ce1c767d205dd752b1e08616ef9009798964a5f8bad`  
		Last Modified: Wed, 21 Dec 2022 14:18:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a72cbdedaff876ef213d6bfbd8e07d429d531e53959d8155b89b5f7de22d53`  
		Last Modified: Wed, 21 Dec 2022 14:18:17 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1872cfb5dcbef9ca2a690eff093153bb0fa0523996e5c3ed2b74f4df1870a3`  
		Last Modified: Thu, 22 Dec 2022 22:49:35 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:9470b37bd427e6b3f1376955f9b00b6f7b6da6663713e417cec2beae25c001a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136758695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7dce6cc467d12f89dd9aeb5d4de677935257df3822e78063eafbd5475df7ad`
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
# Wed, 21 Dec 2022 06:05:37 GMT
ENV PG_MAJOR=11
# Wed, 21 Dec 2022 06:05:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 21 Dec 2022 06:05:39 GMT
ENV PG_VERSION=11.18-1.pgdg110+1
# Wed, 21 Dec 2022 06:17:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 06:17:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 06:17:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 06:17:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 06:18:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 06:18:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:41:41 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:41:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:41:42 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:41:43 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:41:44 GMT
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
	-	`sha256:502e46e0ff0a3588d3220e539c0685b7a04d72f370cc033c5382d811e8e1cccc`  
		Last Modified: Wed, 21 Dec 2022 06:22:10 GMT  
		Size: 89.3 MB (89300923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e0a9d841782780e33693dcc96aeebf36ae2c36ef989e572168a03570e69477`  
		Last Modified: Wed, 21 Dec 2022 06:21:59 GMT  
		Size: 8.3 KB (8329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e20721fea3e0d69e14e0ef2a63036d19e5a92d6ef9bb79f45c1fe352a960a76`  
		Last Modified: Wed, 21 Dec 2022 06:21:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4db5bdc2834ee23e4d514ba14ff7b202af5f1d99272b9bd472c8ada2711bdf1`  
		Last Modified: Wed, 21 Dec 2022 06:21:59 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c37d61fa127e3227eb7c054b33c455effdf8248170a7c4576176520b85d2c80`  
		Last Modified: Thu, 22 Dec 2022 22:45:35 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:f214bf667c1b19dfb9203965de948dad1312c339f402ffbdf4456890d703c96a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129637917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e968debedaafef34ae6a77db996d582e2ae7ab981240070d8457b8bd3e75535a`
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
# Wed, 21 Dec 2022 09:03:29 GMT
ENV PG_MAJOR=11
# Wed, 21 Dec 2022 09:03:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 21 Dec 2022 09:03:35 GMT
ENV PG_VERSION=11.18-1.pgdg110+1
# Wed, 21 Dec 2022 09:57:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 09:57:32 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 09:57:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 09:57:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 09:57:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 09:57:50 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:36:41 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:36:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:36:48 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:36:51 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:36:54 GMT
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
	-	`sha256:22b0b5a513d2eca212f5ca04c6ee52c7e9c26e13069304abc92c6f8bda4f497f`  
		Last Modified: Wed, 21 Dec 2022 10:04:40 GMT  
		Size: 85.4 MB (85372138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fb9d8b259d6479c50b628a088351ac2613ef80edc073d5473bf7f1bcb4a6d6`  
		Last Modified: Wed, 21 Dec 2022 10:03:44 GMT  
		Size: 8.3 KB (8334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd47675be1bfdcc5b209a03d6ed809ee7aa3097a03802a9c38fc50cbc10391b`  
		Last Modified: Wed, 21 Dec 2022 10:03:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1172be98ea967360f55d4bbef1f39dcdffef7102805bdaa615d06c565d2bc197`  
		Last Modified: Wed, 21 Dec 2022 10:03:44 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbdee8d7e84f13f413fe804467c403142d403fad3f75dc74df7134084ec22d2`  
		Last Modified: Thu, 22 Dec 2022 22:38:22 GMT  
		Size: 4.8 KB (4775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:7694265764e9bb3e100be0c515ff664b582d85c092f9998636ed8a2566c5a87f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144145890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52da39580518dc4857ce13bcbc410adfebce0489ff0ccf5de820bffa9eff3bbf`
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
# Wed, 21 Dec 2022 08:04:14 GMT
ENV PG_MAJOR=11
# Wed, 21 Dec 2022 08:04:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 21 Dec 2022 08:04:14 GMT
ENV PG_VERSION=11.18-1.pgdg110+1
# Wed, 21 Dec 2022 08:05:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 08:05:04 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 08:05:05 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 08:05:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 08:05:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 08:05:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 20:36:10 GMT
COPY file:bf069237372db04c7f7fa02783a028485929406470fe90a88fce22131d247679 in /usr/local/bin/ 
# Thu, 22 Dec 2022 20:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 20:36:11 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 20:36:11 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 20:36:12 GMT
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
	-	`sha256:e5f75611425075c00456354cdcedb16b64c2da730495af8eb60a42ed31e3fc20`  
		Last Modified: Wed, 21 Dec 2022 08:19:20 GMT  
		Size: 92.9 MB (92853037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d095a6d01103c8149ae94638c500b09d0b3c6f5ad6baa83aa4f8e8739dd1cf`  
		Last Modified: Wed, 21 Dec 2022 08:18:57 GMT  
		Size: 8.3 KB (8328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decd1cb106cc42053f3b7bf1f2904927c44d6c05b3ee2743ae17014a14592500`  
		Last Modified: Wed, 21 Dec 2022 08:18:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4269e45529219ac9a88e45c0f1cab55e192e31740c6085bcefff58eaeb61b5f`  
		Last Modified: Wed, 21 Dec 2022 08:18:57 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63a7da13f9869ff6c9ee6742e7d532751491c57682e26bc64c5c7c058804bd0`  
		Last Modified: Thu, 22 Dec 2022 20:47:54 GMT  
		Size: 4.7 KB (4737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:4d063c187a6530b18e07c1730ef5940c481c7326f060b2117a483dae3d0f34a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138876551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8620767e946dfc0f4f3b5a33bb803321bbd59a0dcb56f333fedb34bfa98c10`
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
# Wed, 21 Dec 2022 08:30:09 GMT
ENV PG_MAJOR=11
# Wed, 21 Dec 2022 08:30:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/11/bin
# Wed, 21 Dec 2022 08:30:11 GMT
ENV PG_VERSION=11.18-1.pgdg110+1
# Wed, 21 Dec 2022 08:40:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 21 Dec 2022 08:40:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 21 Dec 2022 08:40:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 21 Dec 2022 08:40:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 21 Dec 2022 08:40:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 21 Dec 2022 08:40:58 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Dec 2022 22:43:53 GMT
COPY file:d4c2ceee202d1390df115217c6e567abc1da7a31572f20a840d966332148ebe4 in /usr/local/bin/ 
# Thu, 22 Dec 2022 22:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Dec 2022 22:43:53 GMT
STOPSIGNAL SIGINT
# Thu, 22 Dec 2022 22:43:54 GMT
EXPOSE 5432
# Thu, 22 Dec 2022 22:43:54 GMT
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
	-	`sha256:1f89116aef4401e4d2cbea530ec96e6a947ee0ad6fbcaf81393c11644b5dc93f`  
		Last Modified: Wed, 21 Dec 2022 08:44:03 GMT  
		Size: 94.2 MB (94207108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ab51fd27824b591f57044b8b0d0347f5892e8a4cb6e4fec39db8c3ad95f7ed`  
		Last Modified: Wed, 21 Dec 2022 08:43:51 GMT  
		Size: 8.3 KB (8333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3003ff07462a4919cf3b2cde199c2b0fb4c28f37b4c7ff7388fb308c4c405d`  
		Last Modified: Wed, 21 Dec 2022 08:43:51 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570e98be86cabeb7474f7a18bda592e3617d30e5a730444d030176c8184592ea`  
		Last Modified: Wed, 21 Dec 2022 08:43:51 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4d2eb1c2740f0d3aa918d80c2caa7a0739eae3b1068698d5afa8d893256411`  
		Last Modified: Thu, 22 Dec 2022 22:47:23 GMT  
		Size: 4.8 KB (4774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
