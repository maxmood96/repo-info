## `postgres:16-bullseye`

```console
$ docker pull postgres@sha256:4096ff5ff30796545fa4977347f1d641d6be5f95b66d5cc604943ab9ebef45ae
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

### `postgres:16-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:f2df811ae9be11b24c4021a031e813f68557f6fa659437201511af22d47d23f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141213195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a614ceee094b33dfa4ccf164c68d54ae311aa8a6a2199c6728a48ea4c5c94e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 14:23:13 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 14:23:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 14:23:19 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 14:23:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 14:23:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 14:23:33 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 14:23:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 14:23:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 14:23:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 14:23:39 GMT
ENV PG_MAJOR=16
# Thu, 07 Sep 2023 14:23:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 15 Sep 2023 22:23:19 GMT
ENV PG_VERSION=16.0-1.pgdg110+1
# Fri, 15 Sep 2023 22:23:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 22:23:41 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 22:23:42 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 22:23:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 22:23:42 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 22:23:42 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 22:23:43 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 22:23:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 22:23:43 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 22:23:43 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 22:23:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109a7ddf1bac19161a48105feb68c7b04ddf1845a241f50884645b2e21fffa0f`  
		Last Modified: Thu, 07 Sep 2023 14:30:07 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f3f56119bdd28d10c57cdab715b0f94e0679bc4fe22a74c31b38707f685cec`  
		Last Modified: Thu, 07 Sep 2023 14:30:06 GMT  
		Size: 4.4 MB (4415040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2df7937fd911a95420a63e8fff99cc2ea86028bcd3e2a770628868f4a1b517`  
		Last Modified: Thu, 07 Sep 2023 14:30:06 GMT  
		Size: 1.5 MB (1471571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0ab32f40785aa27f46fd81933a5c09736584fa532980a1f581a01d9e867215`  
		Last Modified: Thu, 07 Sep 2023 14:30:05 GMT  
		Size: 8.0 MB (8045587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98bd85ddf81ea215a5ad1cfbdbb73d706b3cd3b70c9935f4d6212be72240e8ce`  
		Last Modified: Thu, 07 Sep 2023 14:30:04 GMT  
		Size: 1.3 MB (1261270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b11156967cfb55be4fd723803ac71fb44e027cba96098d37a8a98012e3424e`  
		Last Modified: Thu, 07 Sep 2023 14:30:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90521879f20bc16a06f6001899496eb14391034afacb7aa402eca101fcec90d6`  
		Last Modified: Thu, 07 Sep 2023 14:30:03 GMT  
		Size: 3.2 KB (3194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577629ef29c896c2022671be2493d80f4057f3a2ad7d2ad2de3464598f4acddd`  
		Last Modified: Fri, 15 Sep 2023 22:33:05 GMT  
		Size: 94.6 MB (94582046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07f864a1c71876d2ba99784367b0ffeb850d553562f287c86614117ebbe7a7`  
		Last Modified: Fri, 15 Sep 2023 22:32:53 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7461d8628e97ed21ce72358d7c950aff24309cc5a40de30e106fa174489165`  
		Last Modified: Fri, 15 Sep 2023 22:32:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec0d2502b51cf3ab95d2380b5599b46615241b2e9642ad68e5078924b4a3f37`  
		Last Modified: Fri, 15 Sep 2023 22:32:53 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762584270acbe49f0ef042f6f71c25e18f07294a4f7a7536b1a539a3484e05bf`  
		Last Modified: Fri, 15 Sep 2023 22:32:53 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:63530dc59ab2bccc298562565d5cc7289bff9f6d7b739bea7a9c56719f6cc1c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134474617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7783cb80f4d84c1dc756d5838408ba76441951cd004d79d62fa70a7268b9f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:48:46 GMT
ADD file:fb0679e6b5c5114176b186c73a97748a7712d856da24ce6f6aad2cd210825755 in / 
# Thu, 07 Sep 2023 00:48:47 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:11:38 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 03:11:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:11:47 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 03:11:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 03:12:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 03:12:05 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 03:12:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 03:12:15 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 03:12:16 GMT
ENV PG_MAJOR=16
# Thu, 07 Sep 2023 03:12:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 15 Sep 2023 22:59:09 GMT
ENV PG_VERSION=16.0-1.pgdg110+1
# Fri, 15 Sep 2023 23:14:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 23:14:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 23:14:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 23:14:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 23:14:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 23:14:26 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 23:14:27 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 23:14:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 23:14:27 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 23:14:27 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 23:14:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3c087ebb90b5f9b89ab4e03487d68bd9805afd41a68507381ba597291c3083d6`  
		Last Modified: Thu, 07 Sep 2023 00:52:19 GMT  
		Size: 28.9 MB (28919010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa03d871bf047315fefdfd7f33acdd8662b382c3b00512e7676495a3eda93bc8`  
		Last Modified: Thu, 07 Sep 2023 05:51:46 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb4ec0122a83e3e768e8972d25a95d5a47051c9314cf4119bf67408784a02fc`  
		Last Modified: Thu, 07 Sep 2023 05:51:46 GMT  
		Size: 4.1 MB (4096668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d955d99e75e0eeeb6afb7bfaa95bc31288f9fd364329fed91d914c20fca2c8c9`  
		Last Modified: Thu, 07 Sep 2023 05:51:45 GMT  
		Size: 1.4 MB (1448883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb2ae23e019dc3e5cdb2e4008503ed1d3a6d9b36bef6c5ea2477b7fede7f1f3`  
		Last Modified: Thu, 07 Sep 2023 05:51:46 GMT  
		Size: 8.0 MB (8045513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66eb904dfaab049680a12e030e52f89766cd57c38683277e5fa4a3a6cd51dfa`  
		Last Modified: Thu, 07 Sep 2023 05:51:43 GMT  
		Size: 1.3 MB (1257390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f970ee1beabe41d0ebf8219181497d95172c2d17059d7542a82bb7f2d0cadb5b`  
		Last Modified: Thu, 07 Sep 2023 05:51:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b543301196e06a575d5f82cf65e6f42ddc1a03b99fe88293c91eeaa7de2abebd`  
		Last Modified: Thu, 07 Sep 2023 05:51:42 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d373efeb757601d5c6c671ec8787f871a552f939e0b23d8714aedb8e66a1befb`  
		Last Modified: Fri, 15 Sep 2023 23:45:18 GMT  
		Size: 90.7 MB (90686968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c502ba0f9e01ba515101bb6a9fb7d773f68ecfbe8974bf2511f0495f80e7d7ed`  
		Last Modified: Fri, 15 Sep 2023 23:45:02 GMT  
		Size: 9.9 KB (9928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a923198aa0bc7848524caf305fc5bbfbff568cf9d5b65627796b1336a46f9d25`  
		Last Modified: Fri, 15 Sep 2023 23:45:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac1a6ba0dd9c557cdc90b7dbf6899b6fe3904fa0fa1b6722c56afd3bb7a02da`  
		Last Modified: Fri, 15 Sep 2023 23:45:02 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5496fc9c84ee1ed0a51093234649be7de0ca618f9fafebc4ff38a07214e76e77`  
		Last Modified: Fri, 15 Sep 2023 23:45:02 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:61a356779dfd966f5252bb5a56d09cd5f708b34ddd4740156370dacfbe00e85e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129104763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f5b82f838af250392b74062cef777d5b154a33ff6d96fa66ef79e5fcaedda3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:58:09 GMT
ADD file:d714939aacc810de397a02461ce4b9dd85e92783aff066bd3da685e3d2d97439 in / 
# Thu, 07 Sep 2023 00:58:10 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 04:27:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 04:27:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 04:27:17 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 04:27:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 04:27:33 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 04:27:33 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 04:27:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 04:27:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 04:27:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 04:27:40 GMT
ENV PG_MAJOR=16
# Thu, 07 Sep 2023 04:27:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 15 Sep 2023 22:38:00 GMT
ENV PG_VERSION=16.0-1.pgdg110+1
# Fri, 15 Sep 2023 22:51:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 22:51:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 22:51:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 22:51:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 22:51:43 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 22:51:44 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 22:51:44 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 22:51:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 22:51:44 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 22:51:44 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 22:51:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:323242406c24248128abc25e113055d272350b4ac4ecd985dbabfb7061c48d49`  
		Last Modified: Thu, 07 Sep 2023 01:03:12 GMT  
		Size: 26.6 MB (26578710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e8aab239bb85fd9d8959959a6618c6c567479d60c2676490d93667213cc58d`  
		Last Modified: Thu, 07 Sep 2023 06:56:07 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a16c2e61abc85a7be526ce4f71bec9e2061bb5d13c74f7f6e592479868cc0b`  
		Last Modified: Thu, 07 Sep 2023 06:56:07 GMT  
		Size: 3.7 MB (3717412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3e75d90e94b39bab44f1b37075dd18e64c34e4002a782d274078e8ec88a8bf`  
		Last Modified: Thu, 07 Sep 2023 06:56:06 GMT  
		Size: 1.4 MB (1438891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30731fa08c3b4d5af5bb23206acb944498d8e00b0eea4a9e44d91a084ae2b821`  
		Last Modified: Thu, 07 Sep 2023 06:56:06 GMT  
		Size: 8.0 MB (8045533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e49f21508789c22832cb0d1c5b3b0a844754fa25edb54b0c3f7a85c00b6a3b`  
		Last Modified: Thu, 07 Sep 2023 06:56:05 GMT  
		Size: 1.1 MB (1131259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9312e1b297f389d835004304afd0753a3c28aea63272f2715935e583fc370bd`  
		Last Modified: Thu, 07 Sep 2023 06:56:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d2068b512c24d8edd70cfccc9c1288a051378c4a9b02c0ea578f94c20e9cea`  
		Last Modified: Thu, 07 Sep 2023 06:56:04 GMT  
		Size: 3.2 KB (3192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3575cb4fa10d57c21a169e1f8db33614d4f7874b155624237f4435e4fcf4b4`  
		Last Modified: Fri, 15 Sep 2023 23:27:57 GMT  
		Size: 88.2 MB (88172785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d2adabba011dd0e8f294c9b616e102ece5ed0b07a409e6b61aafdc24dc57dc`  
		Last Modified: Fri, 15 Sep 2023 23:27:43 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d2574b9d41a925464599c923eb34166f7a98a9fbb357553b34b4ec21fd6b7`  
		Last Modified: Fri, 15 Sep 2023 23:27:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341685da6a120d20cc84695c8bbef037802eaa65cd2165edf3682e4134723ccb`  
		Last Modified: Fri, 15 Sep 2023 23:27:43 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a8dea1014ad51ffa156bdc93680b44256f41867998d435cda866f33edfa8b0`  
		Last Modified: Fri, 15 Sep 2023 23:27:43 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:805fa539a2c7d39f8f0ed144b1672098ae9814fc04b98eae6184c7c06f4ec25f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136261261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebe8360822d12f25ed9538603c3135d7cd15d20cb3f35ea37bfc4df973215d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 05:49:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 05:49:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:49:52 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 05:49:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 05:50:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 05:50:04 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 05:50:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 05:50:08 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 05:50:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 05:50:09 GMT
ENV PG_MAJOR=16
# Thu, 07 Sep 2023 05:50:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 15 Sep 2023 22:44:24 GMT
ENV PG_VERSION=16.0-1.pgdg110+1
# Fri, 15 Sep 2023 22:44:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 22:44:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 22:44:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 22:44:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 22:44:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 22:44:47 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 22:44:47 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 22:44:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 22:44:47 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 22:44:47 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 22:44:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59e190b947b378e3fbbbc1690a6925f948a412209e4a0c602a071ce29ca9beb3`  
		Last Modified: Thu, 07 Sep 2023 05:55:45 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bf0b3bd7f624ef660ad22e34f33c2662e0581ff8a9602e98f3f7569b734f79`  
		Last Modified: Thu, 07 Sep 2023 05:55:45 GMT  
		Size: 4.4 MB (4416320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc2b431b1550273c050253a1f28904e148f8afef4ba56a09b0beb0105f3aba6`  
		Last Modified: Thu, 07 Sep 2023 05:55:45 GMT  
		Size: 1.4 MB (1403318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78db74f8cf8106e2b37a738c8cd4988d8a7679565dd5a0a09e90aca578ee602`  
		Last Modified: Thu, 07 Sep 2023 05:55:44 GMT  
		Size: 8.0 MB (8045556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcc2743fb8b1d548e87bf097df355cfb81b81c5602c74ec1fed949df16b63c5`  
		Last Modified: Thu, 07 Sep 2023 05:55:43 GMT  
		Size: 1.2 MB (1249301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f4621a927785dd431ad5fe0590f0284f419ebb45ede55bc722902d3f7bc746`  
		Last Modified: Thu, 07 Sep 2023 05:55:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a54aa2b417f50ba29b985d62154b9165bc24548d9fb0964b72a084e482a58e`  
		Last Modified: Thu, 07 Sep 2023 05:55:43 GMT  
		Size: 3.2 KB (3198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc3f1bfb20fc8164af2cc653a56ee9b8a0aac3beed10e154095d61dfc0cb35b`  
		Last Modified: Fri, 15 Sep 2023 22:52:10 GMT  
		Size: 91.1 MB (91063679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61190da80e54375630492a3cd16914c4be948443ed33251031d6bf6e29eaa576`  
		Last Modified: Fri, 15 Sep 2023 22:52:02 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e26514970bcc2b50f83e41e7842bd74bf24e69e31d5ad6c3212c008cecf20a`  
		Last Modified: Fri, 15 Sep 2023 22:52:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4777669e20fd4c256f25984af54e9018e03bed326e122a93a1a7da1a51f3293b`  
		Last Modified: Fri, 15 Sep 2023 22:52:02 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f555cd7debb6effdfd35c983846a843e9ab3fdf2d94662bd0bad0fc3f7772191`  
		Last Modified: Fri, 15 Sep 2023 22:52:02 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:01bc9e11169cbbac74104ea464a890d252a2c7792542c5ce360cf7d083abe58b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143315721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ccf25cb3128608eb097a14b94dcd14d72b4b4368f259f883995a878acd1f4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:23 GMT
ADD file:7da3a32fda5f1208b9e4a0151bc02b156c151608c0a2c17b70ca382b4446d87f in / 
# Thu, 07 Sep 2023 00:39:24 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:29:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 01:29:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:29:34 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 01:29:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 01:29:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 01:29:52 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 01:29:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:29:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 01:29:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 01:29:59 GMT
ENV PG_MAJOR=16
# Thu, 07 Sep 2023 01:29:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 15 Sep 2023 22:43:48 GMT
ENV PG_VERSION=16.0-1.pgdg110+1
# Fri, 15 Sep 2023 23:03:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 23:03:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 23:03:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 23:03:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 23:03:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 23:03:24 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 23:03:24 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 23:03:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 23:03:25 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 23:03:25 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 23:03:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2508d8884943a2a8ff1cc6a8264b3085b7d7637e9de43269faf016019de5c311`  
		Last Modified: Thu, 07 Sep 2023 00:44:37 GMT  
		Size: 32.4 MB (32397335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74655300548258d7d25a328c0bffde08bed08c717de98f207d242c77bf5d14b2`  
		Last Modified: Thu, 07 Sep 2023 04:40:36 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149f9e39276753b35626d23a8eddc070887e3ac5589ed5e7b5d5880a6de76294`  
		Last Modified: Thu, 07 Sep 2023 04:40:37 GMT  
		Size: 4.8 MB (4813656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7907ad5c40789baddd839d2c311dab67e2cb2f0a9d6fa34a75c2fec78fc13f8c`  
		Last Modified: Thu, 07 Sep 2023 04:40:36 GMT  
		Size: 1.4 MB (1447125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6200fa51c3a49e06e95994515ae4ba82449632ef84569828f5a25fee8b9936`  
		Last Modified: Thu, 07 Sep 2023 04:40:36 GMT  
		Size: 8.0 MB (8045465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95726e25d4a4ae499c2adfa9a5b2f9269c200653b1e6efb566504c7003e260f`  
		Last Modified: Thu, 07 Sep 2023 04:40:34 GMT  
		Size: 1.3 MB (1251714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3301c04d87c5b94008e871f7874cc33ccfe5fc3a7a889e6fb75f4986cacdd2`  
		Last Modified: Thu, 07 Sep 2023 04:40:33 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98e073cab7e407921a11a8c0077a8650f69f363a19a92cf06772a24e4b2151a`  
		Last Modified: Thu, 07 Sep 2023 04:40:33 GMT  
		Size: 3.2 KB (3201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19052215aaec7cef57619fd3ff4190269b47272101a08870763ed5a3ec22f792`  
		Last Modified: Fri, 15 Sep 2023 23:55:31 GMT  
		Size: 95.3 MB (95340236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4a402249c79a92a1a8a3375f81ecef2d93a8c8a3cb6d2c50e5154aaf22c99f`  
		Last Modified: Fri, 15 Sep 2023 23:55:11 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1d1ba74b9e6906ad56f61d0daa53c043569d6f4a78e9d3e783e090f9126b4d`  
		Last Modified: Fri, 15 Sep 2023 23:55:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a28293c64bb8c97d6872022e6149a599bc03b7db5faf3d7d3d12e3f3f42a56f`  
		Last Modified: Fri, 15 Sep 2023 23:55:11 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c18e77fb46829ae581a3eaf2dcb7ebc478adcd7434ac59c4408fd665051b8b7`  
		Last Modified: Fri, 15 Sep 2023 23:55:11 GMT  
		Size: 4.8 KB (4794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:5edb42a533cd0361ab0f61541f8a830747887d44ac551353097f8a9cbc032068
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135562224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4929d8d8f869da66c8f45ec9fdf31f647b287ecb681c619c6b4b04f70505d707`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 01:10:26 GMT
ADD file:d38d449a8bdd452a8b7527e92adb18283eee35701f577c61deb4ab93f1b88721 in / 
# Thu, 07 Sep 2023 01:10:31 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 20:52:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 20:53:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 20:53:22 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 20:53:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 20:54:21 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 20:54:24 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 20:54:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 20:54:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 20:54:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 20:54:54 GMT
ENV PG_MAJOR=16
# Thu, 07 Sep 2023 20:54:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 15 Sep 2023 23:20:21 GMT
ENV PG_VERSION=16.0-1.pgdg110+1
# Sat, 16 Sep 2023 00:23:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Sat, 16 Sep 2023 00:23:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Sat, 16 Sep 2023 00:23:59 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 16 Sep 2023 00:24:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 16 Sep 2023 00:24:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 16 Sep 2023 00:24:12 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 16 Sep 2023 00:24:15 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Sat, 16 Sep 2023 00:24:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Sep 2023 00:24:21 GMT
STOPSIGNAL SIGINT
# Sat, 16 Sep 2023 00:24:25 GMT
EXPOSE 5432
# Sat, 16 Sep 2023 00:24:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:daedb7bf89cfe84a87bcfe1ba162d42f6ff21c2cb822f6199737968dee1ec769`  
		Last Modified: Thu, 07 Sep 2023 01:21:41 GMT  
		Size: 29.6 MB (29634539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24db17c5a45628d02b906593fd4c6e8bcda2fdf86793522f9e96c8584afb6f74`  
		Last Modified: Fri, 08 Sep 2023 07:47:40 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95687259bb0d5acfd39d6d7ff72b815606e1b6bb9ac96c47a3176a4d397161f7`  
		Last Modified: Fri, 08 Sep 2023 07:47:42 GMT  
		Size: 4.2 MB (4196306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2cb141e46d8d59ecb8fbf1ce4a746880cec4d0e6804a72028057b1c9789b5b`  
		Last Modified: Fri, 08 Sep 2023 07:47:40 GMT  
		Size: 1.4 MB (1358357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9859c88d53a0c022792d55095baf99e1d4d784ac05b989de675a3c02eab681d`  
		Last Modified: Fri, 08 Sep 2023 07:47:44 GMT  
		Size: 8.0 MB (8044133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472497b2a64d442c3c8a9b1129c464aabaa9e1610c55eba4d6df846a1382104d`  
		Last Modified: Fri, 08 Sep 2023 07:47:37 GMT  
		Size: 1.1 MB (1089514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7028d39043f5fb123fd08fa8798f2c2f475cb68deb10221f09bedffb753e4b95`  
		Last Modified: Fri, 08 Sep 2023 07:47:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d253ad0ed17e54cf4ec6e1797578e678b8755c5c39b186a17d1c4fdf8c495a`  
		Last Modified: Fri, 08 Sep 2023 07:47:36 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07c223ca97fcbb806f6d99ae84839a3e2de127e9c64d2d3973b2b2220f66a18`  
		Last Modified: Sat, 16 Sep 2023 02:33:56 GMT  
		Size: 91.2 MB (91219447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783553e911712c9d4e4e3cb46b910b9d3dd0a4a96f0daf0c68349eaec52130dd`  
		Last Modified: Sat, 16 Sep 2023 02:33:00 GMT  
		Size: 9.9 KB (9938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ba77ec67345894ee7808eb6582af393d8b690987a930f807d56e1b3c7f2d36`  
		Last Modified: Sat, 16 Sep 2023 02:33:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f8202bd53363a9480fdeee362b815f31505de4fc44b98490e159f599fde038`  
		Last Modified: Sat, 16 Sep 2023 02:33:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c513278a7d7fe0a73c514ce3ff9ba9ebaf6f227b4f8300ed5e97a46628d097b4`  
		Last Modified: Sat, 16 Sep 2023 02:33:00 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:47dd5b069d6d25d8ca68c263bda4e538cbcaeb0314c6a79ada5ed0d0b0a0a28b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150293672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a33f557c872dc092e90968e31dfc62281c4b31ee2d6078330223984ec10365`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:18:05 GMT
ADD file:bf50998bef8a71b4723f6c17cc5c3e929d9c3b7a71b56060fea91ea0cd3502c4 in / 
# Thu, 07 Sep 2023 00:18:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 16:27:39 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 16:27:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 16:27:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 16:28:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 16:28:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 16:28:31 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 16:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 16:28:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 16:28:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 16:28:46 GMT
ENV PG_MAJOR=16
# Thu, 07 Sep 2023 16:28:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 15 Sep 2023 22:53:31 GMT
ENV PG_VERSION=16.0-1.pgdg110+1
# Fri, 15 Sep 2023 22:55:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 22:55:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 22:55:18 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 22:55:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 22:55:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 22:55:29 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 22:55:31 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 22:55:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 22:55:35 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 22:55:36 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 22:55:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2365f3cb8bc5e18258159454852d941d92577738f79c1b5594afaec8481b47f3`  
		Last Modified: Thu, 07 Sep 2023 00:24:24 GMT  
		Size: 35.3 MB (35291070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c09abbdb9a4c91ed611264b43af95860c64c6e8ddc2c837fe5014b97b452d0`  
		Last Modified: Thu, 07 Sep 2023 16:42:47 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a99e6868ef28298f7180867a76c70a8d344204691f661dbb43eabb5591b282`  
		Last Modified: Thu, 07 Sep 2023 16:42:47 GMT  
		Size: 5.2 MB (5222924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a4e1a341ee4e6298d6f91e520f9004b397136fa55ec240cdf8334901ffb96e`  
		Last Modified: Thu, 07 Sep 2023 16:42:46 GMT  
		Size: 1.4 MB (1393372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5666274ad2e84c5c187905c411cf5320b04145f2a5e14a4259018d165ef34926`  
		Last Modified: Thu, 07 Sep 2023 16:42:47 GMT  
		Size: 8.0 MB (8045628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13eb1d789503af1457aae3e5f82e0501c6e2ae2b952c1d281dd2ad3e3d389fb`  
		Last Modified: Thu, 07 Sep 2023 16:42:44 GMT  
		Size: 1.4 MB (1420253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e26a7a977522e0d153f0d357a4dadc1b97dd24956fb7ad0a2a8c7411c9a0e4`  
		Last Modified: Thu, 07 Sep 2023 16:42:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ced060017cbf614a43fa5077d2ce9e2988ae44d9582bc890c372111a46cb4d9`  
		Last Modified: Thu, 07 Sep 2023 16:42:43 GMT  
		Size: 3.2 KB (3201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa17f44bc3b62dc07ba17ada2a70dbdc5f954f05a6974eb33bd4dc8e4c6e8656`  
		Last Modified: Fri, 15 Sep 2023 23:12:28 GMT  
		Size: 98.9 MB (98900226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a933c1e14b8a51dae62b5715ef0f7f0bd3a4f79a480303cd3d30f1ec04331b3`  
		Last Modified: Fri, 15 Sep 2023 23:12:06 GMT  
		Size: 9.9 KB (9932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298bfddb90d725f6952ecaf13ffa5e131fef9836c56664233dae213a5e08014a`  
		Last Modified: Fri, 15 Sep 2023 23:12:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b3dc40a0277aa0394eca3e2a936e874d866687c44fba8c5d16e8e1c829cfd8`  
		Last Modified: Fri, 15 Sep 2023 23:12:05 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea513aaf1b788702b2b4f43fa219c2150e59958fbd5feb636cfeb597e323fb7`  
		Last Modified: Fri, 15 Sep 2023 23:12:05 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:410bd449e682f2ab9314923e12d81eafccc15db6856fcba8b58b4484a8fba0c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144841897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb981a1f125e9795b0799d8246b4c23a18faad4ab9e1e5e975a325a2a35686e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 07 Sep 2023 00:44:33 GMT
ADD file:fb2f216acd6d0ecaf48e8d5dd7e3cdb5d1f51d414f2011ed318cb494f96d89ca in / 
# Thu, 07 Sep 2023 00:44:37 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:44:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 07 Sep 2023 09:44:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:44:25 GMT
ENV GOSU_VERSION=1.16
# Thu, 07 Sep 2023 09:44:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 07 Sep 2023 09:44:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 07 Sep 2023 09:44:37 GMT
ENV LANG=en_US.utf8
# Thu, 07 Sep 2023 09:44:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 09:44:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 07 Sep 2023 09:44:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 07 Sep 2023 09:44:42 GMT
ENV PG_MAJOR=16
# Thu, 07 Sep 2023 09:44:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 15 Sep 2023 22:23:54 GMT
ENV PG_VERSION=16.0-1.pgdg110+1
# Fri, 15 Sep 2023 22:24:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 15 Sep 2023 22:24:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 15 Sep 2023 22:24:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 15 Sep 2023 22:24:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 15 Sep 2023 22:24:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 15 Sep 2023 22:24:27 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 15 Sep 2023 22:24:27 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 15 Sep 2023 22:24:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Sep 2023 22:24:27 GMT
STOPSIGNAL SIGINT
# Fri, 15 Sep 2023 22:24:27 GMT
EXPOSE 5432
# Fri, 15 Sep 2023 22:24:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c9501ad9402d64e6c612fa1bb94f16df51188e681dc1f28c603a6109f06f22d7`  
		Last Modified: Thu, 07 Sep 2023 00:50:10 GMT  
		Size: 29.7 MB (29652801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8efb1996e11da0f41ea86848b3b858a7fdd88303aeee531b971eab856810b42`  
		Last Modified: Thu, 07 Sep 2023 09:55:08 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9959a0e2033ea5c43b1d0640311d4bd1c10ca5a0e8818be94a32775b8750d7f4`  
		Last Modified: Thu, 07 Sep 2023 09:55:08 GMT  
		Size: 4.3 MB (4302331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2560dc64da13f9ef0d0821359cccbdf84ccd36d205bffe91f53a92dc3a7d5da8`  
		Last Modified: Thu, 07 Sep 2023 09:55:07 GMT  
		Size: 1.4 MB (1437202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ffa7f2a3582d5a3bd20469e368f06fc436dd46b0a4a88b7a94d6466aee4cfe`  
		Last Modified: Thu, 07 Sep 2023 09:55:07 GMT  
		Size: 8.1 MB (8099363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c5c2daaec6e2c8f053b9b036bcf6179b8ff555d89f10ea516b444440808f38`  
		Last Modified: Thu, 07 Sep 2023 09:55:06 GMT  
		Size: 1.2 MB (1238061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b012427bafa1baca229e9dd76483cd11d634bb7a0b94b4d86876e424d41350`  
		Last Modified: Thu, 07 Sep 2023 09:55:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de58831f289aecce447398bfa7523efb4f620d3b04b326146db119c595760cf`  
		Last Modified: Thu, 07 Sep 2023 09:55:05 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8928212ba9b0bb5452628ff4bd5323aa8f2a4efbfda3c779e7300732081f0003`  
		Last Modified: Fri, 15 Sep 2023 22:35:54 GMT  
		Size: 100.1 MB (100091942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fbe409741a9a83dbf4e48f5b27d48b554fb1b2541f8ba3fe0912f34359c87d`  
		Last Modified: Fri, 15 Sep 2023 22:35:41 GMT  
		Size: 9.9 KB (9927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855b8a6b951dd265caa0d84b6517bcf7f33448609772175ca28d79cb7f7ed1cc`  
		Last Modified: Fri, 15 Sep 2023 22:35:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43386b88f04d590ef0f6707b73430436c5beda75e0d8b1dd7c54b865de50bad3`  
		Last Modified: Fri, 15 Sep 2023 22:35:41 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c78df1687b3ff57f56af1712ff3ff4d1b7b6f4c680f2ba3c57e51f492bf701`  
		Last Modified: Fri, 15 Sep 2023 22:35:41 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
