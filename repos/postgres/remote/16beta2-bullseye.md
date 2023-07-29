## `postgres:16beta2-bullseye`

```console
$ docker pull postgres@sha256:7810548d0b4203688fa47f77dd3d16aa2512be022ee258b25d6e6b9ea0a225c1
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

### `postgres:16beta2-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:13d7ab6c1974e36b072e821f57fec6f6913aba6b25812fbfb0c882988d0091a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140931424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4316d6c253be67442510eca5e804b02089ec98f5f7d9986f17dd2b18fe727fb`
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
# Fri, 28 Jul 2023 10:47:01 GMT
ENV PG_MAJOR=16
# Fri, 28 Jul 2023 10:47:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 28 Jul 2023 10:47:02 GMT
ENV PG_VERSION=16~beta2-1.pgdg110+1
# Fri, 28 Jul 2023 10:47:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 10:47:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 10:47:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 10:47:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 10:47:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 10:47:24 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 10:47:24 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 10:47:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 10:47:24 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 10:47:24 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 10:47:25 GMT
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
	-	`sha256:369bdeb759d407ec41572e86e4f12b52058831284b8f0336232ff9f062122714`  
		Last Modified: Fri, 28 Jul 2023 10:53:18 GMT  
		Size: 94.3 MB (94300236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3f854997e3696b32870b02079b72b57b926970fa26a0350874b56592a8d5ad`  
		Last Modified: Fri, 28 Jul 2023 10:53:06 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7130b0c9db69e4f83cff8811c2671a22cb0de1ce1a9b39fef27c1217e7780af2`  
		Last Modified: Fri, 28 Jul 2023 10:53:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0d409e2e5e624285841ea51ce68dfba409864978f76a4353b5e97c5ffca1aa`  
		Last Modified: Fri, 28 Jul 2023 10:53:06 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fddf9b476cbb4e4f48852dc7e9577085a338cf6c78ba49063a8636bf02022e`  
		Last Modified: Fri, 28 Jul 2023 10:53:06 GMT  
		Size: 4.8 KB (4787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:417a3921dea8c74479e1cdf0a1fdd83e37fa6ae8ee72ef54977cd87c83193333
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134190494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ff604e7c53871a73d22c4c45fb9a6c4ff17b82fb2ae46c8e2022e31de23717`
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
# Fri, 28 Jul 2023 01:33:25 GMT
ENV PG_MAJOR=16
# Fri, 28 Jul 2023 01:33:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 28 Jul 2023 01:33:25 GMT
ENV PG_VERSION=16~beta2-1.pgdg110+1
# Fri, 28 Jul 2023 01:48:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 01:48:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 01:48:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 01:48:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 01:48:31 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 01:48:31 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 01:48:31 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 01:48:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 01:48:31 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 01:48:31 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 01:48:31 GMT
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
	-	`sha256:6e1c0aa94c948f13c24806d78b752905552064e20d6fb007b9f4efd3219a3f9b`  
		Last Modified: Fri, 28 Jul 2023 04:04:09 GMT  
		Size: 90.4 MB (90402735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c4fb36efb9c2d3b17effab2c95060a40dbf94c3ea1fe59c03314e7bf97eb01`  
		Last Modified: Fri, 28 Jul 2023 04:03:54 GMT  
		Size: 9.9 KB (9932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08274fc866a9ab3a8aa14076d4cf1c5309abecb6ff05904a69e3cc3d5fc1d1e7`  
		Last Modified: Fri, 28 Jul 2023 04:03:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956fe6fc0da526bff17f931732bdd074311154e90e7ab5607a11c9a363b28516`  
		Last Modified: Fri, 28 Jul 2023 04:03:54 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42cb8f208542b1bad084afaab78b54006904114fe55f80ac5d1fb026409df419`  
		Last Modified: Fri, 28 Jul 2023 04:03:54 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:12eb901974bcb80ed27da27f3c4447538d15227ec21e56c42b3136bee5bfc077
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128815551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d62ce1d233f1b954862f05ce20b1db093a915e451ada3814a7d79ae5d86b78`
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
# Fri, 28 Jul 2023 16:37:59 GMT
ENV PG_MAJOR=16
# Fri, 28 Jul 2023 16:37:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 28 Jul 2023 16:38:00 GMT
ENV PG_VERSION=16~beta2-1.pgdg110+1
# Fri, 28 Jul 2023 16:51:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 16:51:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 16:51:39 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 16:51:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 16:51:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 16:51:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 16:51:40 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 16:51:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 16:51:41 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 16:51:41 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 16:51:41 GMT
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
	-	`sha256:b1133d8a1af0fd9b27bc24c701c5be53b1a366e7637224d3df5e0360fff109f5`  
		Last Modified: Fri, 28 Jul 2023 19:01:25 GMT  
		Size: 87.9 MB (87883622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16daea8cb13bf0aa3019b4fbb1607548b6747f805c4c43121579ed40b18ccdce`  
		Last Modified: Fri, 28 Jul 2023 19:01:12 GMT  
		Size: 9.9 KB (9935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ea3290e06b6faf10294be16015d7e6acace14ef5bcf542de3ab25855f4c618`  
		Last Modified: Fri, 28 Jul 2023 19:01:12 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52ca8d9a1326996ee00f000449b32137b3a4182c225eb3c15735c5785e743a7`  
		Last Modified: Fri, 28 Jul 2023 19:01:12 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57760983c416a7615d4dfcdd349a65046707385c27faa2ecf5d0344d9a53797d`  
		Last Modified: Fri, 28 Jul 2023 19:01:12 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0653057ad4b565815c627efbc0d7f270ef35105567c9caef698ca39a3850289a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135969657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659fc7a255f681764b722c4b65be0adae0f51f31e3bcf9d5ab53a4cea146efcb`
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
# Fri, 28 Jul 2023 06:29:12 GMT
ENV PG_MAJOR=16
# Fri, 28 Jul 2023 06:29:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 28 Jul 2023 06:29:12 GMT
ENV PG_VERSION=16~beta2-1.pgdg110+1
# Fri, 28 Jul 2023 06:29:31 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 06:29:33 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 06:29:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 06:29:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 06:29:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 06:29:34 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 06:29:34 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 06:29:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 06:29:34 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 06:29:35 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 06:29:35 GMT
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
	-	`sha256:5aeb619c39dd427ccd20920608275b53d627f8d4c3d4ccae9c2bd172aa84ffbb`  
		Last Modified: Fri, 28 Jul 2023 06:34:55 GMT  
		Size: 90.8 MB (90772085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7d1182d5e67a0c3189488d4bc243361495cd20cef714d1a75b6b0a01ba8bd4`  
		Last Modified: Fri, 28 Jul 2023 06:34:46 GMT  
		Size: 9.9 KB (9930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c10f6426d92ceb46da3989db66a8d16cf14357e3273077d9f859942a3609b72`  
		Last Modified: Fri, 28 Jul 2023 06:34:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e1a3f9f7baa894f994c2f529b13bf7f1816ab647fdca907047d9d33ad4196d`  
		Last Modified: Fri, 28 Jul 2023 06:34:46 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d244cbed8a3de4a8cea591b3e82204fc65ab5952e599114db04a38961f34de`  
		Last Modified: Fri, 28 Jul 2023 06:34:46 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:4670115ea44d2b1444c925f92ac470779749c0b7c80be0a9607f75fe26a46ef4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143027817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bc20f87bd19d17c47a27fd23103c56b260caa0d9da6be7ca156b9ff63bec6d`
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
# Fri, 28 Jul 2023 10:10:29 GMT
ENV PG_MAJOR=16
# Fri, 28 Jul 2023 10:10:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 28 Jul 2023 10:10:29 GMT
ENV PG_VERSION=16~beta2-1.pgdg110+1
# Fri, 28 Jul 2023 10:25:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 10:25:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 10:25:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 10:25:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 10:25:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 10:25:47 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 10:25:47 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 10:25:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 10:25:47 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 10:25:47 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 10:25:47 GMT
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
	-	`sha256:005737b653eacac076ec4916cd4f1d8949c55f0b34f8467aeb86c5ba0dec19b5`  
		Last Modified: Fri, 28 Jul 2023 12:46:59 GMT  
		Size: 95.1 MB (95052616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd093ed57c5a1b5ebaeb6a116d0929c84aef1c5ddf8af9d5e9e033d46b265e72`  
		Last Modified: Fri, 28 Jul 2023 12:46:40 GMT  
		Size: 9.9 KB (9936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac0cc4e4948c403e137864cc07db3ee2e5603c513d01b00e8ca33102c62801b`  
		Last Modified: Fri, 28 Jul 2023 12:46:40 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c85b875b2ad4a46958f8ffd8c37839c56571b0b1e702a752f08e9c34a56711`  
		Last Modified: Fri, 28 Jul 2023 12:46:40 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e6c3be518ab92e7c299e4b8634efe16c1104601365d0221c22bd7c5c1bc1f2`  
		Last Modified: Fri, 28 Jul 2023 12:46:40 GMT  
		Size: 4.8 KB (4796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:fbbb74a432860e671db25330a2648f387ef5659ef08aaa2df69693035c8e6fb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135273565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61e8c663e3e7901e77f24d73b113d9eb97bf3b7c3f6115b61549fa985557fec`
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
# Fri, 28 Jul 2023 15:14:11 GMT
ENV PG_MAJOR=16
# Fri, 28 Jul 2023 15:14:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 28 Jul 2023 15:14:17 GMT
ENV PG_VERSION=16~beta2-1.pgdg110+1
# Fri, 28 Jul 2023 16:17:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 16:17:53 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 16:17:59 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 16:18:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 16:18:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 16:18:11 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 16:18:14 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 16:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 16:18:21 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 16:18:25 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 16:18:28 GMT
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
	-	`sha256:e5990b725a61277095f678077ad5862cab76c3e96128d4eb80ed119fd8e21aad`  
		Last Modified: Sat, 29 Jul 2023 02:15:24 GMT  
		Size: 90.9 MB (90930915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abcf3ca5080154fbfeb34a0a68b08db944f15a6baac51f3038c4531f7881c190`  
		Last Modified: Sat, 29 Jul 2023 02:14:25 GMT  
		Size: 9.9 KB (9931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5c8d0d0409794146a78dfd5499bea26de48d61ed4b0672fc47b8041b9eefc6`  
		Last Modified: Sat, 29 Jul 2023 02:14:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7200bba68ad31a33f0440161d7358ce739543d61326a56b64ff109888387a221`  
		Last Modified: Sat, 29 Jul 2023 02:14:25 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f095a3b104d45d0e7becb7eb47691f7f850f696afbd31ddbde92cf07ae670aa9`  
		Last Modified: Sat, 29 Jul 2023 02:14:25 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:684cffca2af5b369f2e6be6d68dd9730313f37462513b531cb6ce82da9e59c84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150014769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415226678b00125c4096e601a7a42b77895259976fa520b822b549d381e8f6c7`
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
# Fri, 28 Jul 2023 04:19:30 GMT
ENV PG_MAJOR=16
# Fri, 28 Jul 2023 04:19:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 28 Jul 2023 04:19:30 GMT
ENV PG_VERSION=16~beta2-1.pgdg110+1
# Fri, 28 Jul 2023 04:20:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 04:20:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 04:20:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 04:20:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 04:20:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 04:20:46 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 04:20:47 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 04:20:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 04:20:48 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 04:20:48 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 04:20:49 GMT
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
	-	`sha256:f63f2d8a6e6d6cc2776bb953e6b0b8f7076914a87cc09b6200d49283f21a76ae`  
		Last Modified: Fri, 28 Jul 2023 04:37:46 GMT  
		Size: 98.6 MB (98621532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32bd2d89eab5dbae9d22058bc9c9ca031ad328881253a3ebe12d17e09bef0cb`  
		Last Modified: Fri, 28 Jul 2023 04:37:23 GMT  
		Size: 9.9 KB (9932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf72e4233822c629496096e8bdc9b4f781ab9eb13bbadda10ed5b64c1b2f7eed`  
		Last Modified: Fri, 28 Jul 2023 04:37:22 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9c25e603fd6cf33fe92eb63b4b3a0e0b0b9871825d0b1c920f00775408ac53`  
		Last Modified: Fri, 28 Jul 2023 04:37:22 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89129b516dc7321d6a3c1be159effa66255cb0f953c622aad8fdfc706f3757b`  
		Last Modified: Fri, 28 Jul 2023 04:37:22 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta2-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:8811a41f4edd623d245cdba87ab8421529135a00743f3b266b51de99c0734056
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144545643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6285b9f8b412a8df2faaaae32f95b50167bb8bfca0aa56a1f9dda3a82fd94b0d`
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
# Fri, 28 Jul 2023 09:37:48 GMT
ENV PG_MAJOR=16
# Fri, 28 Jul 2023 09:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 28 Jul 2023 09:37:48 GMT
ENV PG_VERSION=16~beta2-1.pgdg110+1
# Fri, 28 Jul 2023 09:38:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Fri, 28 Jul 2023 09:38:11 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Fri, 28 Jul 2023 09:38:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 28 Jul 2023 09:38:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 28 Jul 2023 09:38:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 28 Jul 2023 09:38:12 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 28 Jul 2023 09:38:12 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Fri, 28 Jul 2023 09:38:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Jul 2023 09:38:13 GMT
STOPSIGNAL SIGINT
# Fri, 28 Jul 2023 09:38:13 GMT
EXPOSE 5432
# Fri, 28 Jul 2023 09:38:13 GMT
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
	-	`sha256:1fa1ba40d00470a3e83beed628476f2d7207c20ee11319142418595429094aa3`  
		Last Modified: Fri, 28 Jul 2023 09:46:30 GMT  
		Size: 99.8 MB (99795648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab0fecfb4fa093c579ea5943d0a66e07460ef8fa4ef6f0369142eb33593a82a`  
		Last Modified: Fri, 28 Jul 2023 09:46:17 GMT  
		Size: 9.9 KB (9929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f5b74d7b379ce42de638950858cf76954e88ae3a356b23392b4905bddb6845`  
		Last Modified: Fri, 28 Jul 2023 09:46:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07bdf392cfea8b6fbf6b6bb91ef9a05ee48b4f69c4a3a7d65987795609a4c34`  
		Last Modified: Fri, 28 Jul 2023 09:46:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21926eef508ae51300f37409cb6ea57f169e481f46e9762a02c62ad73680225`  
		Last Modified: Fri, 28 Jul 2023 09:46:17 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
