## `postgres:buster`

```console
$ docker pull postgres@sha256:1ee09d8a5bd9fe37e9c89c6ceba7e76299468590f67caff28d15abbe9d7d8b65
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

### `postgres:buster` - linux; amd64

```console
$ docker pull postgres@sha256:c3cfc3c00b2e54698907521ae817b26c84e3a109994f903d7130d22da87e93e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (114952483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29dd0a82ea2076bbb67f78d53236022b3d2968da639617860881d046b555e0c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 12:04:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 12:04:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 17 Aug 2021 12:04:22 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 12:04:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 12:04:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 17 Aug 2021 12:04:38 GMT
ENV LANG=en_US.utf8
# Tue, 17 Aug 2021 12:04:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 12:04:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 12:04:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 17 Aug 2021 12:05:18 GMT
ENV PG_MAJOR=13
# Tue, 17 Aug 2021 12:05:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 17 Aug 2021 12:05:19 GMT
ENV PG_VERSION=13.4-1.pgdg100+1
# Tue, 17 Aug 2021 12:05:36 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 17 Aug 2021 12:05:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 17 Aug 2021 12:05:39 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 17 Aug 2021 12:05:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 17 Aug 2021 12:05:39 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 17 Aug 2021 12:05:40 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 17 Aug 2021 12:05:40 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 12:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 12:05:40 GMT
STOPSIGNAL SIGINT
# Tue, 17 Aug 2021 12:05:40 GMT
EXPOSE 5432
# Tue, 17 Aug 2021 12:05:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab477c15ef75cadc3e27b36dcc2daf1e988cbb5d8640ebf696a5ebb3d9acb3be`  
		Last Modified: Tue, 17 Aug 2021 12:10:57 GMT  
		Size: 4.2 MB (4179246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fb2eb8fe368f1fb5a661527d29bb42c08f8d359a949f1100c1159a516e742a`  
		Last Modified: Tue, 17 Aug 2021 12:10:56 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f524381f883e5271ee1d409a0f7e29c9f04096a8bd620a87b7ef355602544cd7`  
		Last Modified: Tue, 17 Aug 2021 12:10:56 GMT  
		Size: 1.4 MB (1419372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6814a3f43c0002749cd40c0650bf7e24544901a195300985cfe48042049fdfca`  
		Last Modified: Tue, 17 Aug 2021 12:10:56 GMT  
		Size: 8.0 MB (7965271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efeb1f2150cf3acc43561ba3d295ad5b995df86d23b541a4f50025352622efb8`  
		Last Modified: Tue, 17 Aug 2021 12:10:53 GMT  
		Size: 391.2 KB (391211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7c6920299ddd085ae23aa50bc814fe78e51e07a9afadefadee741e6b55269e`  
		Last Modified: Tue, 17 Aug 2021 12:10:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f929d911a2e9b554b4d869de6f21ce204c5054ac4a81e719bc8d516d08185f`  
		Last Modified: Tue, 17 Aug 2021 12:10:53 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a961b3c2645a370f30ef7ed217d3234c35263648e82f92070f8ed44b4206a725`  
		Last Modified: Tue, 17 Aug 2021 12:11:23 GMT  
		Size: 73.8 MB (73832305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a89d8dadc7e30c538aca63c09024838a54f9f88e814dcfca43fe8b09bc2f6d`  
		Last Modified: Tue, 17 Aug 2021 12:11:13 GMT  
		Size: 9.4 KB (9357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca61de601d6ca4dc2a00fda1553d717d2eafc5a67db973767c91c203b71d579f`  
		Last Modified: Tue, 17 Aug 2021 12:11:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3fd90b1a40152a60cc803e9d48f711cd8c8010dd9ad207972c14f45b110bc2`  
		Last Modified: Tue, 17 Aug 2021 12:11:13 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ed85bb4f3ab313b59ece4fe8a693ffbbd20ed08003b49f9eb4fde501c03d43`  
		Last Modified: Tue, 17 Aug 2021 12:11:13 GMT  
		Size: 4.4 KB (4402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; arm variant v5

```console
$ docker pull postgres@sha256:3c47a8cda991faed0f5d57322871987f87d5ba5eb21635f9a5b4fa15ac0f3ca6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109142275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac6cbb50e001bec9c222e9e536c8889b5c14d0170c03ce98056b2f2ac0c5bcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 17 Aug 2021 01:56:50 GMT
ADD file:f29260935f1f8b3eef5eb0d5e49dd4cf5370e8731a3f4006d6023724bce09601 in / 
# Tue, 17 Aug 2021 01:56:51 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:02:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 13:02:41 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 17 Aug 2021 13:02:42 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 13:03:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 13:03:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 17 Aug 2021 13:03:32 GMT
ENV LANG=en_US.utf8
# Tue, 17 Aug 2021 13:03:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 13:03:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 13:03:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 17 Aug 2021 13:39:09 GMT
ENV PG_MAJOR=13
# Tue, 17 Aug 2021 13:39:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 17 Aug 2021 13:39:10 GMT
ENV PG_VERSION=13.4-1.pgdg100+1
# Tue, 17 Aug 2021 14:12:10 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 17 Aug 2021 14:12:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 17 Aug 2021 14:12:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 17 Aug 2021 14:12:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 17 Aug 2021 14:12:16 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 17 Aug 2021 14:12:17 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 17 Aug 2021 14:12:17 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 14:12:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 14:12:18 GMT
STOPSIGNAL SIGINT
# Tue, 17 Aug 2021 14:12:19 GMT
EXPOSE 5432
# Tue, 17 Aug 2021 14:12:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3dfab4a5b2accf2d709d8c7d14a42715948ecf2d6da4943a6e2c0de8ae7536a0`  
		Last Modified: Tue, 17 Aug 2021 02:12:42 GMT  
		Size: 24.9 MB (24879063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896ec01d55f1a7ed3559d1623903e3f6226b32e6d82c46599b7d37754cd78489`  
		Last Modified: Tue, 17 Aug 2021 17:26:51 GMT  
		Size: 3.8 MB (3848032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9d345ef7b2235f9288e2ecbee0f62650cc62b06b37847a3b9e23a9939d9fc5`  
		Last Modified: Tue, 17 Aug 2021 17:26:49 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6817d392da3f3a5395d93dff6dd0653a21ed83bdb4707c1174814c87db9646`  
		Last Modified: Tue, 17 Aug 2021 17:26:50 GMT  
		Size: 1.4 MB (1378683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474a825bba0253ee4e3b175d5f8a3fdb93570c515e0ec01d262f6a4d4eb5c98b`  
		Last Modified: Tue, 17 Aug 2021 17:26:53 GMT  
		Size: 8.0 MB (7965290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748485916536b3c1f45d8ba6904c671e430ad1af37b62aa590c8c2a7ef4d2dbf`  
		Last Modified: Tue, 17 Aug 2021 17:26:47 GMT  
		Size: 390.5 KB (390518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8ed4f354e3cd4fa2040861a0510746ef9a473d075538cac109f5d413d360ea`  
		Last Modified: Tue, 17 Aug 2021 17:26:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5955020c9c9aa2c64171d532a4378de72e6c85f01ce47a59c5b5e115dc852ec7`  
		Last Modified: Tue, 17 Aug 2021 17:26:47 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f805a01392da2631fec3543b0485d7b95a04df9f36216f36dbd716b4c26f77eb`  
		Last Modified: Tue, 17 Aug 2021 17:28:28 GMT  
		Size: 70.7 MB (70661598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d153b28639c24147a5088adabe51918ce501913343e8d1d3438daa78c0382db`  
		Last Modified: Tue, 17 Aug 2021 17:27:43 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5eee4525eacd4893068399b46fc73889eaa1bba4ec62967194479375fb1633`  
		Last Modified: Tue, 17 Aug 2021 17:27:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f63cb12874ac49c5a28ae17f8bce91fdc9996706c82d735eb1dbc7113ddee3a`  
		Last Modified: Tue, 17 Aug 2021 17:27:43 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9be7689a057222e47ee67fa37151e2778fa31809961deb545a9c6acf6f9726`  
		Last Modified: Tue, 17 Aug 2021 17:27:43 GMT  
		Size: 4.4 KB (4402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; arm variant v7

```console
$ docker pull postgres@sha256:25dc836731e49f32475ae91dcb65eddd1cefc3a96be3837dec4f05fa7b2f877a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105219562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187f3db701b1ae74034b1671b02afa22740bb2dbaaa5afeb8e24a350e5f01e83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:46 GMT
ADD file:8f466611d9ba85407e1768128a6a2a51886b78675a4775badb9d42e57c4a182e in / 
# Thu, 22 Jul 2021 02:03:47 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 17:02:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 17:02:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Jul 2021 17:02:31 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 17:02:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 17:03:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 22 Jul 2021 17:03:18 GMT
ENV LANG=en_US.utf8
# Thu, 22 Jul 2021 17:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:03:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 17:03:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jul 2021 17:36:04 GMT
ENV PG_MAJOR=13
# Thu, 22 Jul 2021 17:36:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Fri, 13 Aug 2021 01:21:00 GMT
ENV PG_VERSION=13.4-1.pgdg100+1
# Fri, 13 Aug 2021 01:50:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 13 Aug 2021 01:51:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 13 Aug 2021 01:51:01 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Aug 2021 01:51:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Aug 2021 01:51:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Aug 2021 01:51:04 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Aug 2021 01:51:04 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Fri, 13 Aug 2021 01:51:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Aug 2021 01:51:05 GMT
STOPSIGNAL SIGINT
# Fri, 13 Aug 2021 01:51:06 GMT
EXPOSE 5432
# Fri, 13 Aug 2021 01:51:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:607f77084e8a15bf45d56215b058a593cdcf4e0039e5326157954b12663c0d31`  
		Last Modified: Thu, 22 Jul 2021 02:16:17 GMT  
		Size: 22.7 MB (22745974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce89a6184ac9e93de6b3627911c27612f8b4ce551b9076cb2e25f11b93e86852`  
		Last Modified: Thu, 22 Jul 2021 21:06:15 GMT  
		Size: 3.5 MB (3481703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4e6e7ac86386fa5d134f745010d21e5d24c074de9522ebccc5d26cfcea6b25`  
		Last Modified: Thu, 22 Jul 2021 21:06:13 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f439172b723fa1e08e9a5e51ffad11c8e40e12d1ca92cfdeba32eee1c9ec`  
		Last Modified: Thu, 22 Jul 2021 21:06:14 GMT  
		Size: 1.4 MB (1370425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e803a3461b46c3448ae4e1fb44a4d23f4b422f24b53de5304f32b760e33980f`  
		Last Modified: Thu, 22 Jul 2021 21:06:17 GMT  
		Size: 8.0 MB (7965247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467430f26cab9018bcb5c86732715557438123173f1e8711259a9f65af70830a`  
		Last Modified: Thu, 22 Jul 2021 21:06:11 GMT  
		Size: 385.1 KB (385104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a81afc37621604d0cf199085c6aaee0b41400afc70ad1f4ac44897542295cee`  
		Last Modified: Thu, 22 Jul 2021 21:06:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ceea61b7b5c08921fa659f915c9995d7437d4422ca341c853acac7b13ae3504`  
		Last Modified: Thu, 22 Jul 2021 21:06:11 GMT  
		Size: 3.1 KB (3053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32852e0e56fe52a612bc17796de8b7ac750cd6d2c557831f864cb58fb24773b8`  
		Last Modified: Fri, 13 Aug 2021 05:13:02 GMT  
		Size: 69.3 MB (69252021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7266e1ef42e85474f7410c1aee8f5ab14b586d4ad1aee2bc6880d0f95c9ae298`  
		Last Modified: Fri, 13 Aug 2021 05:12:19 GMT  
		Size: 9.4 KB (9362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b413396f8dc322c88d70fce91eaf5800818886c4009576cc50cf9fc6c46f25`  
		Last Modified: Fri, 13 Aug 2021 05:12:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ab7586a8f5cc662bd93260f7d6d1bbe063809a3ab8d66fd86adbc5ed23ad5b`  
		Last Modified: Fri, 13 Aug 2021 05:12:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9be34592f2f10160fcdba4439296a0ced62e2b4b3d0b3dd1aa20dcaafdf916`  
		Last Modified: Fri, 13 Aug 2021 05:12:19 GMT  
		Size: 4.4 KB (4402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:cdfb8534db544030d01f296b60a4d71d2469bf169d4dad6ee3a6985ce032c7a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111276000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17633a8022b86ef41b4bdb11b495c3c29869e8cb11c5a53cabe2068f00e0d6a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:06:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 11:06:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 17 Aug 2021 11:06:22 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 11:06:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 11:06:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 17 Aug 2021 11:06:39 GMT
ENV LANG=en_US.utf8
# Tue, 17 Aug 2021 11:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:06:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 11:06:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 17 Aug 2021 11:07:21 GMT
ENV PG_MAJOR=13
# Tue, 17 Aug 2021 11:07:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 17 Aug 2021 11:07:22 GMT
ENV PG_VERSION=13.4-1.pgdg100+1
# Tue, 17 Aug 2021 11:07:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 17 Aug 2021 11:07:41 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 17 Aug 2021 11:07:42 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 17 Aug 2021 11:07:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 17 Aug 2021 11:07:42 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 17 Aug 2021 11:07:43 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 17 Aug 2021 11:07:43 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 11:07:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 11:07:43 GMT
STOPSIGNAL SIGINT
# Tue, 17 Aug 2021 11:07:43 GMT
EXPOSE 5432
# Tue, 17 Aug 2021 11:07:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bf3f67d6ca96dc95b202ee48fbbcf0d02e819b4da0dcd1d836dd6c6215160f`  
		Last Modified: Tue, 17 Aug 2021 11:41:27 GMT  
		Size: 4.2 MB (4170256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d1c84ba22f957237d008e1756628c95b2ed60a06ef83ba1e20f7b6eea2c67a`  
		Last Modified: Tue, 17 Aug 2021 11:41:26 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f675a50a6c7fe23de2d831a7b2a89c588be95fbebf7001dca83c07de2418fb3`  
		Last Modified: Tue, 17 Aug 2021 11:41:26 GMT  
		Size: 1.4 MB (1354275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54660a8e35ea5b031332e54bd70a174e1ac4fba6df2f098a2439805e512b85f4`  
		Last Modified: Tue, 17 Aug 2021 11:41:25 GMT  
		Size: 8.0 MB (7965128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb43ecf52b4e164b99e78f8f69fb3315ed51d0e7820a3d79fc52a2bb345e039`  
		Last Modified: Tue, 17 Aug 2021 11:41:23 GMT  
		Size: 389.4 KB (389399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d666763a327409554706c465ed23fe0af859c020c8fa41460f55e0907fda849c`  
		Last Modified: Tue, 17 Aug 2021 11:41:23 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3731addeaab23a33b5b1a6136a626726478fe2ecf45e10c0d77f8322f73b7b`  
		Last Modified: Tue, 17 Aug 2021 11:41:23 GMT  
		Size: 3.1 KB (3053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d64576d1a94a030119d01f8ca8b4a1bb893518ab54de675af6a0d50aab6460`  
		Last Modified: Tue, 17 Aug 2021 11:41:56 GMT  
		Size: 71.5 MB (71462777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48075d654b2b4a00884d06349356209acb8f5baff7054694f1e173f0209ca5dc`  
		Last Modified: Tue, 17 Aug 2021 11:41:46 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfd9fed15a722d5fb05fd228e3ff9c05cf9a218c8982cb0012e36f2b357c0ee`  
		Last Modified: Tue, 17 Aug 2021 11:41:45 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8725f0389ad34ff9c617675a3c453cf1deb1aabf6c8b9d1348bc5f86cfcb786`  
		Last Modified: Tue, 17 Aug 2021 11:41:45 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676fe2370d3f35fc93c26639abe4c3e276e1fe5142575051231b5904c2fcb3bb`  
		Last Modified: Tue, 17 Aug 2021 11:41:45 GMT  
		Size: 4.4 KB (4398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; 386

```console
$ docker pull postgres@sha256:d537ff333a303b4811458b592aaf6025f72e3c50a463ba8256a7ac7e084c66a8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115622269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26c9cda7cfd0116d6bfa2071c5076e785cc33bb53eb2dd511d9af045058fc70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 17 Aug 2021 01:41:16 GMT
ADD file:0418032b55cd0a6dd515ac277fb9f92354397503cab212d446d3a3d8c647a60f in / 
# Tue, 17 Aug 2021 01:41:17 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 13:06:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 13:06:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 17 Aug 2021 13:06:28 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 13:06:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 13:06:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 17 Aug 2021 13:06:45 GMT
ENV LANG=en_US.utf8
# Tue, 17 Aug 2021 13:06:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 13:06:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 13:06:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 17 Aug 2021 13:07:36 GMT
ENV PG_MAJOR=13
# Tue, 17 Aug 2021 13:07:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 17 Aug 2021 13:07:37 GMT
ENV PG_VERSION=13.4-1.pgdg100+1
# Tue, 17 Aug 2021 13:08:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 17 Aug 2021 13:08:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 17 Aug 2021 13:08:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 17 Aug 2021 13:08:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 17 Aug 2021 13:08:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 17 Aug 2021 13:08:11 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 17 Aug 2021 13:08:11 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 13:08:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 13:08:12 GMT
STOPSIGNAL SIGINT
# Tue, 17 Aug 2021 13:08:12 GMT
EXPOSE 5432
# Tue, 17 Aug 2021 13:08:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c1c94e1f2523d69effaa463d64fc9962cfc67e2a956f0476c94200e7cf19edf0`  
		Last Modified: Tue, 17 Aug 2021 01:50:57 GMT  
		Size: 27.8 MB (27797627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62100ad732783543439a73639989a4abdd73b2fc7452f4d32a5dbe390e4e8331`  
		Last Modified: Tue, 17 Aug 2021 13:17:33 GMT  
		Size: 4.5 MB (4543064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab988f65a5da871514f202ea0a7ef605c9b91e5e2f0744b0c7470dfbbd62400b`  
		Last Modified: Tue, 17 Aug 2021 13:17:30 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91add6665fa3f91e33299a6613974e5a019e968d83985a3f3b1b3df0c9ecb5ee`  
		Last Modified: Tue, 17 Aug 2021 13:17:31 GMT  
		Size: 1.4 MB (1389705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c2654a111a43252e2044a8cc9c9279eebedd6c2e7c089a5f68967760dd23d7`  
		Last Modified: Tue, 17 Aug 2021 13:17:32 GMT  
		Size: 8.0 MB (7965159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9431cf0c310dbf02724e68afbace9a0bca672289439332f6fc7274cb2443b995`  
		Last Modified: Tue, 17 Aug 2021 13:17:28 GMT  
		Size: 398.4 KB (398422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9361a868bbcda2871b405a5501127aa1b0e13c52754dd0f31792553a0de902c7`  
		Last Modified: Tue, 17 Aug 2021 13:17:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0e9c10fb0ab2f698984ab101fdee48805998327f9a9cf342a0e3b9ed2f2a38`  
		Last Modified: Tue, 17 Aug 2021 13:17:27 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c974b442713970302bfa07889ba0a3086ca2c26702a90eb33e352ff8e22d8`  
		Last Modified: Tue, 17 Aug 2021 13:18:27 GMT  
		Size: 73.5 MB (73509207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ceaa5d6ff0e7e6c058fd1a0d5724fa690d937deabfd5b4877204a42a8f8453e`  
		Last Modified: Tue, 17 Aug 2021 13:18:05 GMT  
		Size: 9.4 KB (9360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c053eec0b532333f5bcefdab2d046f11f2d9a9efeb3e4ab9302c21730dfa57`  
		Last Modified: Tue, 17 Aug 2021 13:18:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a54eb5c5f70fec06ba5551f260b4465b6822c1efdf380ecafeec5d458bb2094`  
		Last Modified: Tue, 17 Aug 2021 13:18:05 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023b0cb9f52fe63eb2fed9a82580ea71a53914f1ab5548b9556f9a37e98bcca0`  
		Last Modified: Tue, 17 Aug 2021 13:18:05 GMT  
		Size: 4.4 KB (4399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; mips64le

```console
$ docker pull postgres@sha256:758a8bae4a4961735f41a6672a6f3828e51218bf5d3c6173b81debd712a14488
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110544006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7276619653f5cc4708060670b15c5512f2192fd54678d5dbcb2a5a2b64d6306`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Jul 2021 00:09:45 GMT
ADD file:1f77b9001c4977ba733be674fc5eb4b85130f1dea8a7b39d545b70f9c107695f in / 
# Thu, 22 Jul 2021 00:09:46 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:39:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:39:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Jul 2021 01:39:32 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 01:39:53 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 01:40:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Thu, 22 Jul 2021 01:40:17 GMT
ENV LANG=en_US.utf8
# Thu, 22 Jul 2021 01:40:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 01:40:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Thu, 22 Jul 2021 02:35:00 GMT
ENV PG_MAJOR=13
# Thu, 22 Jul 2021 02:35:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 12 Aug 2021 21:28:35 GMT
ENV PG_VERSION=13.4-1.pgdg100+1
# Thu, 12 Aug 2021 22:19:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 12 Aug 2021 22:20:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 12 Aug 2021 22:20:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 12 Aug 2021 22:20:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Aug 2021 22:20:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 12 Aug 2021 22:20:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Aug 2021 22:20:07 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 12 Aug 2021 22:20:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Aug 2021 22:20:08 GMT
STOPSIGNAL SIGINT
# Thu, 12 Aug 2021 22:20:08 GMT
EXPOSE 5432
# Thu, 12 Aug 2021 22:20:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99ee621d0b0485e9de65aa19604aa2453d19ea7fc86b22c5b77c1bab74e3cb42`  
		Last Modified: Thu, 22 Jul 2021 00:16:11 GMT  
		Size: 25.8 MB (25812771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bdab2d9e59c21edd1c1ed0bea820a2a36710fcc1c0a6d961fba0c7efad807b`  
		Last Modified: Thu, 22 Jul 2021 06:18:12 GMT  
		Size: 4.2 MB (4182563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7a3c5aa51144f06d41e36683c8ae29232277fa464842101397bf326604a928`  
		Last Modified: Thu, 22 Jul 2021 06:18:08 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb3ff322b4196628a088eb24d6097ae3d02f39f6c215170f392ccc004067e0a`  
		Last Modified: Thu, 22 Jul 2021 06:18:09 GMT  
		Size: 1.3 MB (1307431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7dd8745bafd859db04d2d93d29427fc89e194645c925192cccb6f136fbba86c`  
		Last Modified: Thu, 22 Jul 2021 06:18:13 GMT  
		Size: 8.0 MB (7964681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96cf69995d3f6a8833e0d9393d42e971a906784d0bb9146a11c7746c1470c2f`  
		Last Modified: Thu, 22 Jul 2021 06:18:06 GMT  
		Size: 389.3 KB (389319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7686b9e71c1dcfc1a215d6be088aeb0bd3f4c4cd4a1467518375f21493bfdd72`  
		Last Modified: Thu, 22 Jul 2021 06:18:05 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7be36dd2ea53aebebb3a7888c9d5fd5fe13451c083b854294b15ade600647d`  
		Last Modified: Thu, 22 Jul 2021 06:18:05 GMT  
		Size: 3.1 KB (3055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0955adb6c1e159bd121c442a63ecff89dd1ea6a289bf69d9debe4150ad2e8a7f`  
		Last Modified: Fri, 13 Aug 2021 01:13:22 GMT  
		Size: 70.9 MB (70868230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90393175e9d72d7eb41121fe46109b067f31a5679ee2fa28fc2ba275bb05d32d`  
		Last Modified: Fri, 13 Aug 2021 01:12:34 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a67a4c12282c5dc0780dfed8778c2b197a56930631addc1a3db2d5735d6eea`  
		Last Modified: Fri, 13 Aug 2021 01:12:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f30c762164b3040a9107834dec0114f9364306d4456daaa3a184c84ef1b8d99`  
		Last Modified: Fri, 13 Aug 2021 01:12:34 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f9f73ac4716e7144aeacddcbee4b131ad83baed7d2e93e6a58fd7564ccaa9e`  
		Last Modified: Fri, 13 Aug 2021 01:12:34 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; ppc64le

```console
$ docker pull postgres@sha256:e11b8919e2c71a2d5a682ac4b4aad59e884145b3a5848699f3e00646df3784ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122225644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2325b6800b8cd40cf3b1597691409eb25030efb9c63a06dda8c656f1b540e260`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 17 Aug 2021 01:34:13 GMT
ADD file:8b9b12a994a2519f725d1ed1f4ab5a444665262678fd8e6c42cf78f32dacb7fa in / 
# Tue, 17 Aug 2021 01:34:20 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 18:19:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 18:19:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 17 Aug 2021 18:19:39 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 18:22:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 18:22:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 17 Aug 2021 18:22:49 GMT
ENV LANG=en_US.utf8
# Tue, 17 Aug 2021 18:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 18:23:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 18:23:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 17 Aug 2021 18:27:02 GMT
ENV PG_MAJOR=13
# Tue, 17 Aug 2021 18:27:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 17 Aug 2021 18:27:13 GMT
ENV PG_VERSION=13.4-1.pgdg100+1
# Tue, 17 Aug 2021 18:28:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 17 Aug 2021 18:28:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 17 Aug 2021 18:29:00 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 17 Aug 2021 18:29:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 17 Aug 2021 18:29:16 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 17 Aug 2021 18:29:51 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 17 Aug 2021 18:30:04 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 18:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 18:30:44 GMT
STOPSIGNAL SIGINT
# Tue, 17 Aug 2021 18:30:51 GMT
EXPOSE 5432
# Tue, 17 Aug 2021 18:30:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c3e09f0e3e7f6fcb741a4c9214b63e341e1d9b53d7689a5ad6ff640b61a82541`  
		Last Modified: Tue, 17 Aug 2021 01:48:22 GMT  
		Size: 30.6 MB (30553721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a225e0ac62af64b5019d8ddc836f1cb7868150fd74f1970b37d7c87550cc72e`  
		Last Modified: Tue, 17 Aug 2021 18:48:46 GMT  
		Size: 5.0 MB (4967478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a5f2c43b48bdef05864f762595627bc380b9a03324164c06ff568cf9d14ed9`  
		Last Modified: Tue, 17 Aug 2021 18:48:45 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3309536427efdb068ba68fced99a5c05b7cabd8933c1fc700086a182ec429adb`  
		Last Modified: Tue, 17 Aug 2021 18:48:45 GMT  
		Size: 1.3 MB (1338188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defa09deb8a7f2ad372316561cc06ade91735dfc7bad7a04472ccc374e53bd96`  
		Last Modified: Tue, 17 Aug 2021 18:48:44 GMT  
		Size: 8.0 MB (7965532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3038cf047ec330b82b7ca852ab784eca4656fcabe6c6e44d58de6413e13d5281`  
		Last Modified: Tue, 17 Aug 2021 18:48:42 GMT  
		Size: 397.2 KB (397181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a09a1b2bcebb6926afeb3686d62cc8eef40e26322063ad47c75d2d89f9219e`  
		Last Modified: Tue, 17 Aug 2021 18:48:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a5b25b0815020e4508241ec764b19524075ef5e22a765242380688bc30c130`  
		Last Modified: Tue, 17 Aug 2021 18:48:42 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5d24e0fb8bba6784fd62439352b8264172d0710a30ba7614ff91fb43b36f3b`  
		Last Modified: Tue, 17 Aug 2021 18:49:21 GMT  
		Size: 77.0 MB (76984433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd000a882ae39ea8c188b6e17f7aa2c7f095f55cbd96a9d6661f30fbc966d0bb`  
		Last Modified: Tue, 17 Aug 2021 18:49:07 GMT  
		Size: 9.4 KB (9362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4086a6c73fbbdbb86954a4737a44a40e04720c1c932a6ed00aaa961dd6393d1`  
		Last Modified: Tue, 17 Aug 2021 18:49:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9555d7b7785335e06f27d192dd8e9349fc225085d1e17b267eb522df81ded97c`  
		Last Modified: Tue, 17 Aug 2021 18:49:07 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe4ed388bd377ecaf498bae4e3771c2d85188049961c00b8fb254259568d7c9`  
		Last Modified: Tue, 17 Aug 2021 18:49:07 GMT  
		Size: 4.4 KB (4401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; s390x

```console
$ docker pull postgres@sha256:37f40645830fa489d0eb16373fd951fb6d760442cccc73c60ecda8f28aaab35c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113258455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504ff018181f2e5bff60ef7b64fc1006ee84d25f15b31aeb03f31dfff4265248`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 10:07:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 17 Aug 2021 10:07:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 17 Aug 2021 10:07:02 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 10:07:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 10:07:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 17 Aug 2021 10:07:25 GMT
ENV LANG=en_US.utf8
# Tue, 17 Aug 2021 10:07:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 10:07:29 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 10:07:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Tue, 17 Aug 2021 10:22:41 GMT
ENV PG_MAJOR=13
# Tue, 17 Aug 2021 10:22:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 17 Aug 2021 10:22:43 GMT
ENV PG_VERSION=13.4-1.pgdg100+1
# Tue, 17 Aug 2021 10:34:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 17 Aug 2021 10:34:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 17 Aug 2021 10:34:59 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 17 Aug 2021 10:35:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 17 Aug 2021 10:35:01 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 17 Aug 2021 10:35:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 17 Aug 2021 10:35:03 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Tue, 17 Aug 2021 10:35:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 10:35:04 GMT
STOPSIGNAL SIGINT
# Tue, 17 Aug 2021 10:35:05 GMT
EXPOSE 5432
# Tue, 17 Aug 2021 10:35:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44b8ee17e7ce84c9b2d2782fdbc4fc8e44281b0a7aff640c54d303cac229ddd`  
		Last Modified: Tue, 17 Aug 2021 11:19:14 GMT  
		Size: 4.1 MB (4060013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c18a3a4849ba01e02bdfb6e33d735da24acd497c717c92218f26cdde84ee110`  
		Last Modified: Tue, 17 Aug 2021 11:19:13 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85463deba1e7ffb80b834e8318fc69dcf4f95904a658b357a1ed47ae6b17be1d`  
		Last Modified: Tue, 17 Aug 2021 11:19:13 GMT  
		Size: 1.4 MB (1406166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a9cfeee8a34eb98aa5bdab75106750f2e4a5140d82b2dfe787b402bb3d0b3c`  
		Last Modified: Tue, 17 Aug 2021 11:19:13 GMT  
		Size: 8.0 MB (8019414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682aa38dee2662a7543ab17721781805f59bee672a5f4ee1ca9e145a55c6aa00`  
		Last Modified: Tue, 17 Aug 2021 11:19:11 GMT  
		Size: 388.4 KB (388381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f1e3f043909738474ae7da0cd5945367141b7d9be5e97c0ed85a3b7ab41a33`  
		Last Modified: Tue, 17 Aug 2021 11:19:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ef8341c4b191bc479a33d412441b9842111412833379c06bdd814bfb60a97c`  
		Last Modified: Tue, 17 Aug 2021 11:19:11 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5da361b878a53f07b70bf6bc6abca49b0ae027acb71eb01260760c00d25131`  
		Last Modified: Tue, 17 Aug 2021 11:19:37 GMT  
		Size: 73.6 MB (73604527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d980ea6ac9274866d65de5ad08cfc09792b87b520c9ed75ff90210111300c1`  
		Last Modified: Tue, 17 Aug 2021 11:19:28 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eab1182768a550afd08f680ecc2a477d99e5e199c944baed8ec6abf832f96b1`  
		Last Modified: Tue, 17 Aug 2021 11:19:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c0f9171be9cbaf60f6578593e4d8e9cc87a681432bea033456506deeb04aab`  
		Last Modified: Tue, 17 Aug 2021 11:19:29 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9539b675f4e853873ec9ec6eaf92f783218d75f7c24d7c9ea1b2c71b270a9979`  
		Last Modified: Tue, 17 Aug 2021 11:19:28 GMT  
		Size: 4.4 KB (4399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
