## `postgres:10-stretch`

```console
$ docker pull postgres@sha256:c45380faa8f19a6b18ea885693a6dca8da7a3b49420682ed8b6e260d9904b01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `postgres:10-stretch` - linux; amd64

```console
$ docker pull postgres@sha256:29e643048dc946894eca94d2eab2c1f9a2e939e0661294ad7f44c3253a5c6fd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74101910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e72caba743b561cec2e1889ae3c80ff3d126aa720748ea797bb06736cab17f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 11 May 2022 01:22:15 GMT
ADD file:026b786cdb9bd5132e483b55e6486a88dc97cd0f1dca7a128c56975e912865c3 in / 
# Wed, 11 May 2022 01:22:15 GMT
CMD ["bash"]
# Wed, 11 May 2022 12:24:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 12:24:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 11 May 2022 12:24:15 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 May 2022 12:24:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 May 2022 12:24:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 11 May 2022 12:24:33 GMT
ENV LANG=en_US.utf8
# Wed, 11 May 2022 12:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 12:24:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 May 2022 12:24:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 May 2022 12:25:29 GMT
ENV PG_MAJOR=10
# Wed, 11 May 2022 12:25:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Wed, 18 May 2022 00:51:41 GMT
ENV PG_VERSION=10.21-1.pgdg90+1
# Wed, 18 May 2022 00:51:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 18 May 2022 00:51:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 18 May 2022 00:51:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 18 May 2022 00:51:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 18 May 2022 00:51:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 18 May 2022 00:51:57 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 18 May 2022 00:51:57 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Wed, 18 May 2022 00:51:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 18 May 2022 00:51:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 18 May 2022 00:51:57 GMT
STOPSIGNAL SIGINT
# Wed, 18 May 2022 00:51:57 GMT
EXPOSE 5432
# Wed, 18 May 2022 00:51:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d956d1d1888bd62aafc454609f2d7adc3a3ee5f9678bb80e4d9d27662c230884`  
		Last Modified: Wed, 11 May 2022 01:28:58 GMT  
		Size: 22.6 MB (22567372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d38a6d6dc2cf97b12bd91608ffbf5981803dfafad39a1cbb346fb5675aea8a5`  
		Last Modified: Wed, 11 May 2022 12:28:42 GMT  
		Size: 4.5 MB (4504008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be54560233f231fd4ac3e3f885899b0f98e1b3ef261e6d477c8b61569d1cc1e1`  
		Last Modified: Wed, 11 May 2022 12:28:40 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4d732b0710d28b3fb805d35cb3cb5d1efae28629b501600f0bd52212a72529`  
		Last Modified: Wed, 11 May 2022 12:28:41 GMT  
		Size: 1.4 MB (1379570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800077ca5ad1e65115b5feaf027255ae94411609cca53cc68df65d1856c73727`  
		Last Modified: Wed, 11 May 2022 12:28:39 GMT  
		Size: 6.2 MB (6185777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25ba21882ce5604cbc677fe2379cf892f9c4dfd35633c14edff5fdf05355363`  
		Last Modified: Wed, 11 May 2022 12:28:39 GMT  
		Size: 1.2 MB (1249933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d179a9f8acc69c51af21fa075876049cdd1f2ee90545926fd157251c9c8c7e7a`  
		Last Modified: Wed, 11 May 2022 12:28:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a607a1546a23fdc5d322003f62c0fac0f6e8ff30081cb8edda271617d4bacf8`  
		Last Modified: Wed, 11 May 2022 12:28:38 GMT  
		Size: 5.6 KB (5578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350896fc407f37e2cf792e9fc9567e93b1f4d89488e03f9e3feb0e6fbd2af67a`  
		Last Modified: Wed, 18 May 2022 01:00:46 GMT  
		Size: 38.2 MB (38194494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfdc68db7617084b59ee4b2f64f2a31f70b0e87fa6ce4300c1408ff1bd1ffbd`  
		Last Modified: Wed, 18 May 2022 01:00:38 GMT  
		Size: 8.1 KB (8070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d437cbce7acd4309d98e23af06377952e804a40190bb0e2178b4ac7f6dd6e8e`  
		Last Modified: Wed, 18 May 2022 01:00:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1f8a3b63b4fd77ff4fdda94eee6083cd303da504e1e9d25aaeb84f46515d83`  
		Last Modified: Wed, 18 May 2022 01:00:38 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3545013681b0a0cb174961e6c13589a2646a91c2b6534e6b3d12f4b69ae8a76f`  
		Last Modified: Wed, 18 May 2022 01:00:38 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96575b202bd527664476be0b1c2878787ddab7266d776f93f0fa8017f4fe71dd`  
		Last Modified: Wed, 18 May 2022 01:00:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; arm variant v5

```console
$ docker pull postgres@sha256:b83ee650da437c012a5e7aaac09367f0a74ebb0ff31c576efe5a4c6101b8a59a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71083217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9cf7653a3916e43ff4778f9dc7b12342bc1934f256d7a5e86b7d6fdceeb040`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 11 May 2022 00:56:06 GMT
ADD file:efd3ed6309109e633b701403f7004b3b175b74971a18b46b1d481f075dd5c8f5 in / 
# Wed, 11 May 2022 00:56:06 GMT
CMD ["bash"]
# Wed, 11 May 2022 22:33:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 22:33:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 11 May 2022 22:33:22 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 May 2022 22:33:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 May 2022 22:34:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 11 May 2022 22:34:14 GMT
ENV LANG=en_US.utf8
# Wed, 11 May 2022 22:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 22:34:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 May 2022 22:34:33 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 May 2022 23:25:19 GMT
ENV PG_MAJOR=10
# Wed, 11 May 2022 23:25:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Wed, 11 May 2022 23:25:20 GMT
ENV PG_VERSION=10.20-1.pgdg90+1
# Wed, 11 May 2022 23:51:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 11 May 2022 23:51:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 11 May 2022 23:51:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 11 May 2022 23:51:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 11 May 2022 23:51:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 11 May 2022 23:51:47 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 11 May 2022 23:51:47 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Wed, 11 May 2022 23:51:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 11 May 2022 23:51:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 23:51:50 GMT
STOPSIGNAL SIGINT
# Wed, 11 May 2022 23:51:50 GMT
EXPOSE 5432
# Wed, 11 May 2022 23:51:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cf06fd8914d4c16f6407e9b08c3fb21faf74781e70c848c5994854f41d186ade`  
		Last Modified: Wed, 11 May 2022 01:13:42 GMT  
		Size: 21.2 MB (21240674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2914c114ab9c321a27e1fa57202badc92bcce7b8df0881d2c05164879e00911e`  
		Last Modified: Wed, 11 May 2022 23:59:00 GMT  
		Size: 4.2 MB (4239521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a6964d4ac9093ebec3d435cef74361473ae4255edf496ddeb08d71c4642d23`  
		Last Modified: Wed, 11 May 2022 23:58:57 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be121304dd7931d8a2e034e5076e57f64f0f791cdc0b67ced08933e1441b919d`  
		Last Modified: Wed, 11 May 2022 23:58:58 GMT  
		Size: 1.3 MB (1344488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e6d98a8f348c427aff6067c94b66cd159d4f972aca6c73fec0ab01eb265c90`  
		Last Modified: Wed, 11 May 2022 23:59:01 GMT  
		Size: 6.2 MB (6185881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2b531a132f0a00889204721f01e72ef30b00ef0fa665e472b699083d2fdc46`  
		Last Modified: Wed, 11 May 2022 23:58:56 GMT  
		Size: 1.2 MB (1194897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715ebfd372c8ce71471b1febf5c0b856a07096e57e79ce00071c7238b8972449`  
		Last Modified: Wed, 11 May 2022 23:58:56 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a3517ba6fe10086449e5141940c07640d873a7e85c91c5991452dacb8f64ea`  
		Last Modified: Wed, 11 May 2022 23:58:55 GMT  
		Size: 5.6 KB (5583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54e90db09407ef5ae01d58f0a4f9b5e75cc6c954a18281ede25104dffd230ff`  
		Last Modified: Thu, 12 May 2022 00:00:46 GMT  
		Size: 36.9 MB (36856991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec9097e093d0e7211f0731de1047c2bd5356f357add4f67ee6681e21beab7a9`  
		Last Modified: Thu, 12 May 2022 00:00:18 GMT  
		Size: 8.1 KB (8074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc6cb0fd996a68a0dc5cb1ed649a8c517674702517b2ca4c27af7c25e5120ff`  
		Last Modified: Thu, 12 May 2022 00:00:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d72fecbd4410cd2e16d7320f3eecc5b6ea117ceb48b24ebbf2e3500fa852430`  
		Last Modified: Thu, 12 May 2022 00:00:18 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550a6340cfaf843811011454e4be8249ebedffd5d25803f45f8c1a5adefea46f`  
		Last Modified: Thu, 12 May 2022 00:00:18 GMT  
		Size: 4.7 KB (4708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c03e22dbd0151b8392e8ac3bb773c6131198fd263d5833ef23a8b95ba596a9`  
		Last Modified: Thu, 12 May 2022 00:00:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; arm variant v7

```console
$ docker pull postgres@sha256:0f5fd021e7b9da7fc9c3108981a23f6de18437be05d538b7257a9c9f7f23eb19
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67673479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec61f134dc914d9694adaf4a55ec435bd893e59305a0086e3ee251e1e3c3db6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 11 May 2022 01:55:08 GMT
ADD file:2053868b10dc5164f3fb9b77a89aafd3da73e08ef244700b78666cc3e0f05b0f in / 
# Wed, 11 May 2022 01:55:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 20:15:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 20:15:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 11 May 2022 20:15:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 May 2022 20:16:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 May 2022 20:16:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 11 May 2022 20:16:44 GMT
ENV LANG=en_US.utf8
# Wed, 11 May 2022 20:16:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 20:16:55 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 May 2022 20:16:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 May 2022 21:03:20 GMT
ENV PG_MAJOR=10
# Wed, 11 May 2022 21:03:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Wed, 11 May 2022 21:03:21 GMT
ENV PG_VERSION=10.20-1.pgdg90+1
# Wed, 11 May 2022 21:26:34 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 11 May 2022 21:26:36 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 11 May 2022 21:26:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 11 May 2022 21:26:38 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 11 May 2022 21:26:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 11 May 2022 21:26:40 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 11 May 2022 21:26:41 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Wed, 11 May 2022 21:26:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 11 May 2022 21:26:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 21:26:43 GMT
STOPSIGNAL SIGINT
# Wed, 11 May 2022 21:26:43 GMT
EXPOSE 5432
# Wed, 11 May 2022 21:26:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1b0318fd9d43e032add67ea408393c8e890c1ea4b437ecc600ea0107fa7de956`  
		Last Modified: Wed, 11 May 2022 02:11:56 GMT  
		Size: 19.4 MB (19359811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53046a866d15d4760eb4e4d14f27c1b78e934c27cdf23944451d04b2d5d472b`  
		Last Modified: Wed, 11 May 2022 21:35:48 GMT  
		Size: 3.9 MB (3875769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e46571f7c56a215c3c363ec526c456f0ad61f9eaa4d9c41c12ee81a04592f6`  
		Last Modified: Wed, 11 May 2022 21:35:45 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a019daa04d80334befd97fa82686e0e9df2676870c278d4b332246d8dad00e`  
		Last Modified: Wed, 11 May 2022 21:35:46 GMT  
		Size: 1.3 MB (1336149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3985436eaeb41f1e25c39ae7b9462582d4df1999fe5b744a692ff35e1559a19f`  
		Last Modified: Wed, 11 May 2022 21:35:48 GMT  
		Size: 6.2 MB (6185636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360adf5f64b18d48c2fbe179ef1e2e386824648a294bbeb4ac3f6721e33785de`  
		Last Modified: Wed, 11 May 2022 21:35:44 GMT  
		Size: 1.1 MB (1097138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1dc6d892dfb74ff216fc1576534d368daf3cadd4b74d601b039547c8c5d19f`  
		Last Modified: Wed, 11 May 2022 21:35:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb68343b7b2e633a105703194198bf67e264972a9a759b5f40c2ec7ba3162bd`  
		Last Modified: Wed, 11 May 2022 21:35:44 GMT  
		Size: 5.6 KB (5583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f389b973668e78c572d615faacf434337cb7ca2222b07475dbeb1923e6ab12`  
		Last Modified: Wed, 11 May 2022 21:37:37 GMT  
		Size: 35.8 MB (35798214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7957ee2b515032f2ff682851a7c65ebbb4faeb4d24af396514c39d9a12a987bc`  
		Last Modified: Wed, 11 May 2022 21:37:11 GMT  
		Size: 8.1 KB (8075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d35c4dfc0970a2e0ad952c7791aad2bb8be05ba7789cccd2262fa11a4ae8c7d`  
		Last Modified: Wed, 11 May 2022 21:37:11 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059a2a280cdfb58202f65d12594bf9a82ed98d54b0e7b49e347e95528dab3aae`  
		Last Modified: Wed, 11 May 2022 21:37:11 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9621a0fd69af1783c42499f1d9b4caf9009843b89302456e6a1ca3fe1bf84560`  
		Last Modified: Wed, 11 May 2022 21:37:11 GMT  
		Size: 4.7 KB (4707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c9433208f40577671fe7d0b6a6ca96b5e9c3387df9ec1ec9f895be4eb41d33`  
		Last Modified: Wed, 11 May 2022 21:37:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:af51019e271f33b0d591ed99fa3101a2fa04e7490f8e403d6dc886d2ea3bb12f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69980061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace11f0a706fb8b2f5c2deac0cf004f2606f2b696b86f057ac7a070ad4265050`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 11 May 2022 00:49:23 GMT
ADD file:2da23cbf134c6ddbf47e6a21fd94f5d08453f8ea5b6d8c101c8a55408e61162c in / 
# Wed, 11 May 2022 00:49:24 GMT
CMD ["bash"]
# Wed, 11 May 2022 07:56:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 07:56:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 11 May 2022 07:56:45 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 May 2022 07:56:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 May 2022 07:57:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 11 May 2022 07:57:05 GMT
ENV LANG=en_US.utf8
# Wed, 11 May 2022 07:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 07:57:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 May 2022 07:57:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 May 2022 08:07:30 GMT
ENV PG_MAJOR=10
# Wed, 11 May 2022 08:07:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Wed, 11 May 2022 08:07:32 GMT
ENV PG_VERSION=10.20-1.pgdg90+1
# Wed, 11 May 2022 08:16:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 11 May 2022 08:16:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 11 May 2022 08:16:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 11 May 2022 08:16:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 11 May 2022 08:16:18 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 11 May 2022 08:16:19 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 11 May 2022 08:16:21 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Wed, 11 May 2022 08:16:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 11 May 2022 08:16:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 08:16:23 GMT
STOPSIGNAL SIGINT
# Wed, 11 May 2022 08:16:24 GMT
EXPOSE 5432
# Wed, 11 May 2022 08:16:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:716cebb420f77090ed0f738eb4ff36a4aff63f4b8bd8ad1e9fa099b3e2a53961`  
		Last Modified: Wed, 11 May 2022 00:57:53 GMT  
		Size: 20.4 MB (20423950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f28654705d5e9bce15eebb9b1530263b0cad0c143ac5ac706e1ff205acbedf`  
		Last Modified: Wed, 11 May 2022 08:20:13 GMT  
		Size: 3.9 MB (3890906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53421761fcfb66be9fe86bc42c40a7652676b525748f32d94b83e6c5ceb863c3`  
		Last Modified: Wed, 11 May 2022 08:20:12 GMT  
		Size: 1.7 KB (1661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c5b23e6ad13d97bc4767064725465579719ede8c74b8666b2cf0235c283261`  
		Last Modified: Wed, 11 May 2022 08:20:12 GMT  
		Size: 1.3 MB (1307854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc7b1cb6e6f71857a848267d9ebf482f5b6a30d8d33b5a7ec52d6d735516dd3`  
		Last Modified: Wed, 11 May 2022 08:20:11 GMT  
		Size: 6.2 MB (6182598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e6e2b71348b7e8a25f8da45752d6931e3db480388daad7a1f0c8a05e55275b`  
		Last Modified: Wed, 11 May 2022 08:20:10 GMT  
		Size: 1.0 MB (1007512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ecbb71ad65e93d931ef51fa7a75eda676d1252ed3abf4c57774c7de597e682`  
		Last Modified: Wed, 11 May 2022 08:20:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7465da7e2008b84ca962be1eb1071a8ef5a2f368c0992e1e68c92c96f8e67cee`  
		Last Modified: Wed, 11 May 2022 08:20:10 GMT  
		Size: 5.5 KB (5527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7519ad938eaf1311164bb5638d144a55f35d61f4e4067e6482df85892dd6f733`  
		Last Modified: Wed, 11 May 2022 08:21:02 GMT  
		Size: 37.1 MB (37146737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c891ac33780987453923cae3cd9f3d12f4c1395e74ef0311b1317d8f87e021`  
		Last Modified: Wed, 11 May 2022 08:20:54 GMT  
		Size: 8.1 KB (8072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63892736825514a0ba1e18f63066b358a859848f63317da832407dbff487961`  
		Last Modified: Wed, 11 May 2022 08:20:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8f01510dfc1f991da08a4948a295f5ea3d80267e87e75f2869470850ae44f5`  
		Last Modified: Wed, 11 May 2022 08:20:54 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c94ffbccaff306e2036a66661531803fa45fe59e34dc0cc54aa1f51fd07382`  
		Last Modified: Wed, 11 May 2022 08:20:54 GMT  
		Size: 4.7 KB (4708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b989d49c00da2faeef1c4a0b112cf28529c2188b16ec57a00244076eda9d3d`  
		Last Modified: Wed, 11 May 2022 08:20:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-stretch` - linux; 386

```console
$ docker pull postgres@sha256:d2eb15fa0faa01b6047c2f154db69e863d2f2d3854732baaa8a611074bb0c037
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74841711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279ac4b506420d881100cbeb2d1a4a3eb96eb37f4ddd31bc96defe2320f2406c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 11 May 2022 01:41:44 GMT
ADD file:99bd3f1842fa0bf09a3c19b09bb2291aeaa26ba30f2704a7074d1e9c395e1bbb in / 
# Wed, 11 May 2022 01:41:45 GMT
CMD ["bash"]
# Wed, 11 May 2022 10:25:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 10:25:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 11 May 2022 10:25:12 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 May 2022 10:25:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 May 2022 10:25:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 11 May 2022 10:25:31 GMT
ENV LANG=en_US.utf8
# Wed, 11 May 2022 10:25:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 10:25:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 May 2022 10:25:41 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 May 2022 10:35:36 GMT
ENV PG_MAJOR=10
# Wed, 11 May 2022 10:35:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/10/bin
# Wed, 11 May 2022 10:35:37 GMT
ENV PG_VERSION=10.20-1.pgdg90+1
# Wed, 11 May 2022 10:35:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ stretch-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | i386 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 11 May 2022 10:35:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 11 May 2022 10:35:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 11 May 2022 10:35:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 11 May 2022 10:35:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 11 May 2022 10:35:59 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 11 May 2022 10:36:01 GMT
COPY file:3cf28939740c4fc7f2787c08c792133ea7778bcbe5a7254c7efea56f5632f447 in /usr/local/bin/ 
# Wed, 11 May 2022 10:36:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 11 May 2022 10:36:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 May 2022 10:36:03 GMT
STOPSIGNAL SIGINT
# Wed, 11 May 2022 10:36:04 GMT
EXPOSE 5432
# Wed, 11 May 2022 10:36:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d986b441a1343c1b3027f0fcd148ee0392ceb52fd4b1e8cfb0de32bd1f09938`  
		Last Modified: Wed, 11 May 2022 01:50:52 GMT  
		Size: 23.2 MB (23202360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2925ddaf5865bac82afd07560a9d73e804c381fcdb1e4fb8888e62c70fbc3b5`  
		Last Modified: Wed, 11 May 2022 10:39:34 GMT  
		Size: 4.6 MB (4623951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba85d252d8ec188f1813e53d252a519f99c808a3dc911f1d05637210f2de275b`  
		Last Modified: Wed, 11 May 2022 10:39:33 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040a84a65089a783b9cac1f0c73d7c2c6044b4a7e161fcca3e278f83763a615`  
		Last Modified: Wed, 11 May 2022 10:39:33 GMT  
		Size: 1.3 MB (1346969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9961ee93ed5243457f2054aa9a244e64bc881a2b17e60a8b5dfd116d577ba56`  
		Last Modified: Wed, 11 May 2022 10:39:32 GMT  
		Size: 6.2 MB (6182820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33333f21d0b5aafa403ef8c1ce7e2e00bd651a8cf2533061f1e1215b65d5e4f`  
		Last Modified: Wed, 11 May 2022 10:39:31 GMT  
		Size: 1.0 MB (1030547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9baae5be6dc2679245333b19d711f0252556d81233a753efc50c5bbbd9599664`  
		Last Modified: Wed, 11 May 2022 10:39:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2b9314e82cf0cb8daeeb233b2bc86ca21c93af5c4d8ff706964a9760de3bbb`  
		Last Modified: Wed, 11 May 2022 10:39:30 GMT  
		Size: 5.5 KB (5527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f7d2d884f5dfce59058cb084d5553a39c6958b70484ea393e7772666e3a2ab`  
		Last Modified: Wed, 11 May 2022 10:40:31 GMT  
		Size: 38.4 MB (38434573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54c07541d702512e17323abd1d1cc834d9e9c3f986afea77cdd924f1fe0e46e`  
		Last Modified: Wed, 11 May 2022 10:40:24 GMT  
		Size: 8.1 KB (8070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7b0409bf01320a42044ce77936330672631bb6959404bc0e883af156d68fd2`  
		Last Modified: Wed, 11 May 2022 10:40:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c0f4494d062408b69451ec397fdb47a1cdf6809ced5f87637edb649cf35f80`  
		Last Modified: Wed, 11 May 2022 10:40:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cdb84d5ffcbc399ebd62ff6f6fdfbb8ff842b5f8348c4365db980fa1ca7d0d`  
		Last Modified: Wed, 11 May 2022 10:40:24 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbac9c744a6d9ff715ed962667433698f0c3c2b4df7b32572878e4b5092e3976`  
		Last Modified: Wed, 11 May 2022 10:40:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
