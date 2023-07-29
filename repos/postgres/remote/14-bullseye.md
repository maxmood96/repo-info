## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:8f895965d97f4d9a11addc260476305beb5f204f46de9167ea96c3c7b11e5b6a
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

### `postgres:14-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:2cdcb80b188f92f4d995dcfb544f1ce7a6336838563f948d69209946426450e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138041896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f77003d5be53b81571d1b2ae770082fc96cc9289a2ea8be83ba0c58005bb1e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 10:46:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 28 Jul 2023 10:46:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 10:46:43 GMT
ENV GOSU_VERSION=1.16
# Fri, 28 Jul 2023 10:46:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 28 Jul 2023 10:46:56 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 28 Jul 2023 10:46:56 GMT
ENV LANG=en_US.utf8
# Fri, 28 Jul 2023 10:47:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 10:47:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 28 Jul 2023 10:47:01 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 28 Jul 2023 10:49:01 GMT
ENV PG_MAJOR=14
# Fri, 28 Jul 2023 10:49:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 28 Jul 2023 10:49:01 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Fri, 28 Jul 2023 10:49:19 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 10:49:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 10:49:21 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 10:49:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 10:49:21 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 10:49:21 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 10:49:21 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 10:49:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 10:49:22 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 10:49:22 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 10:49:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024ad9bec3dc28e27d7c084850e708939002c4fc0b85703c16f44739408e576f`  
		Last Modified: Fri, 28 Jul 2023 10:53:10 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd873abf5f61297809a1ea8c64287108e18e55c73f6ab734e1233b4c5192c73`  
		Last Modified: Fri, 28 Jul 2023 10:53:10 GMT  
		Size: 4.4 MB (4414998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe9a34510c576feca96de1feb60b25552d7489736422f696ece8181a672b0e7`  
		Last Modified: Fri, 28 Jul 2023 10:53:10 GMT  
		Size: 1.5 MB (1471525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66791212fee3c69b26f5fc9e655d6b4744388a7f247c666d0ec7b6809a477f6b`  
		Last Modified: Fri, 28 Jul 2023 10:53:09 GMT  
		Size: 8.0 MB (8045586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c53d590081eb4a8ee5df512be301285b697ef90e84276451b8c80a2da74501`  
		Last Modified: Fri, 28 Jul 2023 10:53:08 GMT  
		Size: 1.3 MB (1261280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d320348feab94969692596a3b418ec19e453dd5e534a3d1a5a90202d28948`  
		Last Modified: Fri, 28 Jul 2023 10:53:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878635654290e81617b5d0bbd8d6b76c939e0077b9282d79de401bae6493d80`  
		Last Modified: Fri, 28 Jul 2023 10:53:08 GMT  
		Size: 3.2 KB (3195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d56707fc5004ba3bb689e6314daccc6453c16f7ec3ab6c56b2abb27ee39d96`  
		Last Modified: Fri, 28 Jul 2023 10:55:02 GMT  
		Size: 91.4 MB (91411107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7789dc2e7dc04fe3de9f9102a0eb6a97beb9820474bab4cda8e73e2349e3e378`  
		Last Modified: Fri, 28 Jul 2023 10:54:48 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fac2dc8c3121468cc0b13906cbfb3fc1ef30e818ebbf7fdf12edad95afd447`  
		Last Modified: Fri, 28 Jul 2023 10:54:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f23d8193bac09d4bdc041a4d588602063ca01c894f1b9787942fee8e6ba24d`  
		Last Modified: Fri, 28 Jul 2023 10:54:48 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4dea71b5cce80d1a2324094c2c3814a3f82b88b64d3f215cefb269a7a802f07`  
		Last Modified: Fri, 28 Jul 2023 10:54:48 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:414e48982f255dd5f2268d860925832e7b8ce747d19b975eb3295a58b9b0293c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131295645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846d25e4ad5b4c04edebdc02b21eb77d390a374cb6d3409ee7ddb0da9e075f72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Jul 2023 23:48:45 GMT
ADD file:4c13aa568a9f7143288e9aa12f732c9bd7a01061a2a2d51ccf21cc471cb8ecda in / 
# Thu, 27 Jul 2023 23:48:45 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:32:43 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 28 Jul 2023 01:32:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:32:59 GMT
ENV GOSU_VERSION=1.16
# Fri, 28 Jul 2023 01:33:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 28 Jul 2023 01:33:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 28 Jul 2023 01:33:17 GMT
ENV LANG=en_US.utf8
# Fri, 28 Jul 2023 01:33:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 28 Jul 2023 01:33:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 28 Jul 2023 02:31:16 GMT
ENV PG_MAJOR=14
# Fri, 28 Jul 2023 02:31:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 28 Jul 2023 02:31:16 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Fri, 28 Jul 2023 02:44:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 02:44:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 02:44:49 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 02:44:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 02:44:50 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 02:44:50 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 02:44:50 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 02:44:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 02:44:50 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 02:44:51 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 02:44:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1d3ac731dc7e180da95b42e129ecf35def5601ce6f8cb38769eb5be8b48420a7`  
		Last Modified: Thu, 27 Jul 2023 23:52:11 GMT  
		Size: 28.9 MB (28919023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680b60c237cc028b3eb58625739224104d80d90436bae2a9d1e37ad1d5508e72`  
		Last Modified: Fri, 28 Jul 2023 04:03:58 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e490d500df7590a7ee43aaf3a86c265075875ba0cc56a8d6d1c3cb75079610e`  
		Last Modified: Fri, 28 Jul 2023 04:03:58 GMT  
		Size: 4.1 MB (4096731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84230c0a617cfb60cd863c8c60c71c425dcdb55a3c65c26bc06c5e1ff643f3fa`  
		Last Modified: Fri, 28 Jul 2023 04:03:58 GMT  
		Size: 1.4 MB (1448856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8b673be57b1a5d5761a7df206d20c0e3e3e326c5ad76f2513753ac4fc5bfe`  
		Last Modified: Fri, 28 Jul 2023 04:03:58 GMT  
		Size: 8.0 MB (8045543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dec168d1a17e959e2db8e91867a9e99c7ec8060d185af947e2a56b1b8384af`  
		Last Modified: Fri, 28 Jul 2023 04:03:56 GMT  
		Size: 1.3 MB (1257407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95876903367fd9ddab35ad88fa20836e3bb4f295a4ea13c374b6f384ae46dfc`  
		Last Modified: Fri, 28 Jul 2023 04:03:55 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1430f4cee8f139ac83b9fca5db0841baed36059d9d8e60e35343546b4a8a27`  
		Last Modified: Fri, 28 Jul 2023 04:03:55 GMT  
		Size: 3.2 KB (3203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e54b84aecc2b47b465c5d768603699838aecec9e99282a2cc690d7b49250ab0`  
		Last Modified: Fri, 28 Jul 2023 04:06:09 GMT  
		Size: 87.5 MB (87508281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06d220efee294e9a605019ad450478ec845f437b9cb379aa283039480a0cd2f`  
		Last Modified: Fri, 28 Jul 2023 04:05:54 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8aedb0e9138dc50895246f6502ccc72d767fab2ef55068ae2d23d452f3405d1`  
		Last Modified: Fri, 28 Jul 2023 04:05:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66971696a2db8782f9bf2a181a428644b2161bc8a12b81d634d3dbebb0e0eae3`  
		Last Modified: Fri, 28 Jul 2023 04:05:54 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3cb5d0da71b0a0d101e436fc977fb567c8efb13b1ca1bfc2e6c171320888386`  
		Last Modified: Fri, 28 Jul 2023 04:05:54 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b23b4240640d27903a7838e6777c5c5dee88c208dda414b1071d7c38f22c3869
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125948650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5219a1e4b5e861323df2bc4077affb96c9e1a9ca889598bca48b72bda9978b3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Jul 2023 23:58:18 GMT
ADD file:480cada6975fa477736805a1834cca05d1e18de255c6cc0cca13df01fdb44253 in / 
# Thu, 27 Jul 2023 23:58:18 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 16:37:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 28 Jul 2023 16:37:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 16:37:37 GMT
ENV GOSU_VERSION=1.16
# Fri, 28 Jul 2023 16:37:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 28 Jul 2023 16:37:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 28 Jul 2023 16:37:53 GMT
ENV LANG=en_US.utf8
# Fri, 28 Jul 2023 16:37:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 16:37:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 28 Jul 2023 16:37:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 28 Jul 2023 17:32:24 GMT
ENV PG_MAJOR=14
# Fri, 28 Jul 2023 17:32:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 28 Jul 2023 17:32:25 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Fri, 28 Jul 2023 17:44:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 17:44:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 17:44:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 17:44:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 17:44:59 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 17:44:59 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 17:44:59 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 17:44:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 17:44:59 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 17:44:59 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 17:44:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1236490553984befd7be19a151a0489729a35a66c4aaf5d799cd87d2c738371a`  
		Last Modified: Fri, 28 Jul 2023 00:03:56 GMT  
		Size: 26.6 MB (26578603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed8ed30854931230e9ca38bc525ae4002d9dbadb22b9393d8bf3ee5d8983600`  
		Last Modified: Fri, 28 Jul 2023 19:01:17 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c997de075e79a173f6ebb6f589a1272a4eb3009174447de138027c51825bce`  
		Last Modified: Fri, 28 Jul 2023 19:01:16 GMT  
		Size: 3.7 MB (3717396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bdfc6d2b8932bf14d1f41878e070d2aba542ee917b8f940b862bdfc9d5c09c`  
		Last Modified: Fri, 28 Jul 2023 19:01:16 GMT  
		Size: 1.4 MB (1438916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868a6b2df5c130d2c8dabb569158b96b7fe9d88c7da12f1491609962feaf2a6c`  
		Last Modified: Fri, 28 Jul 2023 19:01:16 GMT  
		Size: 8.0 MB (8045546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9eaaa77aecdc5eb6d131b39ddc593b3cbc4c181c7109fd4407b6dc84456b51`  
		Last Modified: Fri, 28 Jul 2023 19:01:14 GMT  
		Size: 1.1 MB (1131275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1917e3458d0b6afabb2a68b785b0647fe52b87b761b2a86f14f9c11500b730`  
		Last Modified: Fri, 28 Jul 2023 19:01:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb0dc07f02230241d7305dd33907f91fb376a262eb543928bb636b8a371f29d`  
		Last Modified: Fri, 28 Jul 2023 19:01:14 GMT  
		Size: 3.2 KB (3196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44291830d2afc6b2dfe80e6704595a40982f771cd398234e4f30060ac4b7aca`  
		Last Modified: Fri, 28 Jul 2023 19:03:16 GMT  
		Size: 85.0 MB (85017122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6809365ef52607d9d3542c43e0547794f25345c6421c92c410d9eacf8a7a913`  
		Last Modified: Fri, 28 Jul 2023 19:03:03 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8df2b851153fa8ff5575eac42fa444676076f820ae6bd7b7a83dc60af286199`  
		Last Modified: Fri, 28 Jul 2023 19:03:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae93c9af4b0693202977b2ec64751f326a351a81336df229387c3b3321440c0`  
		Last Modified: Fri, 28 Jul 2023 19:03:03 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c232eedbdde72223aca9f11d4807aea8bd0663bc9370c187a8e79dab42df18`  
		Last Modified: Fri, 28 Jul 2023 19:03:03 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:708b4b1a3f82cece9f296b0347af1f74bf240eb9f25891d497320f029cbcc42b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133118524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df73988575af2a32b1abcf5f5dbdb7eda7ab5302683724edbadb75d82cb5cd92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 06:28:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 28 Jul 2023 06:28:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:28:55 GMT
ENV GOSU_VERSION=1.16
# Fri, 28 Jul 2023 06:29:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 28 Jul 2023 06:29:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 28 Jul 2023 06:29:07 GMT
ENV LANG=en_US.utf8
# Fri, 28 Jul 2023 06:29:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:29:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 28 Jul 2023 06:29:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 28 Jul 2023 06:30:54 GMT
ENV PG_MAJOR=14
# Fri, 28 Jul 2023 06:30:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 28 Jul 2023 06:30:54 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Fri, 28 Jul 2023 06:31:10 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 06:31:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 06:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 06:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 06:31:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 06:31:13 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 06:31:13 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 06:31:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 06:31:13 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 06:31:13 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 06:31:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ef2a54d14635bb9aa5bc4e21635bd4ac8c079ff7fe9dfdfa6a35b58a31893a`  
		Last Modified: Fri, 28 Jul 2023 06:34:50 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd15fc515dcb3713dc4984c9595ffe220d13645ec81431956021b137ec05448b`  
		Last Modified: Fri, 28 Jul 2023 06:34:51 GMT  
		Size: 4.4 MB (4416363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb9ea850135b445c55a8707be7977d677e4f468c76ebf1c825a5c4040d06bde`  
		Last Modified: Fri, 28 Jul 2023 06:34:50 GMT  
		Size: 1.4 MB (1403308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae46c8f2169db1ca2f34537a7228a0ada9ae3819b958519b0adca13666756b73`  
		Last Modified: Fri, 28 Jul 2023 06:34:49 GMT  
		Size: 8.0 MB (8045545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f48aec438d5be1ddeec5ade20605879138bff9f1a653a90bd74030118f56b7`  
		Last Modified: Fri, 28 Jul 2023 06:34:48 GMT  
		Size: 1.2 MB (1249321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913902521fcb846f003b537825e9d08451988dba2549ccf5eee01d56e73d90d0`  
		Last Modified: Fri, 28 Jul 2023 06:34:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8050d8259ea10ef8bc53ed0a05dedccc3206c63e55e670dfdb3fdd1876fe91`  
		Last Modified: Fri, 28 Jul 2023 06:34:48 GMT  
		Size: 3.2 KB (3199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce08c7ba00cd37f364d82ed5585215a3c8c0bf81205028e4e2dc9345e4bc117`  
		Last Modified: Fri, 28 Jul 2023 06:36:35 GMT  
		Size: 87.9 MB (87921352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add6fa1ef43171f46bc29a00986f592d3c19942ca1967a2bd57dd81889086c4a`  
		Last Modified: Fri, 28 Jul 2023 06:36:26 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2182a6ac729ac50524eba8966ebbb33a5bee59a9258135eff5d58127ae6e9ed6`  
		Last Modified: Fri, 28 Jul 2023 06:36:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a19bc01f952779c78675b35815b94ee797941eac99781f04c50b1b917198dbc`  
		Last Modified: Fri, 28 Jul 2023 06:36:26 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d67055c1bba876afd75d63f3c0583116f46b95e835e4c9d3b1c3c898e6a28a`  
		Last Modified: Fri, 28 Jul 2023 06:36:26 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:75a698c65d891eff70c2488855456822e8b6f503c09eb8a3fad018557a334345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140088043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31160a8ff9d5201ee508a8bb5d120e52a87e6cefbc4866fc5daed7ab90ed3d48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Jul 2023 23:39:19 GMT
ADD file:1b873519e4db5a8c03ce73348afdd01ea06bbc550a0a873f4c3f9ead4db3c27e in / 
# Thu, 27 Jul 2023 23:39:19 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 10:09:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 28 Jul 2023 10:10:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 10:10:05 GMT
ENV GOSU_VERSION=1.16
# Fri, 28 Jul 2023 10:10:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 28 Jul 2023 10:10:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 28 Jul 2023 10:10:22 GMT
ENV LANG=en_US.utf8
# Fri, 28 Jul 2023 10:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 10:10:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 28 Jul 2023 10:10:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 28 Jul 2023 11:10:36 GMT
ENV PG_MAJOR=14
# Fri, 28 Jul 2023 11:10:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 28 Jul 2023 11:10:37 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Fri, 28 Jul 2023 11:24:33 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 11:24:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 11:24:35 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 11:24:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 11:24:36 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 11:24:36 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 11:24:36 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 11:24:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 11:24:36 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 11:24:36 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 11:24:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e929cbc32ad44888448591b293bf4b9f260f11c666001b727228b58fd1774225`  
		Last Modified: Thu, 27 Jul 2023 23:44:12 GMT  
		Size: 32.4 MB (32397129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8376e39f278420adbd0517d955bb841b8d5be8f57660990539ae94b72560ac`  
		Last Modified: Fri, 28 Jul 2023 12:46:45 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f900b256243a7d2fe67692c541b1902ad6fb1d46bd5e69bd7c73d1a2d9b01e32`  
		Last Modified: Fri, 28 Jul 2023 12:46:46 GMT  
		Size: 4.8 MB (4813582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a462698116ccd595d3ced638522906f00bb665eb1f5860c47fd89d2533c48d`  
		Last Modified: Fri, 28 Jul 2023 12:46:45 GMT  
		Size: 1.4 MB (1447104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8253463367bcf05b85a3c52246d3ba264882f1ee375f573b2837a481677f5a2b`  
		Last Modified: Fri, 28 Jul 2023 12:46:45 GMT  
		Size: 8.0 MB (8045457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37319c7d83cb298d4d69884cefdbb5aee74aff609d92160fcfadc58bed094be9`  
		Last Modified: Fri, 28 Jul 2023 12:46:43 GMT  
		Size: 1.3 MB (1251731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30653d6c61a38dba29287a86119ea7d0ebb7f2ab05deb0832618f9336cd4b671`  
		Last Modified: Fri, 28 Jul 2023 12:46:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da91bee4b15fd94c4f313807bfb2fe9e6c5fbaebebefe9609dfb7adb9330b10c`  
		Last Modified: Fri, 28 Jul 2023 12:46:42 GMT  
		Size: 3.2 KB (3195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad847314c387eb749b13e056d75b75ff3dacfcfc737084640e2ab16de623e19`  
		Last Modified: Fri, 28 Jul 2023 12:49:10 GMT  
		Size: 92.1 MB (92113246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4331a0c475f157a7b714985f90161bce004854845b8b196dfa6ecbb7b695d6c8`  
		Last Modified: Fri, 28 Jul 2023 12:48:53 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5585eb16d4c11a76674e19bd72e2de4397ba7bfa16be411a5788fb60a1f9d14`  
		Last Modified: Fri, 28 Jul 2023 12:48:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe794aad5b1a5f976fcc45da646685772b159a66046d24d5d8ada9d1a4b15571`  
		Last Modified: Fri, 28 Jul 2023 12:48:53 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bc7b7ed5a58f54fd7fe065ebf724daf577adb4837d6d397ef9807a3852f44b`  
		Last Modified: Fri, 28 Jul 2023 12:48:53 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:b0b39d2bb493ac591d4d3e2925e72af8b7f018a101cc02e441b3de7ac4b5a598
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe82ecdf41f886ffe11e1ef8a68cb68c7754633aab32fbd8b8c3ce7ae01ec7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Jul 2023 23:12:38 GMT
ADD file:eb90061ee3f4fd61dbda173f0380200a5dc076351179eba4b0b8c33f105cc9a9 in / 
# Thu, 27 Jul 2023 23:12:42 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 15:11:57 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 28 Jul 2023 15:12:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 15:12:35 GMT
ENV GOSU_VERSION=1.16
# Fri, 28 Jul 2023 15:13:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 28 Jul 2023 15:13:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 28 Jul 2023 15:13:40 GMT
ENV LANG=en_US.utf8
# Fri, 28 Jul 2023 15:13:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 15:14:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 28 Jul 2023 15:14:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 28 Jul 2023 19:27:55 GMT
ENV PG_MAJOR=14
# Fri, 28 Jul 2023 19:27:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 28 Jul 2023 19:28:00 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Fri, 28 Jul 2023 20:27:38 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 20:27:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 20:27:51 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 20:27:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 20:28:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 20:28:04 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 20:28:07 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 20:28:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 20:28:14 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 20:28:17 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 20:28:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:10d8abc44954ef848b9859622726cf3c6369682051190a64889c4392d6106fb5`  
		Last Modified: Thu, 27 Jul 2023 23:23:50 GMT  
		Size: 29.6 MB (29634516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32a8857a806db6d981609eae25bbca51ab17f3ec5f0bdf57e64cfae32bb06a4`  
		Last Modified: Sat, 29 Jul 2023 02:14:31 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66998fe1733637bbb7a7004c2d7bea78a073e0aadda55a89f501f0f5623b153`  
		Last Modified: Sat, 29 Jul 2023 02:14:34 GMT  
		Size: 4.2 MB (4196293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f182721c76f330deac8ec48db49012a2cfc3c0298626c43989eece06663077`  
		Last Modified: Sat, 29 Jul 2023 02:14:31 GMT  
		Size: 1.4 MB (1358351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc2c92f55b8a18cb06ca7c60047da12cc715ca6d2c21e53d648fc893246becb`  
		Last Modified: Sat, 29 Jul 2023 02:14:35 GMT  
		Size: 8.0 MB (8044044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168f9e8b17d3597da62c98c54907bd6c26b87795039f6395364c795e340a4944`  
		Last Modified: Sat, 29 Jul 2023 02:14:28 GMT  
		Size: 1.1 MB (1089529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dba2e50f59fbe2cf43d6278158ee1e009b3795fa84c4d1c29511ac350c884d5`  
		Last Modified: Sat, 29 Jul 2023 02:14:28 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28f3575370aa2afa010f9a9516d1b7154f1da7ee89a1b5b6900727940e73ea4`  
		Last Modified: Sat, 29 Jul 2023 02:14:27 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f204833732ba4cc0e03a538371539b1ccb986882a5818cf043bd090bf4034bb3`  
		Last Modified: Sat, 29 Jul 2023 02:20:22 GMT  
		Size: 88.1 MB (88057401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964d86c28a76c1a2532d0c4b74e3a4c7edd5826abb14fe8326daaf9322de22a1`  
		Last Modified: Sat, 29 Jul 2023 02:19:26 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef77f8eea8ebe317a87b8dbcfd7a8d6ece8247f2552774e904fb745a8720d1a2`  
		Last Modified: Sat, 29 Jul 2023 02:19:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1feb207795841f5c5b8c919b6b75770c156b347c3429d466b5d29110fe6b19a`  
		Last Modified: Sat, 29 Jul 2023 02:19:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f17f2a77dbe1eb807335388d7b8249d18bca8b7e2e1cc4f3366fac541ceab4`  
		Last Modified: Sat, 29 Jul 2023 02:19:26 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:4d1fe28196046ae17eae45c761c2b02b122d302ac7476cf0a5b74e148d03902a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147111719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb844d199bf9f4378e21fd5bf54a711b4875c1541bf8fb61c74ac63fe1f70d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Jul 2023 23:23:41 GMT
ADD file:bc63550bad6e6b1e46c01c4911ac409a0a01e632b56a9a846fa2d7c86d8bb292 in / 
# Thu, 27 Jul 2023 23:23:43 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 04:18:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 28 Jul 2023 04:18:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 04:18:47 GMT
ENV GOSU_VERSION=1.16
# Fri, 28 Jul 2023 04:19:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 28 Jul 2023 04:19:17 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 28 Jul 2023 04:19:18 GMT
ENV LANG=en_US.utf8
# Fri, 28 Jul 2023 04:19:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 04:19:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 28 Jul 2023 04:19:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 28 Jul 2023 04:25:15 GMT
ENV PG_MAJOR=14
# Fri, 28 Jul 2023 04:25:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 28 Jul 2023 04:25:16 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Fri, 28 Jul 2023 04:26:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 04:26:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 04:26:19 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 04:26:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 04:26:25 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 04:26:33 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 04:26:35 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 04:26:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 04:26:37 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 04:26:39 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 04:26:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:90fff1cd317dd6511bdf25cbc4f6797ea09a5bc0657b6e1d88772d885bed1da0`  
		Last Modified: Thu, 27 Jul 2023 23:30:33 GMT  
		Size: 35.3 MB (35291031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c37e787375d79b7f69584dce2070cb63af455a0f61bde3875b5ef8c0e03646`  
		Last Modified: Fri, 28 Jul 2023 04:37:28 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69ddddd9fd353ac1ed7f39b15b54c734286873268077ba763727f0d9d8e1845`  
		Last Modified: Fri, 28 Jul 2023 04:37:29 GMT  
		Size: 5.2 MB (5222967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2335d1115100bf7ece1b4056a41d907d50baa5d73c056d438f5a0406ac26d5e`  
		Last Modified: Fri, 28 Jul 2023 04:37:28 GMT  
		Size: 1.4 MB (1393341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b8c4a4898f98a9670d92aef71fa57ff8e5af2471005ba6a1c1d0b08804b1b0`  
		Last Modified: Fri, 28 Jul 2023 04:37:28 GMT  
		Size: 8.0 MB (8045444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db4fdeb28d093ec381f144fb0b08369a420d190e534cc7775ed890a386c4921`  
		Last Modified: Fri, 28 Jul 2023 04:37:25 GMT  
		Size: 1.4 MB (1420249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0931b0e672d29709e2a79615fd1404ac98b08502d1af275a3d8e5b005edcdbba`  
		Last Modified: Fri, 28 Jul 2023 04:37:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6d9c7bf7bc5b1748d09bb53fc14878ab92b5131e84412ae77ffe59b411d852`  
		Last Modified: Fri, 28 Jul 2023 04:37:25 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43f8bd245b232f34b9167812fd0630041631639700cc7ac809a5bf091ad2b62`  
		Last Modified: Fri, 28 Jul 2023 04:40:47 GMT  
		Size: 95.7 MB (95718878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905ed2b317d5c5ae40aefb27921794e70ae3f2cfae36f181da937517231dd196`  
		Last Modified: Fri, 28 Jul 2023 04:40:25 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7062d4431b7a0ca9534c3001014f07deff02a2658dbf81d32a1c6d2994a1f0`  
		Last Modified: Fri, 28 Jul 2023 04:40:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b3b02350ec8cab5d9112c621060ceebb03bc4eb0c999e2b8a80f9ee580f2da`  
		Last Modified: Fri, 28 Jul 2023 04:40:24 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b80269292505ce3be3f626d1e53a2d3f4f00416786a646af53107974c41b192`  
		Last Modified: Fri, 28 Jul 2023 04:40:24 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:12de9f81e9eeafdf9c4d3c0742ff8709ea6a0e5a071badacee432e43aea7760a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141664641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16896a49741135adb71c18749b3982e6997e6853ba97c91b8925eebf994416`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:42 GMT
ADD file:af0651fb20da5a08d22c074a04a2d96d68d66b5be86a11d348364e151de46196 in / 
# Thu, 27 Jul 2023 23:47:44 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 09:37:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 28 Jul 2023 09:37:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 09:37:32 GMT
ENV GOSU_VERSION=1.16
# Fri, 28 Jul 2023 09:37:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 28 Jul 2023 09:37:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Fri, 28 Jul 2023 09:37:43 GMT
ENV LANG=en_US.utf8
# Fri, 28 Jul 2023 09:37:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 09:37:47 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 28 Jul 2023 09:37:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 28 Jul 2023 09:40:22 GMT
ENV PG_MAJOR=14
# Fri, 28 Jul 2023 09:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Fri, 28 Jul 2023 09:40:22 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Fri, 28 Jul 2023 09:40:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 09:40:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 09:40:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 09:40:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 09:40:44 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 09:40:44 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 09:40:44 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 09:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 09:40:44 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 09:40:45 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 09:40:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:010ebc9d3534dabb784b6e93117170f0f20f698913991111a4ea549e5d951b7b`  
		Last Modified: Thu, 27 Jul 2023 23:52:47 GMT  
		Size: 29.7 MB (29652882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98fbfdca892b11ca05f9ce6635b53da4a570855d1d96d99573a8bb3ec056a03`  
		Last Modified: Fri, 28 Jul 2023 09:46:20 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebca4cfcc6e5011858d85ee03ecd0f4e9c993fd0c42d32f1fa30d023a0f61e12`  
		Last Modified: Fri, 28 Jul 2023 09:46:20 GMT  
		Size: 4.3 MB (4302323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9147711560021d081b089ed89d9c449b602d28d0051ef88696e90229ab203a82`  
		Last Modified: Fri, 28 Jul 2023 09:46:20 GMT  
		Size: 1.4 MB (1437201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b790b88c90e81d58689821abb6bc7452bbfe466675ac5a666990c1698b408f07`  
		Last Modified: Fri, 28 Jul 2023 09:46:20 GMT  
		Size: 8.1 MB (8099342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70318fcd50ec1597b40d72986c11d4c83918eb8ab7f9acea4e171a4fa7cfc9b2`  
		Last Modified: Fri, 28 Jul 2023 09:46:18 GMT  
		Size: 1.2 MB (1238040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e4d5a6ba6196d48ede337720ef35cd082cbd9d0961e3e19845e9772281a821`  
		Last Modified: Fri, 28 Jul 2023 09:46:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2acf7d78aeb4e583ca2e3a39f683548f36bfb5f9975d74c5dd344089db57265`  
		Last Modified: Fri, 28 Jul 2023 09:46:18 GMT  
		Size: 3.2 KB (3202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20189f7ad801cb706e74883b51ed512663021205847896c3941c16b9005f96d9`  
		Last Modified: Fri, 28 Jul 2023 09:48:02 GMT  
		Size: 96.9 MB (96915040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5958de9862a5d7f9e25f8bab32ff2d4b1aff2b6f091269e159d306d69e5eb595`  
		Last Modified: Fri, 28 Jul 2023 09:47:50 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41012dbf7254d4c2d0ff3c05fd578b1a86950cc5405451637c08deb46d06f03c`  
		Last Modified: Fri, 28 Jul 2023 09:47:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085ce50c558dbd2e4563a51f5f38d7359790f1bfe38f8b6dd0102c6b3e840ef6`  
		Last Modified: Fri, 28 Jul 2023 09:47:50 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1797c67fe4a5ecace82fcef8090ec3946e94f8b04d0fa03422588d2e2a16bf`  
		Last Modified: Fri, 28 Jul 2023 09:47:50 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
