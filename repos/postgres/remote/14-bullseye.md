## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:62654975aa29c64dbc7ad1150e42557939da756dbdf6455c0aa1a05c9b424f25
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
$ docker pull postgres@sha256:9802ea8929ca49a53a5701632661aef909a7d039fd717140a0d494c82470e8a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138041801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21c2c7aae0b17cd66e029f02c111bbff620703c08c3929192ddc2be6c8c3180`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:07:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 04 Jul 2023 02:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:07:11 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 02:07:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 02:07:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 04 Jul 2023 02:07:25 GMT
ENV LANG=en_US.utf8
# Tue, 04 Jul 2023 02:07:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:07:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 02:07:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 02:15:18 GMT
ENV PG_MAJOR=14
# Tue, 04 Jul 2023 02:15:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 04 Jul 2023 02:15:18 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Tue, 04 Jul 2023 02:15:37 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 04 Jul 2023 02:15:38 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 02:15:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 04 Jul 2023 02:15:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 02:15:39 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 04 Jul 2023 02:15:39 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 02:15:39 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Tue, 04 Jul 2023 02:15:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:15:39 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 02:15:39 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 02:15:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5fc10339ab3e8250af9a6292376d07108f76d001812e021bae7b1c21c50282`  
		Last Modified: Tue, 04 Jul 2023 02:19:31 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3264721a5f26aea471f31848de1400e7c3acc70c50a945d23e8bd3485421c96e`  
		Last Modified: Tue, 04 Jul 2023 02:19:31 GMT  
		Size: 4.4 MB (4415046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fdf08161ac818d038c48567f86fcb2a57dec72f012896ec8f8e79a326a7ce40`  
		Last Modified: Tue, 04 Jul 2023 02:19:30 GMT  
		Size: 1.5 MB (1471565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb15a94fccdafcb7d0336b4eb3a3e347e9f98cf6919ed82a26813e1d5407c72`  
		Last Modified: Tue, 04 Jul 2023 02:19:26 GMT  
		Size: 8.0 MB (8045625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03abbfe9b1d195dea1ea276ccda700d830ae317c0ce0f40a1d466f2bf78c3d19`  
		Last Modified: Tue, 04 Jul 2023 02:19:25 GMT  
		Size: 1.3 MB (1261268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7037be39d6345fa1ecc4227de34a4ca5ed4b0bb6b04bda37a989853a5a1721`  
		Last Modified: Tue, 04 Jul 2023 02:19:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8446f22be51a70626126e033bb97529c3e86d47452fcdee54db9d5473d35d0`  
		Last Modified: Tue, 04 Jul 2023 02:19:25 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9469fbc95b0a0e9be00a73f2fe615ec6835fedf9bc42de30ffc055455f450cff`  
		Last Modified: Tue, 04 Jul 2023 02:21:53 GMT  
		Size: 91.4 MB (91411128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b45daaf891d5b1ccdd55ce48ad3823f347c49ad0c43acc93564a51eb56005d`  
		Last Modified: Tue, 04 Jul 2023 02:21:41 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62142ace214fc08b4b3d58266a3e52dcd39a34bcc2e6e99fb82ffa40b51b2b96`  
		Last Modified: Tue, 04 Jul 2023 02:21:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6997fac042973930d5bd190371cf49e5ac71b634d4822696b8cf862e089c8bb0`  
		Last Modified: Tue, 04 Jul 2023 02:21:42 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c630e4d1989eea9a0c3d241a622ca5fc51ea6f013212737d6dbc4a5878f3bb7`  
		Last Modified: Tue, 04 Jul 2023 02:21:42 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:2d325fd8c3730151cd508498cfdfe96f658dc01adc47987b97b6b29a0f5f43ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131295120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c13247c0c45b6a82afc895546ad6f379906c6bf932a61ed61101cedb6a837c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:47 GMT
ADD file:2dc75d45982de1ae93d7466556a8d6f806e24a837046bd3445b5df6853b0b5bb in / 
# Tue, 04 Jul 2023 00:48:47 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:20:49 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 04 Jul 2023 01:21:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 01:21:03 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 01:21:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 01:21:21 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 04 Jul 2023 01:21:21 GMT
ENV LANG=en_US.utf8
# Tue, 04 Jul 2023 01:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 01:21:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 01:21:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 02:21:21 GMT
ENV PG_MAJOR=14
# Tue, 04 Jul 2023 02:21:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 04 Jul 2023 02:21:21 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Tue, 04 Jul 2023 02:34:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 04 Jul 2023 02:34:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 02:34:50 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 04 Jul 2023 02:34:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 02:34:51 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 04 Jul 2023 02:34:51 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 02:34:51 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Tue, 04 Jul 2023 02:34:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:34:51 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 02:34:51 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 02:34:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e5c23077f8d036e239b1eb6572155131327f3345abd95ce868b997d2e1d969f3`  
		Last Modified: Tue, 04 Jul 2023 00:52:38 GMT  
		Size: 28.9 MB (28918872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d081f4eeb9e15998004b5b80fe88f85765bd29862aedb166ba100992df0d6d6`  
		Last Modified: Tue, 04 Jul 2023 03:57:13 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87b1c06935d6d7db84a6b823ffd46a5382f3c8fd8aebef3b68e3c8c11dfa848`  
		Last Modified: Tue, 04 Jul 2023 03:57:13 GMT  
		Size: 4.1 MB (4096655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d96b51b044d1bad57aac53806e2a59d78c670e4eaa32ed23ad8641be9ccbc21`  
		Last Modified: Tue, 04 Jul 2023 03:57:12 GMT  
		Size: 1.4 MB (1448842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30628c6d13459e578f6e48a3e53eb9b7f0f39713dd726472676da0381b38ad9`  
		Last Modified: Tue, 04 Jul 2023 03:57:12 GMT  
		Size: 8.0 MB (8045505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97104034abfbb1d4028b80154ecf9a466d07acfee6ce8b3f7c7759db062b51b0`  
		Last Modified: Tue, 04 Jul 2023 03:57:11 GMT  
		Size: 1.3 MB (1257381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659cda4b07dec2ced7eea72ce7d73e1e8d90c2b3bc00ff44ae7dd69f6dfca9bc`  
		Last Modified: Tue, 04 Jul 2023 03:57:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee87bbac43987f7a785a906ffc36b99f9d1dbf67906ce3e96b6fe76fd3399cc`  
		Last Modified: Tue, 04 Jul 2023 03:57:10 GMT  
		Size: 3.2 KB (3199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb72feb1099d922e78e9729d6c6150039d90b32b8fbffc22e9acb49050ff886`  
		Last Modified: Tue, 04 Jul 2023 03:59:13 GMT  
		Size: 87.5 MB (87508090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37800567b66443f76d648c860134b06bcd079f232b93cafd46441689c94d11f`  
		Last Modified: Tue, 04 Jul 2023 03:59:00 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bae6b5ab6ccaa043b3f3378834c14f5fd959c9a737a53d13b0cb85798ecfac4`  
		Last Modified: Tue, 04 Jul 2023 03:58:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c0798876eca7e1e9eea00e460ca8c72d1938073bee1c01459124bdcbf0fa0d`  
		Last Modified: Tue, 04 Jul 2023 03:59:00 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1daa2682fe71d987755b90365a79d0555385cb6bfd879aa2ea13028213b1bf1`  
		Last Modified: Tue, 04 Jul 2023 03:59:00 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:42695fd1c703ef53af78097dba01f5e04d9412fb35c138f086a5504170b7ba47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125947609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95eaaa90efe306e3705fbb4cbc6676f004d97838fce1e3ace56506ce93d6c72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:20 GMT
ADD file:c023c66ee4b7cdae5c542f2ad2dd35aef94ad24e1b3b479a16538c46013ae6a5 in / 
# Tue, 04 Jul 2023 00:58:21 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:02:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 04 Jul 2023 02:02:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:02:17 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 02:02:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 02:02:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 04 Jul 2023 02:02:32 GMT
ENV LANG=en_US.utf8
# Tue, 04 Jul 2023 02:02:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:02:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 02:02:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 03:04:57 GMT
ENV PG_MAJOR=14
# Tue, 04 Jul 2023 03:04:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 04 Jul 2023 03:04:57 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Tue, 04 Jul 2023 03:17:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 04 Jul 2023 03:17:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 03:17:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 04 Jul 2023 03:17:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 03:17:45 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 04 Jul 2023 03:17:45 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 03:17:45 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:17:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:17:45 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:17:45 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 03:17:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d9e6a8b782e380f447723ac26499c5014f2d383b9210819b9e73e97abaf81249`  
		Last Modified: Tue, 04 Jul 2023 01:03:35 GMT  
		Size: 26.6 MB (26578754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b5f3733dcd37e4f7ff0be22dd05c52cbf7287315b183d2aabb3a5f999ca24c`  
		Last Modified: Tue, 04 Jul 2023 04:33:52 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be245a12b7ce01f847b1b50f98694f5ab54239ecc9ac71b3f38291b03352bbe3`  
		Last Modified: Tue, 04 Jul 2023 04:33:52 GMT  
		Size: 3.7 MB (3717413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13472a7e6b8ee9f7c2c6ed5bf427c2e289633f2c0d891dbedc1ddc1bfda19df6`  
		Last Modified: Tue, 04 Jul 2023 04:33:52 GMT  
		Size: 1.4 MB (1438912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71bb3b68ec7371d845a657ea40bf26b71e8853af58447af446cef05b9e858bc`  
		Last Modified: Tue, 04 Jul 2023 04:33:52 GMT  
		Size: 8.0 MB (8045541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b572871a8936b32ae766cd7b7ada93fad8bea8d7b08cc41730622933cb598340`  
		Last Modified: Tue, 04 Jul 2023 04:33:50 GMT  
		Size: 1.1 MB (1131278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79738be4a2f37d5643346f42fa07028d3a12a7e54e5db980c52653d8b5fe02fb`  
		Last Modified: Tue, 04 Jul 2023 04:33:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faa05a78a44bd0e8d6118f09301e96957d3a5c49085c4c9a3a8b83e41556138`  
		Last Modified: Tue, 04 Jul 2023 04:33:50 GMT  
		Size: 3.2 KB (3201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44cbcacbeb3323bfcbc1a2bf14eaa1100634cc37335c19e2b7d8a3a91ad000e`  
		Last Modified: Tue, 04 Jul 2023 04:36:30 GMT  
		Size: 85.0 MB (85015938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea92d100a87540d8eddaea863e4f43f454a1ab6d8aa44286916cc246a3de5da8`  
		Last Modified: Tue, 04 Jul 2023 04:36:17 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc03055440a8c5fe5c4ff727670916ad9a0828f78d27766822d44771029ed7a`  
		Last Modified: Tue, 04 Jul 2023 04:36:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1b0ff16b9032d69d580df5267ca93f5b505ce866524d1ab842c1b58f28ade5`  
		Last Modified: Tue, 04 Jul 2023 04:36:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d7134888ec7a9d2cc8a56116d37307a2e9c92cc2f87fd55a44689bdf09cc3f`  
		Last Modified: Tue, 04 Jul 2023 04:36:18 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:19d8ffeeb36e3f812b7a3d287fb958c4be92e29a45f43762b3075e049b151524
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133118536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b2611a4fed1d7954697d954a247d5055884bf1ce6fc20c13b518d72a9dec90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 10:11:36 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 13 Jun 2023 10:11:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 10:11:42 GMT
ENV GOSU_VERSION=1.16
# Tue, 13 Jun 2023 10:11:49 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jun 2023 10:11:55 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 13 Jun 2023 10:11:55 GMT
ENV LANG=en_US.utf8
# Tue, 13 Jun 2023 10:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 10:11:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jun 2023 10:12:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Jun 2023 10:12:53 GMT
ENV PG_MAJOR=14
# Tue, 13 Jun 2023 10:12:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 13 Jun 2023 10:12:53 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Tue, 13 Jun 2023 10:13:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 13 Jun 2023 10:13:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 13 Jun 2023 10:13:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Jun 2023 10:13:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Jun 2023 10:13:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Jun 2023 10:13:11 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Jun 2023 10:13:11 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Tue, 13 Jun 2023 10:13:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 10:13:11 GMT
STOPSIGNAL SIGINT
# Tue, 13 Jun 2023 10:13:12 GMT
EXPOSE 5432
# Tue, 13 Jun 2023 10:13:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10301e74546286e11f33711bbcca6589f2434199679b001c7ad555b3b515ca4a`  
		Last Modified: Tue, 13 Jun 2023 10:14:59 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a71409c6a84935ad1f398b0f7f12c942e6b302b760e441f753d3d2ba8e0121a`  
		Last Modified: Tue, 13 Jun 2023 10:14:59 GMT  
		Size: 4.4 MB (4416327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5467be1f7bdf544cccf59fd32edb7f8fb6c2aff362b6977a85334a230316cfa2`  
		Last Modified: Tue, 13 Jun 2023 10:14:59 GMT  
		Size: 1.4 MB (1403371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5eedf22017d702c77c2c7011ede83e92852e9010989903f2782a978fd39325`  
		Last Modified: Tue, 13 Jun 2023 10:14:58 GMT  
		Size: 8.0 MB (8045524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57dd01eb97330ee44bdcbe6e582c1f026738f9aa744ca2e3d6cb8f8fbecdeb8`  
		Last Modified: Tue, 13 Jun 2023 10:14:57 GMT  
		Size: 1.2 MB (1249286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c917251e7429ec9bf4e7f7cc8ed7779153a02d0f9ef736af5bf523075ab9b5`  
		Last Modified: Tue, 13 Jun 2023 10:14:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c5d43a2da839a26d6f745f2f0eb5950fdcfb23f4d1f47bbee6e8fe612d788`  
		Last Modified: Tue, 13 Jun 2023 10:14:57 GMT  
		Size: 3.2 KB (3194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e5158676a47c2b31d706cc4eaa55cb6f278247a0996c1872097cc91dd01927`  
		Last Modified: Tue, 13 Jun 2023 10:15:50 GMT  
		Size: 87.9 MB (87921414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afe68ccc59ed416141d0be06ed19549bbbea9c788ff3003248ee8ea32f2500f`  
		Last Modified: Tue, 13 Jun 2023 10:15:42 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e8dcc80c01ebf5db5d6658330a3cdc2c018b541a1d9c0ce0066515c7cac1a0`  
		Last Modified: Tue, 13 Jun 2023 10:15:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7857a64a66c27a146c8e12c42cf9b4cb31c10ddbd755be19aa8a52391bc6d3f`  
		Last Modified: Tue, 13 Jun 2023 10:15:42 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c39c63858a1c90b1d5e729d30a0ad5d96861c4cc99a03eb5a73b1b23442407`  
		Last Modified: Tue, 13 Jun 2023 10:15:41 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:9e361aa33e57a407be048b2bc94bce7e8cca4929e010b64628889f382561933f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140090087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0535e230630b17e2d13fcdafeec88863adcfc07862d649714266836e49eed4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:59 GMT
ADD file:c39e332ccb9cb890ba7896a09e9f074b3c8d67094b4eaf73d5c67e8949c2e0be in / 
# Tue, 04 Jul 2023 01:39:00 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:20:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 04 Jul 2023 02:20:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:20:43 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 02:20:51 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 02:20:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 04 Jul 2023 02:20:59 GMT
ENV LANG=en_US.utf8
# Tue, 04 Jul 2023 02:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:21:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 02:21:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 03:33:52 GMT
ENV PG_MAJOR=14
# Tue, 04 Jul 2023 03:33:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 04 Jul 2023 03:33:52 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Tue, 04 Jul 2023 03:48:15 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 04 Jul 2023 03:48:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 03:48:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 04 Jul 2023 03:48:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 03:48:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 04 Jul 2023 03:48:18 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 03:48:18 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Tue, 04 Jul 2023 03:48:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 03:48:18 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 03:48:18 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 03:48:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3466e7f9e8ec982697fc130dbb1706d708f5c53e348a638019a955c15c7395af`  
		Last Modified: Tue, 04 Jul 2023 01:44:12 GMT  
		Size: 32.4 MB (32397496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498d9a17fd0e1d28e949677d6905e992e8491b2f4b08fa6f2eab4f0e7d83eefa`  
		Last Modified: Tue, 04 Jul 2023 05:12:04 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e325143a58686d40a9f0ed5e2a2a81500ecbd8b4c44725d45b889725fd513033`  
		Last Modified: Tue, 04 Jul 2023 05:12:05 GMT  
		Size: 4.8 MB (4813643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1186f20610e3bd42421a518f66dcac9c6ded8bfa29ec7e88be2759ab51fdc695`  
		Last Modified: Tue, 04 Jul 2023 05:12:04 GMT  
		Size: 1.4 MB (1447150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229043d2a03eacccf09699b3c4361fb51e01b716432f63f08f6a3707e5c1679f`  
		Last Modified: Tue, 04 Jul 2023 05:12:04 GMT  
		Size: 8.0 MB (8045444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e50a3045bff53041f8bce869082f6ef15083e2a97ca546a87b0589c64f4358`  
		Last Modified: Tue, 04 Jul 2023 05:12:02 GMT  
		Size: 1.3 MB (1251733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349812dbc2c070cc61b044edf966a58933866a462c0132fa58abb6e7552d600f`  
		Last Modified: Tue, 04 Jul 2023 05:12:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c740dd891c26b39a040064566d0512086182a72abe1aae929c262b0d557733ec`  
		Last Modified: Tue, 04 Jul 2023 05:12:01 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c59641b02134fdfb9f1d3ab915138765f8df09862a44e1d3a20b573befbf8f7`  
		Last Modified: Tue, 04 Jul 2023 05:15:25 GMT  
		Size: 92.1 MB (92114840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1087c94e1932bde03e563ddf08ca79442520f3b149e67a20c05734f0fe4af91f`  
		Last Modified: Tue, 04 Jul 2023 05:15:06 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e096c925858bc504e1d51c203b105a847fe4f3d982f2cec5fd02d146a81ed4`  
		Last Modified: Tue, 04 Jul 2023 05:15:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29cff6777d571c32e30e583000287a5ee8794be9dd383efcc0adbfcfcc72588`  
		Last Modified: Tue, 04 Jul 2023 05:15:06 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527c1cc03e7697242161ddc2b3ab55b2bdb20e9b3596f41da873f5c19df8d539`  
		Last Modified: Tue, 04 Jul 2023 05:15:06 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:ded66681d5a334b710a1810bd8903dd5b4600934527f1453ece405dfe47f4d66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132399684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524f195d8e5fbf02c3b7717c138f6ba92d64e661810b248c0e6e4db0ae623269`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 13 Jun 2023 00:10:34 GMT
ADD file:4d5c7737e954f157e3d7ea47cc1814c46ec5c753a3d5d828ad9614969b572253 in / 
# Tue, 13 Jun 2023 00:10:38 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 05:37:39 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 13 Jun 2023 05:38:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 05:38:19 GMT
ENV GOSU_VERSION=1.16
# Tue, 13 Jun 2023 05:38:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Jun 2023 05:39:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 13 Jun 2023 05:39:26 GMT
ENV LANG=en_US.utf8
# Tue, 13 Jun 2023 05:39:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 05:39:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Jun 2023 05:39:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Jun 2023 07:46:59 GMT
ENV PG_MAJOR=14
# Tue, 13 Jun 2023 07:47:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 13 Jun 2023 07:47:05 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Tue, 13 Jun 2023 08:46:45 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 13 Jun 2023 08:46:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 13 Jun 2023 08:46:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 13 Jun 2023 08:47:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 13 Jun 2023 08:47:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 13 Jun 2023 08:47:10 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 13 Jun 2023 08:47:13 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Tue, 13 Jun 2023 08:47:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jun 2023 08:47:20 GMT
STOPSIGNAL SIGINT
# Tue, 13 Jun 2023 08:47:24 GMT
EXPOSE 5432
# Tue, 13 Jun 2023 08:47:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:61bd6562a93acd0a3b327321e5465408e1d921b3ce1fb4fe353633330c3ede91`  
		Last Modified: Tue, 13 Jun 2023 00:23:53 GMT  
		Size: 29.6 MB (29634422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073643ad5e346216479b355967f6d2c9a40527f54b879f1ce303949c212bf08d`  
		Last Modified: Tue, 13 Jun 2023 11:37:07 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d207fc98f3f6181e1511a804faf7781164662e6f3ff5e98608730cf1d5c462e`  
		Last Modified: Tue, 13 Jun 2023 11:37:09 GMT  
		Size: 4.2 MB (4196383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f8746c86b216f99c7d605ff04bb2a9aba85fcfba8ccab9a84d156b417b2e04`  
		Last Modified: Tue, 13 Jun 2023 11:37:07 GMT  
		Size: 1.4 MB (1358406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa1724d0b30a3f122e7c1502eea93f6224ef610db292c02bc921c0c666c82a8`  
		Last Modified: Tue, 13 Jun 2023 11:37:12 GMT  
		Size: 8.0 MB (8044119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986e8fb226b08566d76a7975aff59f50a8d429ee4a8f6939e132a2620860e69c`  
		Last Modified: Tue, 13 Jun 2023 11:37:04 GMT  
		Size: 1.1 MB (1089556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00877d40b9facfe51d324e422defee4c467842fda5effcfbe4735cd87b7650a1`  
		Last Modified: Tue, 13 Jun 2023 11:37:03 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff950b66d453f99c73a908940521fe723c1e003305e159c403102f8bd4f37999`  
		Last Modified: Tue, 13 Jun 2023 11:37:03 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f374a1f1b8a0ba9ce5494d0204bfb01ad30f1cdf7b7a1b419597cd2b81bbdc7`  
		Last Modified: Tue, 13 Jun 2023 11:40:20 GMT  
		Size: 88.1 MB (88057286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12ed2212ea27b3f9d68ecb790082835a5807bc7605834c45df0b79b78c4dc20`  
		Last Modified: Tue, 13 Jun 2023 11:39:26 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bbf57b2c825f2b0f3c65545f2a3c35d3881852194c0401a088ef1202e2e392`  
		Last Modified: Tue, 13 Jun 2023 11:39:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62175c8bfc181b10cfd66e8a4dba9a45b7cd805e69bbc8c54341fe9affbf127e`  
		Last Modified: Tue, 13 Jun 2023 11:39:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460fb5d031b85b395c2936b792a48a7ffe81fd9d674d64bd644e378b02434d77`  
		Last Modified: Tue, 13 Jun 2023 11:39:26 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:f3fdfe97a2181ded768cbde7616d2a31532a2ff9bf8f36486eb2e63d141fb5a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.1 MB (147111813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619660f96db29e46813e6dd63120e7d5fd1640483d9c92b974da510964ee2fed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 04 Jul 2023 01:18:33 GMT
ADD file:37fa020aca7253d41d395ed529c38db73caaa4da098754836244552f65fa7d5d in / 
# Tue, 04 Jul 2023 01:18:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 02:02:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 04 Jul 2023 02:02:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:02:37 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 02:02:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 02:03:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 04 Jul 2023 02:03:10 GMT
ENV LANG=en_US.utf8
# Tue, 04 Jul 2023 02:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 02:03:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 02:03:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 02:17:15 GMT
ENV PG_MAJOR=14
# Tue, 04 Jul 2023 02:17:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 04 Jul 2023 02:17:15 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Tue, 04 Jul 2023 02:17:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 04 Jul 2023 02:18:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 02:18:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 04 Jul 2023 02:18:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 02:18:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 04 Jul 2023 02:18:09 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 02:18:09 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Tue, 04 Jul 2023 02:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:18:11 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 02:18:11 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 02:18:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:147bb8b5828c99cd6b07d252d2987490463c142099eaa0815025685f8fa4f3d8`  
		Last Modified: Tue, 04 Jul 2023 01:25:40 GMT  
		Size: 35.3 MB (35291082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fe06070e673f2d7b6a8d277efe239f788b26c2dec01cd584140f6a0797e6f9`  
		Last Modified: Tue, 04 Jul 2023 02:28:22 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239670d8326535190821797fb46941bb4d3d55cfb6236874ca15f4f882ada804`  
		Last Modified: Tue, 04 Jul 2023 02:28:23 GMT  
		Size: 5.2 MB (5222952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a1c1287f15c67db8c9f43c797de43469a5dcc38925e2b344327bf73a6d55b`  
		Last Modified: Tue, 04 Jul 2023 02:28:22 GMT  
		Size: 1.4 MB (1393351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bec0c768ceb67969e662cdd3861a52551f93b2f800c9740254b0b293bd86e3b`  
		Last Modified: Tue, 04 Jul 2023 02:28:22 GMT  
		Size: 8.0 MB (8045654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093d7eb93c9847882b8c0e6106b7ecf7b23137457ccaa79a33f737fbc8eb07d7`  
		Last Modified: Tue, 04 Jul 2023 02:28:20 GMT  
		Size: 1.4 MB (1420279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6d90e7f86504a9e26cd8ad551b6488d56f956f6c74120bc3cb2c8f28e3f8f1`  
		Last Modified: Tue, 04 Jul 2023 02:28:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6185ea52f35c7c59d43d0e200114ba9117df5bd9cf4f9c756d15c66e9e8d7db5`  
		Last Modified: Tue, 04 Jul 2023 02:28:19 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591abc2d33f7f8016e938027b3abdc94cae7b2e2633f36ccf9bbdec23efffda8`  
		Last Modified: Tue, 04 Jul 2023 02:32:43 GMT  
		Size: 95.7 MB (95718720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af3fcb73192636c2866dcd2be91070a5ae351222f3b88462b362484a2e419fa`  
		Last Modified: Tue, 04 Jul 2023 02:32:21 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5912ae8a66573631ad5b176dfca361084059ddc4bfac0f22a4cee3b98d539f88`  
		Last Modified: Tue, 04 Jul 2023 02:32:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b983ce2d618a49d8a8dd0c29ad05e4aeeee44f182ab924843ace6454e52c79`  
		Last Modified: Tue, 04 Jul 2023 02:32:21 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e329bbf43f393979985ee8c285900e975be0302f1f6a5846dfc328714c1bc31c`  
		Last Modified: Tue, 04 Jul 2023 02:32:21 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:14-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:e0ed27238c886c364b06d3cd53350f7bc482f888b4c8140ccff0f5fc433b7431
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141664653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4825fccdad7c4e428156786192468f85365e510e43ce2af9c20f5a4d129f4adc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 04 Jul 2023 01:32:44 GMT
ADD file:799c0afa70fa3bf4bb7804964481cba79e80aa3fad5c7a25beadde206ed6a8ff in / 
# Tue, 04 Jul 2023 01:32:46 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 01:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 04 Jul 2023 01:59:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 01:59:00 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 01:59:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 01:59:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8
# Tue, 04 Jul 2023 01:59:13 GMT
ENV LANG=en_US.utf8
# Tue, 04 Jul 2023 01:59:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 01:59:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 01:59:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 02:09:02 GMT
ENV PG_MAJOR=14
# Tue, 04 Jul 2023 02:09:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 04 Jul 2023 02:09:02 GMT
ENV PG_VERSION=14.8-1.pgdg110+1
# Tue, 04 Jul 2023 02:09:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version
# Tue, 04 Jul 2023 02:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample
# Tue, 04 Jul 2023 02:09:27 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 04 Jul 2023 02:09:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Jul 2023 02:09:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 04 Jul 2023 02:09:28 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Jul 2023 02:09:28 GMT
COPY file:512acb0aab31f9e5d908f16e2f4478f65cddd5d4e555a02a1551074bb16f54d7 in /usr/local/bin/ 
# Tue, 04 Jul 2023 02:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 02:09:28 GMT
STOPSIGNAL SIGINT
# Tue, 04 Jul 2023 02:09:28 GMT
EXPOSE 5432
# Tue, 04 Jul 2023 02:09:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbee891481f2623da9c7d37a49947926519c858c2b06773370a6189440d4b4de`  
		Last Modified: Tue, 04 Jul 2023 01:37:37 GMT  
		Size: 29.7 MB (29652540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06c898ae2477811f8161971c5f4b3591f7058030d36974f34fe2821e5047ed7`  
		Last Modified: Tue, 04 Jul 2023 02:15:53 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0766d6ce61b3eb60a952a1bfbc2319884464f0f407199becfb3ad551486b098`  
		Last Modified: Tue, 04 Jul 2023 02:15:53 GMT  
		Size: 4.3 MB (4302386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4a36ac3046bbb6158e7031594e22170e0df48ea22c9292b5d800ada1a11cb3`  
		Last Modified: Tue, 04 Jul 2023 02:15:53 GMT  
		Size: 1.4 MB (1437269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a8f26c5d5287a511f54885d8709d66702628a400b16fa1c9f127fdcbc05da9`  
		Last Modified: Tue, 04 Jul 2023 02:15:53 GMT  
		Size: 8.1 MB (8099401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85cbf61dfe745ae9c4e47bed07e1ea795d88a3b4865c095fb568c0c2a440a89`  
		Last Modified: Tue, 04 Jul 2023 02:15:52 GMT  
		Size: 1.2 MB (1238077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0757e83426ec7e1d8194dbb62616bc446da0aaa6b355a98358605126a773d8`  
		Last Modified: Tue, 04 Jul 2023 02:15:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e339b146ed21039efdc9c30801cc7b638cc9fe4c4139568ff3adfd0e675a120a`  
		Last Modified: Tue, 04 Jul 2023 02:15:51 GMT  
		Size: 3.2 KB (3200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81aeb4c3a0dd9d11fb8a26b46c5c2d489c97c9ac37cd42a46a7261df30b3d509`  
		Last Modified: Tue, 04 Jul 2023 02:18:13 GMT  
		Size: 96.9 MB (96915196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57aa5a6b6aa3dcf0e372d5fc2313a0aae51c939c4a6d4061acfa36a62461db41`  
		Last Modified: Tue, 04 Jul 2023 02:18:00 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0387c81dddb60fe49bb68b235cb2609a09c23b29d1fc8a97f65697f28d8ca1b`  
		Last Modified: Tue, 04 Jul 2023 02:18:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1ac8195fa2ce2788c289ff8d1da348d9f415e61f2c02366f191e5ac547dbfd`  
		Last Modified: Tue, 04 Jul 2023 02:18:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02af506541f268ba6357af0f3da06d902c90cf118631fad23ed0492f0679ae0d`  
		Last Modified: Tue, 04 Jul 2023 02:18:00 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
