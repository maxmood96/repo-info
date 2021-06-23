## `postgres:buster`

```console
$ docker pull postgres@sha256:cb8a6e05ce3e0ee72a3e6f25c9a491b67910f246d270078fe7f0bb2f56b1ed49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
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
$ docker pull postgres@sha256:38039b3f2a0784a37244f557cf644a5cedc0c4269d14d9b09d089925586e8384
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114946009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36567eeafa19bf09a11b8f56e588bf7f338682d71afef1c9daa20db6868cc2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 01:21:22 GMT
ADD file:7362e0e50f30ff45463ea38bb265cb8f6b7cd422eb2d09de7384efa0b59614be in / 
# Wed, 12 May 2021 01:21:22 GMT
CMD ["bash"]
# Wed, 12 May 2021 14:33:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 14:33:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 12 May 2021 14:33:57 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 14:34:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 14:34:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 12 May 2021 14:34:21 GMT
ENV LANG=en_US.utf8
# Wed, 12 May 2021 14:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 14:34:29 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 14:34:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 12 May 2021 14:34:31 GMT
ENV PG_MAJOR=13
# Wed, 16 Jun 2021 22:24:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 16 Jun 2021 22:24:18 GMT
ENV PG_VERSION=13.3-1.pgdg100+1
# Wed, 16 Jun 2021 22:24:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 16 Jun 2021 22:24:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 16 Jun 2021 22:24:49 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 16 Jun 2021 22:24:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 16 Jun 2021 22:24:50 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 16 Jun 2021 22:24:50 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 16 Jun 2021 22:24:51 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 22:24:51 GMT
STOPSIGNAL SIGINT
# Wed, 16 Jun 2021 22:24:51 GMT
EXPOSE 5432
# Wed, 16 Jun 2021 22:24:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69692152171afee1fd341febc390747cfca2ff302f2881d8b394e786af605696`  
		Last Modified: Wed, 12 May 2021 01:27:20 GMT  
		Size: 27.1 MB (27145915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b993d5cc6e9a84a3130f78ebe55f65faa48be24f531c18c8ffaf47e241000`  
		Last Modified: Wed, 12 May 2021 14:40:05 GMT  
		Size: 4.2 MB (4179219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65921886500e967ceb3ecb351d57f7ff716ff2c80968c3ac9433f37aea25c53`  
		Last Modified: Wed, 12 May 2021 14:40:03 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c1a94e4ca8e4e20495b3293c3c3cfc71c6ceb8918a27ea0c34a3f056947198`  
		Last Modified: Wed, 12 May 2021 14:40:04 GMT  
		Size: 1.4 MB (1419400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dd99ceb686f66e94ad1dc9101faf039bc49863df13f9a2f5f84c0f2e95610`  
		Last Modified: Wed, 12 May 2021 14:40:03 GMT  
		Size: 8.0 MB (7965263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ee8e88c67c9c8fe47ad18c8699316478f3bd56f9f9d64ca6553ad9c1aee769`  
		Last Modified: Wed, 12 May 2021 14:40:01 GMT  
		Size: 391.2 KB (391212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b08674f9421970e07641cbbad748919e87c1e9589250e16adcb24b88e88387`  
		Last Modified: Wed, 12 May 2021 14:40:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d358e850d3e87346cf60611562e51226216d2192b71dc399ef9fab05e28e632`  
		Last Modified: Wed, 12 May 2021 14:40:01 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0e4d11f35122cc6fcc67bc893f6cd2935520f47fd807ff114f513ea9360d40`  
		Last Modified: Wed, 16 Jun 2021 22:38:08 GMT  
		Size: 73.8 MB (73825929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2609ba76e85be8a80965902e29f53b368e0b4e5a31bba1f54949419468bb29fb`  
		Last Modified: Wed, 16 Jun 2021 22:37:58 GMT  
		Size: 9.3 KB (9338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343d9dc54115660f21043c4a6cadec4fee192a36c14dcb1fec075f6b0c37e9b8`  
		Last Modified: Wed, 16 Jun 2021 22:37:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741e0010b238a56d68c968e619a5b9e003b941644062c1c6758ffbc42949a0d9`  
		Last Modified: Wed, 16 Jun 2021 22:37:58 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8993560d1eea4d02b29c1ad2fc2ea16683c4ee133cfbdf731db8fedc871e2c74`  
		Last Modified: Wed, 16 Jun 2021 22:37:58 GMT  
		Size: 4.4 KB (4401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; arm variant v5

```console
$ docker pull postgres@sha256:fb7ff4e89b7fb7ed9648c81a298b26904dc022052c39070b578471d3412c1b15
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109128285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0f5f8ee54923fed81df945009ed3fb801ba65f6284bdfae6e2473888d6e79d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 00:55:35 GMT
ADD file:241925c5ca73c99d58f93bc78d7c5bfb6f8b280201a9b55ade45ba0cc054c31d in / 
# Wed, 12 May 2021 00:55:46 GMT
CMD ["bash"]
# Wed, 16 Jun 2021 01:19:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Jun 2021 01:19:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 16 Jun 2021 01:19:11 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Jun 2021 01:19:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Jun 2021 01:19:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 16 Jun 2021 01:19:44 GMT
ENV LANG=en_US.utf8
# Wed, 16 Jun 2021 01:19:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Jun 2021 01:19:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Jun 2021 01:19:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 16 Jun 2021 01:19:55 GMT
ENV PG_MAJOR=13
# Wed, 16 Jun 2021 23:29:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 16 Jun 2021 23:29:29 GMT
ENV PG_VERSION=13.3-1.pgdg100+1
# Wed, 16 Jun 2021 23:44:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 16 Jun 2021 23:44:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 16 Jun 2021 23:44:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 16 Jun 2021 23:44:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 16 Jun 2021 23:44:05 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 16 Jun 2021 23:44:05 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 16 Jun 2021 23:44:05 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 23:44:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 23:44:06 GMT
STOPSIGNAL SIGINT
# Wed, 16 Jun 2021 23:44:06 GMT
EXPOSE 5432
# Wed, 16 Jun 2021 23:44:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:48885a8e20b16cb3bb9d2c3aafc7f040d8609844f69ca8482c42b4829d01b6da`  
		Last Modified: Wed, 12 May 2021 01:10:24 GMT  
		Size: 24.9 MB (24879601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96839a8af50d5993e4941636ec99d6a2c635203241a6fa300a56f5452b21e5b4`  
		Last Modified: Wed, 16 Jun 2021 02:48:00 GMT  
		Size: 3.8 MB (3848014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3e7181e51db3c7dda10708185c5f121b41710502f785d8a3d123bbacd6b560`  
		Last Modified: Wed, 16 Jun 2021 02:47:57 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b382e008baaadfaf278c37a0213e0bdb956fbe862d61aac7e7a0c924d06db4`  
		Last Modified: Wed, 16 Jun 2021 02:47:58 GMT  
		Size: 1.4 MB (1378636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9440b94fd26c601fa99c152fb74f21476fd3c5cd0b9e65cd1eac0fc7db1ba6be`  
		Last Modified: Wed, 16 Jun 2021 02:48:01 GMT  
		Size: 8.0 MB (7965245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6784db25ccf9b6b5183fc17f0e0a9eb92cea76b4701eeba5795f0047ea24595d`  
		Last Modified: Wed, 16 Jun 2021 02:47:55 GMT  
		Size: 390.4 KB (390426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4b83961ba29245b4b81823e7c5da894a79b4ec31167c2ed51fd7a3ac331461`  
		Last Modified: Wed, 16 Jun 2021 02:47:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4033563612369390bac66d37bb474315242eb932752344137cfe7bcd31cb0f`  
		Last Modified: Wed, 16 Jun 2021 02:47:54 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f383d57b361c5ab0982d7c31e557cc29307fa2235e190426c331c81c54268b9`  
		Last Modified: Thu, 17 Jun 2021 01:10:22 GMT  
		Size: 70.6 MB (70647285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efb45677fcf6590174056abd47107aaa96159371b7f8df9b8b8f34fc83f8818`  
		Last Modified: Thu, 17 Jun 2021 01:10:07 GMT  
		Size: 9.3 KB (9344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8204ac5c7fd0ee6ca017a5f1b00973518b84ebbbbca6e6ec46fe4230f7a0a89d`  
		Last Modified: Thu, 17 Jun 2021 01:10:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d523498fc35200684391554a16b32d9e5cb2a7d3e19daafa4e08dcc4e10884`  
		Last Modified: Thu, 17 Jun 2021 01:10:07 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b75beba0930f270dd64d1374dcfe7de292d36b77cdff5172cbd86022f0b3a11`  
		Last Modified: Thu, 17 Jun 2021 01:10:07 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; arm variant v7

```console
$ docker pull postgres@sha256:70de15e82d00d5a8b63a00df4806f3c567f32263435ccda3fab8cf0f54e7ddd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105202590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153b787fe442e72f88423721e13cc43a5237626b5db678acec93bdd4fbcd0c98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 01:03:14 GMT
ADD file:94bf2394dc26abd9f028c2933057a8673c8562e58ec4a0f51bb9bde0a5e4dee0 in / 
# Wed, 12 May 2021 01:03:32 GMT
CMD ["bash"]
# Wed, 16 Jun 2021 17:05:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 16 Jun 2021 17:05:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 16 Jun 2021 17:05:40 GMT
ENV GOSU_VERSION=1.12
# Wed, 16 Jun 2021 17:05:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 16 Jun 2021 17:06:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 16 Jun 2021 17:06:08 GMT
ENV LANG=en_US.utf8
# Wed, 16 Jun 2021 17:06:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Jun 2021 17:06:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Jun 2021 17:06:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 16 Jun 2021 17:06:17 GMT
ENV PG_MAJOR=13
# Thu, 17 Jun 2021 00:00:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 17 Jun 2021 00:00:20 GMT
ENV PG_VERSION=13.3-1.pgdg100+1
# Thu, 17 Jun 2021 00:14:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Thu, 17 Jun 2021 00:14:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Thu, 17 Jun 2021 00:14:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Jun 2021 00:14:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Jun 2021 00:14:04 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Jun 2021 00:14:04 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 17 Jun 2021 00:14:05 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Thu, 17 Jun 2021 00:14:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Jun 2021 00:14:05 GMT
STOPSIGNAL SIGINT
# Thu, 17 Jun 2021 00:14:05 GMT
EXPOSE 5432
# Thu, 17 Jun 2021 00:14:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3035777cd90a3389593bc49a7b39b6f67f9f2679f4e04cc59515f4d5f83ad818`  
		Last Modified: Wed, 12 May 2021 01:19:13 GMT  
		Size: 22.7 MB (22746266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781e8a2dd521ae1bb1175f3670daa6096d63240257fc5c0d9c4bfd48382bedf2`  
		Last Modified: Wed, 16 Jun 2021 18:31:41 GMT  
		Size: 3.5 MB (3481649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e8510c911d73570d80271300d25f2e67cb9fab8ec21fed40102300a039c46d`  
		Last Modified: Wed, 16 Jun 2021 18:31:40 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eed89b15b1003ef4de5c99674647bb3865018f111340d66ae8d6360ea52122`  
		Last Modified: Wed, 16 Jun 2021 18:31:40 GMT  
		Size: 1.4 MB (1370396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33a5b9a4afa27c81212c6bc749fceb2c0e4de0ecf8099f2b730e5014a515b5b`  
		Last Modified: Wed, 16 Jun 2021 18:31:41 GMT  
		Size: 8.0 MB (7965196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb6f6329508c731d2b049306a30e9effc838cbaece8f2ed1513ad9270245bf8`  
		Last Modified: Wed, 16 Jun 2021 18:31:38 GMT  
		Size: 385.1 KB (385077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1286560dd1d1f1cddda5fce28ce22c12ae8872a4ac5fd4d56464c01c2eeaab0c`  
		Last Modified: Wed, 16 Jun 2021 18:31:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f44160ef74c47548aeb4345b20c08453ec5765d3956d0b4f6053929fc4a0d6`  
		Last Modified: Wed, 16 Jun 2021 18:31:37 GMT  
		Size: 3.1 KB (3056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272c58260d29c1b2c1ef48b2df06a938ee5d62d36c8bd8045859e8b1b830baf7`  
		Last Modified: Thu, 17 Jun 2021 01:41:45 GMT  
		Size: 69.2 MB (69234919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4933591eaac4ac78a6c6cc5d677d88ca3b5f18d2e6c50840f5302f4f8869d113`  
		Last Modified: Thu, 17 Jun 2021 01:41:30 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c458dfb2f16e55c297ba5d2f3f889dd360addfc8075aa8cb8f861849c88da3b0`  
		Last Modified: Thu, 17 Jun 2021 01:41:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e109cbf051c099d072cf3dad47562e6b6011ab0393db7cfa37820135b9ea29e9`  
		Last Modified: Thu, 17 Jun 2021 01:41:31 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d417b073b29cc2bed988b4e70cec8523f8c06e9abde4bc4df6f97cc4323370`  
		Last Modified: Thu, 17 Jun 2021 01:41:30 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:179c9da75dee161350afd9c3e50528855dc6ee7d5063028a39854a4eafa06cf4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.3 MB (111255840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24ddd78d62db61600c9dd3c64efa79bb2c7d906da1503a7b9255aafa39146d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Jun 2021 23:49:40 GMT
ADD file:beee00b59da720f68e12e2ba2a8134207c80c777ddb4ceb03c71e3e4c3f51c93 in / 
# Tue, 22 Jun 2021 23:49:40 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 08:00:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 08:00:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 23 Jun 2021 08:00:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 23 Jun 2021 08:01:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 23 Jun 2021 08:01:10 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 23 Jun 2021 08:01:11 GMT
ENV LANG=en_US.utf8
# Wed, 23 Jun 2021 08:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 08:01:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Jun 2021 08:01:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 23 Jun 2021 08:01:17 GMT
ENV PG_MAJOR=13
# Wed, 23 Jun 2021 08:01:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 23 Jun 2021 08:01:18 GMT
ENV PG_VERSION=13.3-1.pgdg100+1
# Wed, 23 Jun 2021 08:01:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 23 Jun 2021 08:01:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 23 Jun 2021 08:01:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 23 Jun 2021 08:01:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 23 Jun 2021 08:01:41 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 23 Jun 2021 08:01:41 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 23 Jun 2021 08:01:41 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 23 Jun 2021 08:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Jun 2021 08:01:42 GMT
STOPSIGNAL SIGINT
# Wed, 23 Jun 2021 08:01:42 GMT
EXPOSE 5432
# Wed, 23 Jun 2021 08:01:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:448f6bf000e31217a7c202c659b03b7f8ac8d3ae6b03ef7a2f8339be2f00ff4a`  
		Last Modified: Tue, 22 Jun 2021 23:55:25 GMT  
		Size: 25.9 MB (25914993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac3c0fe3ab17bfa4c3c1f905b67e705dd622e5b719250a3707da3275f6427c`  
		Last Modified: Wed, 23 Jun 2021 08:43:51 GMT  
		Size: 4.2 MB (4170280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4262cf38624a63127b9f8a869b2008bbbc19d68f64ea18a57e1a571a2ac4758a`  
		Last Modified: Wed, 23 Jun 2021 08:43:50 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa7b7e739f9235bd376773e956230ce34be4fee1ac7515b4b061e692e5bcbbd`  
		Last Modified: Wed, 23 Jun 2021 08:43:50 GMT  
		Size: 1.4 MB (1354308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b13a00ff8f5091034119a7504c90c399e5a944d7a4046a7d1de913d3af5d07`  
		Last Modified: Wed, 23 Jun 2021 08:43:50 GMT  
		Size: 8.0 MB (7965162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6582bc95f89c2fffbd09f50933c184070070b2f05ec18079f9253705c81aec`  
		Last Modified: Wed, 23 Jun 2021 08:43:48 GMT  
		Size: 389.4 KB (389428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9731edaa8053d4c7628e5bac8a251b7afd2831aea1b9cf30a41521f2684fd9a4`  
		Last Modified: Wed, 23 Jun 2021 08:43:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7234d2c24f1fc9041caf2d2a5c9adc28a2b7132cb90abcee81043b07965f747a`  
		Last Modified: Wed, 23 Jun 2021 08:43:48 GMT  
		Size: 3.1 KB (3056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1f48b202f29ad475cacd4701c2c46ade4f64e73c664d4e32be426474dc7eef`  
		Last Modified: Wed, 23 Jun 2021 08:43:56 GMT  
		Size: 71.4 MB (71442583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f950a2de470c59f7b830c09ad984d733e07fa1495d332438e7acb6ddfe422528`  
		Last Modified: Wed, 23 Jun 2021 08:43:45 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c9a4ff023ad28cafcbe5d26e6514eae14b54e825709756197bd4877cd9aff`  
		Last Modified: Wed, 23 Jun 2021 08:43:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46951b2fbe4f35611bd81c16c7145a0656fab4d682f56c1a5a2c0f7a3cd0f986`  
		Last Modified: Wed, 23 Jun 2021 08:43:45 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa0ea7ec16980c2ab5c6a004d4518026f50ae7fed138cfadeedecb054a679e6`  
		Last Modified: Wed, 23 Jun 2021 08:43:45 GMT  
		Size: 4.4 KB (4401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; 386

```console
$ docker pull postgres@sha256:82c8f43263694eae073783f0314ac15c4a93053a808815aa9549ce2c201cad07
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115615200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185c3d4070704c8e9084ba2cefc3e2d74d2f36e9c28d99b3f7e57ca071b12f4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 00:39:52 GMT
ADD file:62173a7456d614031a7b20be741983644d9723c734eee663b099ad6b47af7b35 in / 
# Wed, 12 May 2021 00:39:53 GMT
CMD ["bash"]
# Wed, 12 May 2021 17:08:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 17:08:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 12 May 2021 17:08:53 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 17:09:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 17:09:11 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 12 May 2021 17:09:12 GMT
ENV LANG=en_US.utf8
# Wed, 12 May 2021 17:09:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:09:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 17:09:19 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 12 May 2021 17:09:19 GMT
ENV PG_MAJOR=13
# Wed, 16 Jun 2021 23:08:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 16 Jun 2021 23:08:05 GMT
ENV PG_VERSION=13.3-1.pgdg100+1
# Wed, 16 Jun 2021 23:08:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 16 Jun 2021 23:08:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 16 Jun 2021 23:08:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 16 Jun 2021 23:08:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 16 Jun 2021 23:08:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 16 Jun 2021 23:08:30 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 16 Jun 2021 23:08:30 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 23:08:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 23:08:31 GMT
STOPSIGNAL SIGINT
# Wed, 16 Jun 2021 23:08:31 GMT
EXPOSE 5432
# Wed, 16 Jun 2021 23:08:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9b548256784c8e079e5953ec08bd26ce8cbaed0d606a5d350b4bcd12710d2192`  
		Last Modified: Wed, 12 May 2021 00:46:39 GMT  
		Size: 27.8 MB (27795074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575d2475eb150e7d16bbcdfa247b6f1a3aa6a73693f94eb289f098327fb89bb9`  
		Last Modified: Wed, 12 May 2021 17:15:20 GMT  
		Size: 4.5 MB (4543045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b434d866cd5570a22a7a52ded13a7856fcb343a6d230820fb0022fa841e62363`  
		Last Modified: Wed, 12 May 2021 17:15:18 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffb0fa0b2256116815de20a50cb376412fa098595414c406aeef9c597ee16bb`  
		Last Modified: Wed, 12 May 2021 17:15:18 GMT  
		Size: 1.4 MB (1389738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a94ef8cc2afab34e9eb1f1310432c84a8e2bbc1dd48ab64ab9644b8e6982b23`  
		Last Modified: Wed, 12 May 2021 17:15:19 GMT  
		Size: 8.0 MB (7965150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35d27ddd9d107742d4a8ea8fac6ae5d63fc2a680336806633d79d50521f060f`  
		Last Modified: Wed, 12 May 2021 17:15:16 GMT  
		Size: 398.4 KB (398431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bbcb1012cb3c455f850f3efd71c7fa5d6afbd02c9185fb86240c0e64691863`  
		Last Modified: Wed, 12 May 2021 17:15:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a2d9f699733f0ae6ccc320aa99942739cc83b870955e475870edd0adf767d6`  
		Last Modified: Wed, 12 May 2021 17:15:15 GMT  
		Size: 3.1 KB (3053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff7c55a57db4fbb15f0ed4ccd7e4abb335d2f4e6b24966a7b83f414db3cfe54`  
		Last Modified: Wed, 16 Jun 2021 23:24:01 GMT  
		Size: 73.5 MB (73504690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6829e842cf5796e2bca02798f6a324481603adf9ec908f83bc1602de0b990e1f`  
		Last Modified: Wed, 16 Jun 2021 23:23:46 GMT  
		Size: 9.3 KB (9343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f382c89f929f0e0dea9c2314e83ce45dec0ca6fcb0a2f24bbec17407ebbcb9d7`  
		Last Modified: Wed, 16 Jun 2021 23:23:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc6e2d29f089ca72324018e54d8c45a741e6fa1a85c26da945727dd3232d310`  
		Last Modified: Wed, 16 Jun 2021 23:23:46 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d288630c724e1c4f976aa7a154e1549a78e919477292a763d844dd35b8b33eae`  
		Last Modified: Wed, 16 Jun 2021 23:23:45 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; mips64le

```console
$ docker pull postgres@sha256:34a1214a1e714f429737206b4b9ea3b1413be34675d6e2eee04e35e3ed8b3b6f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.5 MB (110527461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78dd63d908d9c6bd3b7c9865bb16d3ccf65641c72839921e2ea03c759868e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 12 May 2021 01:09:45 GMT
ADD file:867397d3fb44b3b936a4ff02bbc3a1b760fb6865b5a85efab82fff224f704241 in / 
# Wed, 12 May 2021 01:09:46 GMT
CMD ["bash"]
# Wed, 12 May 2021 12:50:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 12:50:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 12 May 2021 12:51:00 GMT
ENV GOSU_VERSION=1.12
# Wed, 12 May 2021 12:51:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 May 2021 12:51:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 12 May 2021 12:51:45 GMT
ENV LANG=en_US.utf8
# Wed, 12 May 2021 12:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 12:52:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 May 2021 12:52:02 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 12 May 2021 12:52:03 GMT
ENV PG_MAJOR=13
# Wed, 16 Jun 2021 22:07:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 16 Jun 2021 22:07:42 GMT
ENV PG_VERSION=13.3-1.pgdg100+1
# Wed, 16 Jun 2021 22:59:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 16 Jun 2021 22:59:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 16 Jun 2021 22:59:28 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 16 Jun 2021 22:59:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 16 Jun 2021 22:59:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 16 Jun 2021 22:59:31 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 16 Jun 2021 22:59:31 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 16 Jun 2021 22:59:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 22:59:32 GMT
STOPSIGNAL SIGINT
# Wed, 16 Jun 2021 22:59:32 GMT
EXPOSE 5432
# Wed, 16 Jun 2021 22:59:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:09564b0ac149fb24b77cbc75ce6fa5d9ba61bd7c99d11b42bd8339c3bb28e557`  
		Last Modified: Wed, 12 May 2021 01:16:36 GMT  
		Size: 25.8 MB (25812884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711734087a2d95ecb47d73397f83c426824b6dcd118984a2af0667aae286d9ff`  
		Last Modified: Wed, 12 May 2021 14:34:14 GMT  
		Size: 4.2 MB (4182535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1162cdaa5e1cce6b85f005af9858ef960750e330ac30edbcdfa756ea2f2ab4f`  
		Last Modified: Wed, 12 May 2021 14:34:10 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27359d35deb141040e851c50117b5f2d741a454f4e8971acc2fc59bc1bfc8c8b`  
		Last Modified: Wed, 12 May 2021 14:34:11 GMT  
		Size: 1.3 MB (1307413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cec65f9ce0c1e4ae5275e0b87bd64d62e37f2d0773112ff56d47b174cf9694c`  
		Last Modified: Wed, 12 May 2021 14:34:15 GMT  
		Size: 8.0 MB (7964671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bdaf7052f544eedd7eba3e8a88181c405de5aac9ed4be8d4df658ed61735054`  
		Last Modified: Wed, 12 May 2021 14:34:07 GMT  
		Size: 389.3 KB (389307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97a2946cea7e515e4776c3b5c7b66c1253652efc6c4afb79018e776d1e2b17d`  
		Last Modified: Wed, 12 May 2021 14:34:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80373f65da43be81495635f60f8834f07b39d7bbaddbe635aded32c7f6ac39f3`  
		Last Modified: Wed, 12 May 2021 14:34:07 GMT  
		Size: 3.1 KB (3054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b779664ef3b545283ec2319fb85b13b411ac292c0d3b275376404753de609f28`  
		Last Modified: Thu, 17 Jun 2021 01:52:28 GMT  
		Size: 70.9 MB (70851657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d896af1ad0cea1cbc8879f4006de76927b50b1a08c4207bdbd72b4bbf0620745`  
		Last Modified: Thu, 17 Jun 2021 01:51:40 GMT  
		Size: 9.3 KB (9350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2180d3e671f4b502eb431064be324068157ac01a12f7bc52f664f5d518e01d24`  
		Last Modified: Thu, 17 Jun 2021 01:51:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13eeb413b7983b962dba39fac1037d7d69da2da373b70db32d63a454281408d5`  
		Last Modified: Thu, 17 Jun 2021 01:51:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881605f9b3a6c0e6234d081962bdf8e0487bd305b8cc2df094435f11ab75c7b9`  
		Last Modified: Thu, 17 Jun 2021 01:51:40 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; ppc64le

```console
$ docker pull postgres@sha256:35c88d02698ef40eb9b0e538f78180f29cc0f32de1f086e6701251d73cbd2d84
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122209750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6527d17e0afe6058a64cb358a253ae43f71cf339af32d21563b46e445496b685`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 23 Jun 2021 00:30:38 GMT
ADD file:e599654230c9fe95fe2c591dbe60e8a0a886cd053b6117230fbae47561145731 in / 
# Wed, 23 Jun 2021 00:30:46 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 05:37:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 05:38:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 23 Jun 2021 05:38:29 GMT
ENV GOSU_VERSION=1.12
# Wed, 23 Jun 2021 05:40:17 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 23 Jun 2021 05:40:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 23 Jun 2021 05:40:45 GMT
ENV LANG=en_US.utf8
# Wed, 23 Jun 2021 05:41:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 05:41:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Jun 2021 05:41:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 23 Jun 2021 05:41:26 GMT
ENV PG_MAJOR=13
# Wed, 23 Jun 2021 05:41:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 23 Jun 2021 05:41:34 GMT
ENV PG_VERSION=13.3-1.pgdg100+1
# Wed, 23 Jun 2021 05:44:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 23 Jun 2021 05:44:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 23 Jun 2021 05:44:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 23 Jun 2021 05:44:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 23 Jun 2021 05:45:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 23 Jun 2021 05:45:08 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 23 Jun 2021 05:45:11 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 23 Jun 2021 05:45:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Jun 2021 05:45:23 GMT
STOPSIGNAL SIGINT
# Wed, 23 Jun 2021 05:45:27 GMT
EXPOSE 5432
# Wed, 23 Jun 2021 05:45:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f9cb1946299ce1824ee44809cd0c8b419528fee2f0f89e86400787a14b666f59`  
		Last Modified: Wed, 23 Jun 2021 00:37:07 GMT  
		Size: 30.6 MB (30553627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e89b134563ab5479f4009d9250e3a6f1a4d8cc0ef5abc7a890ca99ce1126de3`  
		Last Modified: Wed, 23 Jun 2021 06:17:54 GMT  
		Size: 5.0 MB (4967553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e28cc873846f676dbfca4597116b0c7ad15feedd60831dee56eacaad3132400`  
		Last Modified: Wed, 23 Jun 2021 06:17:51 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b74c9fea9bcb8291b53cd9f048e240e4b3b5fee457f4774a06fd462820c981`  
		Last Modified: Wed, 23 Jun 2021 06:17:51 GMT  
		Size: 1.3 MB (1338280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8da47b7b3df3323e707894b5e736c54b0ce2e729194b3ce70b867745ff2976`  
		Last Modified: Wed, 23 Jun 2021 06:17:51 GMT  
		Size: 8.0 MB (7965585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50945a7f61624d8dd91059cb1ccf68a7ec2f569c3cbc470e235ed153e49d8558`  
		Last Modified: Wed, 23 Jun 2021 06:17:49 GMT  
		Size: 397.2 KB (397204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d056b9ba09a6e667d3b87d57bfc2628080f8b3e75a39581ddb938e3e6e202d05`  
		Last Modified: Wed, 23 Jun 2021 06:17:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd485720540812fce78b6cb85c9a12688c4d2a19efd314e6f28dd97e0b1d085`  
		Last Modified: Wed, 23 Jun 2021 06:17:48 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b8c685ff8532f78a22d24ab4d43b4ef1f9708f2bb082f0afd3303dda4a4525`  
		Last Modified: Wed, 23 Jun 2021 06:18:00 GMT  
		Size: 77.0 MB (76968392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95b8e9d4366243c6a3d19a324d5967386f3e92a9def9e69b5926a19b437314e`  
		Last Modified: Wed, 23 Jun 2021 06:17:45 GMT  
		Size: 9.4 KB (9356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fda56301ab89815b03d3e7cb5c4ff0be00f76d82a4cff28cf1892f5e163edcf`  
		Last Modified: Wed, 23 Jun 2021 06:17:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055d9dddf01e42895be00a0e1d55e8005989f75c035743692d465b86ff6c0ac4`  
		Last Modified: Wed, 23 Jun 2021 06:17:45 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeab13247999c897745ae06d3d6d6b75c9b6a15d22f182054d66ff76c9979fd`  
		Last Modified: Wed, 23 Jun 2021 06:17:45 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:buster` - linux; s390x

```console
$ docker pull postgres@sha256:23df50b1e1d0bcb399b10932ed37e784f420a53b76e8e1767bae144f24e3d7a7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113254522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b5f4c96d743f108114467b9eab224e19c44a8cbd1d7a667c347dd70a3badb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Jun 2021 23:42:28 GMT
ADD file:a53e5772eefa4592eeff989f279dcc870986db7207b419dc3ae61cae85fce41f in / 
# Tue, 22 Jun 2021 23:42:29 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 04:28:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 04:28:56 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 23 Jun 2021 04:28:56 GMT
ENV GOSU_VERSION=1.12
# Wed, 23 Jun 2021 04:29:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 23 Jun 2021 04:29:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Wed, 23 Jun 2021 04:29:09 GMT
ENV LANG=en_US.utf8
# Wed, 23 Jun 2021 04:29:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 04:29:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 23 Jun 2021 04:29:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/postgres.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list
# Wed, 23 Jun 2021 04:29:14 GMT
ENV PG_MAJOR=13
# Wed, 23 Jun 2021 04:29:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 23 Jun 2021 04:29:15 GMT
ENV PG_VERSION=13.3-1.pgdg100+1
# Wed, 23 Jun 2021 04:38:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		amd64 | arm64 | i386 | ppc64el) 			echo "deb http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src http://apt.postgresql.org/pub/repos/apt/ buster-pgdg main $PG_MAJOR" > /etc/apt/sources.list.d/pgdg.list; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						savedAptMark="$(apt-mark showmanual)"; 						apt-get update; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y 				postgresql-common pgdg-keyring 				"postgresql-$PG_MAJOR=$PG_VERSION" 			; 			DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)" 				apt-get source --compile 					postgresql-common pgdg-keyring 					"postgresql-$PG_MAJOR=$PG_VERSION" 			; 						apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			dpkg-scanpackages . > Packages; 			grep '^Package: ' Packages; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			apt-get -o Acquire::GzipIndexes=false update; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Wed, 23 Jun 2021 04:38:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Wed, 23 Jun 2021 04:38:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 23 Jun 2021 04:38:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 23 Jun 2021 04:38:18 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 23 Jun 2021 04:38:18 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 23 Jun 2021 04:38:19 GMT
COPY file:e9c9c5e19c7b014c81f4ef8bcc5c1f247c4d9b165d34d35e9a28ca5adb5e0ab3 in /usr/local/bin/ 
# Wed, 23 Jun 2021 04:38:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Jun 2021 04:38:19 GMT
STOPSIGNAL SIGINT
# Wed, 23 Jun 2021 04:38:19 GMT
EXPOSE 5432
# Wed, 23 Jun 2021 04:38:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d08eb187b3111e87e1b138f7b93df64c5470da613a64d0adc804e17e12aed4dc`  
		Last Modified: Tue, 22 Jun 2021 23:45:45 GMT  
		Size: 25.8 MB (25760716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99b60ef2b79478040c8c3ca3299039831a30c7badfbe6d16855ad4941822ceb`  
		Last Modified: Wed, 23 Jun 2021 05:16:05 GMT  
		Size: 4.1 MB (4060053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a4a62f2a254f029e3d8c1f8bec27159c961cb7a2ad692510a249552f14f2ab`  
		Last Modified: Wed, 23 Jun 2021 05:16:04 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88a397c68280243551d2da16aa81d6922ad8819e1b6b26602ba4d654a46f21e`  
		Last Modified: Wed, 23 Jun 2021 05:16:04 GMT  
		Size: 1.4 MB (1406172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2815bc875cb001669a840d5480c0cac7fe3fe152756407fd06a2d960cf0af6`  
		Last Modified: Wed, 23 Jun 2021 05:16:04 GMT  
		Size: 8.0 MB (8019461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7ac18883f0c91daaca48b0c6689e54bbf1ff0e4ed9a158596a004d22aa1868`  
		Last Modified: Wed, 23 Jun 2021 05:16:03 GMT  
		Size: 388.4 KB (388375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0858d55bbb1aac6825ed98915f99daffe6d3428b8d4921103c83516e47be507`  
		Last Modified: Wed, 23 Jun 2021 05:16:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8744748438aab69abf849a567b4e0f46d449f975062b55efc5a1fee9118e38`  
		Last Modified: Wed, 23 Jun 2021 05:16:02 GMT  
		Size: 3.1 KB (3055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f1121652f5b1c2f3418de76b90be2d389bd46dcbb35555244bce09dd4115e4`  
		Last Modified: Wed, 23 Jun 2021 05:16:11 GMT  
		Size: 73.6 MB (73600655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a40778278adb9d5e885c94101d35e885c890e45ee30479631b7dc5d21c9cf03`  
		Last Modified: Wed, 23 Jun 2021 05:16:01 GMT  
		Size: 9.3 KB (9344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d358740a0868793059b6979043f112c850492f162007ffcbafcbba8a79fa7d8`  
		Last Modified: Wed, 23 Jun 2021 05:16:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f840077776e6bc8edb6596370a4e6b41ddc87d4e6a599e55cf20f4f329c37bc`  
		Last Modified: Wed, 23 Jun 2021 05:16:01 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47627acadf05a7c9f80994aca7c7196e0b9851c0a1521960cf548c197d0a88a0`  
		Last Modified: Wed, 23 Jun 2021 05:16:01 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
