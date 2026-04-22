## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:c30575d46712280d262e09e63570324a7253e17580675284541876c8ef27da80
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

### `postgres:16-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:ddb18bbc2fbd1ebb760e4a1e18beb2f3931b02540c7b3666ef979103b31f04a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155038496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facee8ded805a6843af36d66788def7da8c5faeb9a5d6138baab4a18ad742227`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:32:37 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:32:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:32:48 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:32:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:32:52 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:32:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:32:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:32:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:32:56 GMT
ENV PG_MAJOR=16
# Wed, 22 Apr 2026 01:32:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 22 Apr 2026 01:32:56 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Wed, 22 Apr 2026 01:33:07 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 01:33:07 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 01:33:07 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 01:33:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 01:33:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 01:33:08 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 01:33:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:33:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 01:33:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:33:08 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 01:33:08 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 01:33:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a53e925fd9555e0abba1c42bf3c76f23f46aa675533c3c321fa3dfbd602d50`  
		Last Modified: Wed, 22 Apr 2026 01:33:27 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085614a87a8e9818644fc07b59b81ac39d938738a1cbb8b8aac068e05ab07344`  
		Last Modified: Wed, 22 Apr 2026 01:33:27 GMT  
		Size: 4.5 MB (4534241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8047b4ef40ffc4c727b1a4e5602fec3ebbfdb696a8d3a142423763f96fc42a3`  
		Last Modified: Wed, 22 Apr 2026 01:33:27 GMT  
		Size: 1.2 MB (1249542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c883ba792057c2bd4626a14cc57dfb432dd84ec701aa8569a356807e063dc40b`  
		Last Modified: Wed, 22 Apr 2026 01:33:28 GMT  
		Size: 8.1 MB (8066444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a5040237bc67794be6711dd661187aac9840c3b6c1d00e6682914f915204b4`  
		Last Modified: Wed, 22 Apr 2026 01:33:28 GMT  
		Size: 1.2 MB (1196411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec3ed948d94395abe643ee16ba0ada04cbea6bd119473a51ecf7fd436392287`  
		Last Modified: Wed, 22 Apr 2026 01:33:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdca04122849d4731f0d4282eeba113cb873e2329c6eb758ec382fc6601e69c1`  
		Last Modified: Wed, 22 Apr 2026 01:33:29 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7689acbb638f147cb5d8bcf0cb5f731604da5680d5b41c1e2fb2b84207c27d7`  
		Last Modified: Wed, 22 Apr 2026 01:33:32 GMT  
		Size: 111.7 MB (111734633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d03bb458bb6ebfdbd06db732906800d1a9c5a55b443880c40f29236208750cb`  
		Last Modified: Wed, 22 Apr 2026 01:33:30 GMT  
		Size: 10.0 KB (9967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cdc1ca34c9bd9270e425b331e672dd16306eb6becb0551fac978aee3fa81f`  
		Last Modified: Wed, 22 Apr 2026 01:33:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5cf3911f67bb3455b967dbce97b07322eeab4430f6defc04b2530f1bf0b22d`  
		Last Modified: Wed, 22 Apr 2026 01:33:30 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710f3e46e1edd42530a0c50cb25b4e1f21fd7376d7a2595895326d0a9c1a3bd5`  
		Last Modified: Wed, 22 Apr 2026 01:33:31 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861c842b76f8040a520ffb546b65d88b782650ffc02ce2d25e2b639bfab37698`  
		Last Modified: Wed, 22 Apr 2026 01:33:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:df6f5facea233ada732e1b69257d1d7539cafb269792992c1099fd9a428947d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efadc48b06710f07403e786d4c6d8e2ed2a3d800387f12a9be79327616ad1c7b`

```dockerfile
```

-	Layers:
	-	`sha256:2b9bbf8093280bfd3d562f5d927d1cd8b56fe5979e9fb42651e92c8817063733`  
		Last Modified: Wed, 22 Apr 2026 01:33:28 GMT  
		Size: 5.9 MB (5909556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:920d1c3dde00eabd8693c6d328f0a4f553bbca81fa02471c12fe1431d6209527`  
		Last Modified: Wed, 22 Apr 2026 01:33:27 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:f2945d893b480f26b6c39bb9e285d1bc137e8c7511837772f2b8626c9e001fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148047817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d386b9e0df96e59dac3abc3210ea0f2b2dbf1517802e14c09d39838e6d089a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:24:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 02:24:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:24:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 02:24:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:24:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 02:24:29 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 02:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:24:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 02:24:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:24:35 GMT
ENV PG_MAJOR=16
# Tue, 07 Apr 2026 02:24:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 07 Apr 2026 02:24:35 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Tue, 07 Apr 2026 02:40:51 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 02:40:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 02:40:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 02:40:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 02:40:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 02:40:51 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 02:40:51 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:40:51 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 02:40:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:40:51 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 02:40:51 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 02:40:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4748d6bbb5a5b9e671dcabe2f909bdd7514f760a5cfdcd37d5b04627424120f2`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 25.8 MB (25765667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996596f1df3794faf8d0cc273aa40a4ff2c3aabb9204a470ea71619f70b90905`  
		Last Modified: Tue, 07 Apr 2026 02:41:10 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9665a276b6a9005feb3543b88e7116bf7c980d7ab88829d8ef5477f26de33ec`  
		Last Modified: Tue, 07 Apr 2026 02:41:10 GMT  
		Size: 4.2 MB (4151301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1f7083babc0251d48083cbe5697f7e534f052362bcbcf1cef0f85825cd1bc3`  
		Last Modified: Tue, 07 Apr 2026 02:41:10 GMT  
		Size: 1.2 MB (1220105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be09106a9f6eebf9bc1301362d36cdf76f5bc851e47fdeaad688069feec4c400`  
		Last Modified: Tue, 07 Apr 2026 02:41:10 GMT  
		Size: 8.1 MB (8066574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e4d2193dc45403c72bfe0847051e5ced95ecf9ba5ffa63545be3d407a9be6c`  
		Last Modified: Tue, 07 Apr 2026 02:41:11 GMT  
		Size: 1.2 MB (1195071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71adf7bdf243f6957db75835b706571bd11c271dcd35d294ac23464149078f69`  
		Last Modified: Tue, 07 Apr 2026 02:41:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380a5e890dc8ab21f9a24fcbd8d4f791fb6c6d831d0e613f329ee61feae23480`  
		Last Modified: Tue, 07 Apr 2026 02:41:12 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8cf119fb1f71059514fe18bb58f39b7bbd5d669146ea674378ea6465fc895f`  
		Last Modified: Tue, 07 Apr 2026 02:41:19 GMT  
		Size: 107.6 MB (107628377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06aced74f15c82e5cf6606fade37b8d0d1993b26f856d816574c14d7807f5c11`  
		Last Modified: Tue, 07 Apr 2026 02:41:13 GMT  
		Size: 10.0 KB (9973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7909b51f81987482b9898630e0189bce2dd67ee2daca57d9e1065fcafbe4b11a`  
		Last Modified: Tue, 07 Apr 2026 02:41:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb022a12a81cebe95cc55b12efc79b63ff63a8667e999b868c989b37e2556b9b`  
		Last Modified: Tue, 07 Apr 2026 02:41:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfa31ecd214bb235c8b7408785e374f370fbc8b8b6e3644682d77b57c904012`  
		Last Modified: Tue, 07 Apr 2026 02:41:14 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7374e872a9dba56188b7e7b17166fe0cac53fb67449bd65ed7f608f25888cb57`  
		Last Modified: Tue, 07 Apr 2026 02:41:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b53b504147208f8ca6653ab43d12a66084914f253bce66229bc5b1145de90027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db9f613435983b9a3f0c2a70e76f85f8f378663121898f966d0c6deaf38cf81`

```dockerfile
```

-	Layers:
	-	`sha256:e4b6a666d16c4f0e6c55882089134c0dcb374e5e23a3214640cf318ea32cbe35`  
		Last Modified: Tue, 07 Apr 2026 02:41:10 GMT  
		Size: 5.9 MB (5927653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c312c5ebf6f10fb6a6afb620b2d3596d0d77869c27fd6bc627a9a05b9967d2`  
		Last Modified: Tue, 07 Apr 2026 02:41:10 GMT  
		Size: 53.5 KB (53502 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:03c49e8390ac6f0db1528e9b8175da3533375fcfc46b3db1c1952ee5b36f0b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143081166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c507ff4350925abb011652eb309c3f7f251a01cdb443944d034b2c17f392e980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:38:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:38:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:26 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:38:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:38:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:38:32 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:38:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:38:36 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:38:37 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:38:37 GMT
ENV PG_MAJOR=16
# Tue, 07 Apr 2026 01:38:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 07 Apr 2026 01:38:37 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Tue, 07 Apr 2026 01:53:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 01:53:21 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 01:53:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 01:53:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 01:53:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 01:53:21 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 01:53:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:53:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 01:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:53:21 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 01:53:21 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 01:53:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02213217f791b9ee0be333f5af3a790fa7bfa536ca01205a34b62c9cf69cb38`  
		Last Modified: Tue, 07 Apr 2026 01:53:39 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2d06a7a9c239b0fcebf5946dc2d09af2b29c197793f9cc81dc59d2a326bb0`  
		Last Modified: Tue, 07 Apr 2026 01:53:39 GMT  
		Size: 3.7 MB (3742733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f0645b4a8a12ad1ba04475529058037ee46b434f3cd36f76b2bcf8ba3ec9f0`  
		Last Modified: Tue, 07 Apr 2026 01:53:39 GMT  
		Size: 1.2 MB (1216022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e229421e220b4e2fc1146d7995ac1fa9a455fe3344eddb190230822f490ddf84`  
		Last Modified: Tue, 07 Apr 2026 01:53:39 GMT  
		Size: 8.1 MB (8066434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bee691741dd9c5e886d869d61972f51a597c74d3588dddd7f9caef66e7be25`  
		Last Modified: Tue, 07 Apr 2026 01:53:40 GMT  
		Size: 1.1 MB (1067272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08468edf5ded45cc465503db546b512cd789216d206335bca7e8a0b143faa323`  
		Last Modified: Tue, 07 Apr 2026 01:53:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560043487a31d081ee1ce5eb10236d4a8ea6b5398592e7fa4a1c94ecde1dbdbb`  
		Last Modified: Tue, 07 Apr 2026 01:53:40 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f97347178423284d5ab25ac7242722a98332be6bbfd548b4e7a50572ba9107`  
		Last Modified: Tue, 07 Apr 2026 01:53:43 GMT  
		Size: 105.0 MB (105026513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9e1dc9635b0b69d0f76c29d39020b48cfc2802964b70fcc24fe0e395894b1c`  
		Last Modified: Tue, 07 Apr 2026 01:53:41 GMT  
		Size: 10.0 KB (9974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61bdb66e00627d81d047d2975c05d8a4cd195ff6afc74d4a29331634dfca492`  
		Last Modified: Tue, 07 Apr 2026 01:53:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a2a4b557f193e68ca31ff91a9fe9e08c1710bed8127d9b866e759222a5da12`  
		Last Modified: Tue, 07 Apr 2026 01:53:41 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288e35139305df797673fa53fd6ae632b661f8d4fcb8533d450795dbbe37ed29`  
		Last Modified: Tue, 07 Apr 2026 01:53:42 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac50394b99cb690d494bc7b82fe6471f02530e0ea72a492cd9d0850f49a9859`  
		Last Modified: Tue, 07 Apr 2026 01:53:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:23fd401a8dea40f4ead8af42e77e3514c96db71efe8dd5804eae9d803be0c696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5763bf37dbbcdc6207fb103b3488f8883f449e010d7cb9cb28516b4099a3466`

```dockerfile
```

-	Layers:
	-	`sha256:30e85d75369c50618d325891073de25cdfe5f94071d55a09efd7ed59d255b6d7`  
		Last Modified: Tue, 07 Apr 2026 01:53:39 GMT  
		Size: 5.9 MB (5926908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6370b2f15c0b6e68a512c5bab3f9bd97189a4167f6e34e82b7b72f99d55c7d1b`  
		Last Modified: Tue, 07 Apr 2026 01:53:38 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:d731824e736797b76e33c68efad4d8a9c107303c134b5204c0f505c18c1f097b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (153024910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c12fbd92486ad80d5c4acee23ca4579ebdcbb4f978e14ae7bce706a5ece326e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:42:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:42:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:42:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:42:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:42:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:42:26 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:42:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:42:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:42:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:42:30 GMT
ENV PG_MAJOR=16
# Tue, 07 Apr 2026 01:42:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 07 Apr 2026 01:42:30 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Tue, 07 Apr 2026 01:42:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 01:42:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 01:42:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 01:42:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:42:42 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 01:42:42 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 01:42:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7287f2d0aa94a25a999e5aca3c62ff41517955571d33a8aacc3bf26deaac354c`  
		Last Modified: Tue, 07 Apr 2026 01:43:01 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f48923c014f388b86815bdeaba56eaa662f7f8a978434d06373a95c47ba1b02`  
		Last Modified: Tue, 07 Apr 2026 01:43:01 GMT  
		Size: 4.5 MB (4519546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833b9f87649dc251beb06f1f6f51d7671978a59f7a5bca074a956e6458105183`  
		Last Modified: Tue, 07 Apr 2026 01:43:01 GMT  
		Size: 1.2 MB (1203276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7e5d893fae5ae8054fd4cf59be0417697343a77c40768091e7616a7e01d0ae`  
		Last Modified: Tue, 07 Apr 2026 01:43:01 GMT  
		Size: 8.1 MB (8066548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8938c414a838bb24937e62924f85303e9809976e8735a62b5a5fe618c8b3698`  
		Last Modified: Tue, 07 Apr 2026 01:43:02 GMT  
		Size: 1.1 MB (1109018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d203b86ce9e1b61c31fcb6dda75efdeecfa1e2b2330da4773a7cd622301a311`  
		Last Modified: Tue, 07 Apr 2026 01:43:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7697fdbc8b917782db1769310c7834cdfb27509ded35c3ab4d79bab51f0525`  
		Last Modified: Tue, 07 Apr 2026 01:43:02 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89aba65034435ec10fd65d611031633267269c1414881d42c640db6e98421bc`  
		Last Modified: Tue, 07 Apr 2026 01:43:05 GMT  
		Size: 110.0 MB (109989640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3682c7b6f6d4aa152cd8d7b435fa2542ed8abd722d48d173e8b6ab1407eb5320`  
		Last Modified: Tue, 07 Apr 2026 01:43:04 GMT  
		Size: 10.0 KB (9967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba68532cdcc86e0e6abd696a6fa0138d11d4a37f323039ce21858b9969e4e09d`  
		Last Modified: Tue, 07 Apr 2026 01:43:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249acfd119e7c50d61efbdebded19c6a823f6a8645a4f561ec1009e164cd80f1`  
		Last Modified: Tue, 07 Apr 2026 01:43:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e8baef7b6370688e983e49b31032a4d25d15a542b7a7bbd06f4569e5b7cdd3`  
		Last Modified: Tue, 07 Apr 2026 01:43:05 GMT  
		Size: 5.8 KB (5838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd5ed2525098979c68e7a24fde4e8eedf139aabcd7713066e488924d19b371e`  
		Last Modified: Tue, 07 Apr 2026 01:43:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:c1ea3a358edf8d5b3dc7b20a6aa411e730cb0628a8120321c44c67f0d2047bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5969408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5413ad3a2a422fd6c38a78fbded069ba8d58d818182a4313c1abdebe2e57a3`

```dockerfile
```

-	Layers:
	-	`sha256:4123d3052a4b28abda4dd7fdb367c2e1199562a8c0e5dcabae075048734b1f60`  
		Last Modified: Tue, 07 Apr 2026 01:43:01 GMT  
		Size: 5.9 MB (5915867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:412b3361cbfe3460544e2dce8fa3a083eafdd8e13208d3e50c3bb712e88b4a08`  
		Last Modified: Tue, 07 Apr 2026 01:43:01 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:11c78bae28f277c99f667f8740051468b03c3e36897bbdc057667c4606cc8919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163837794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196de7c8d2562baab995534dc2c32a38d4b106bbe5ebe9e6cd4ba343b535acf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:36:29 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:36:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:36:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:36:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:36:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:36:46 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:36:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:36:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:36:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:36:50 GMT
ENV PG_MAJOR=16
# Tue, 07 Apr 2026 01:36:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 07 Apr 2026 01:36:50 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Tue, 07 Apr 2026 01:47:20 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 01:47:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 01:47:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 01:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:47:20 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 01:47:20 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 01:47:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75484923cb1a9a0675f98e7a7758d5d2938142f83fba3f666daa086a462021f4`  
		Last Modified: Tue, 07 Apr 2026 01:47:39 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b509c0599788927d79d1e0a06719b6bd99451a62aae1b81f24214f9a0cb91f5`  
		Last Modified: Tue, 07 Apr 2026 01:47:39 GMT  
		Size: 5.0 MB (4966091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d596207ec833b44abd8b2e850bf0aba77a736aa3c1546f1c7685faee432c84`  
		Last Modified: Tue, 07 Apr 2026 01:47:39 GMT  
		Size: 1.2 MB (1218671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79a7a43425b5b5695f2bb3f721bef6be844a08fe82cd829d93f372dbdfbcca7`  
		Last Modified: Tue, 07 Apr 2026 01:47:39 GMT  
		Size: 8.1 MB (8066453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b56162cd9613c74ea287f873c03aa0cc74170192c7fd9e7e0b37b53357ca8f2`  
		Last Modified: Tue, 07 Apr 2026 01:47:40 GMT  
		Size: 1.1 MB (1137488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ad0bb9910dbeb148f60eea7a7524e2511c7ed2d08061c190a5a00ba4a03466`  
		Last Modified: Tue, 07 Apr 2026 01:47:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5aa04628ebc1f86ba87e414a70c294f31f17b28bd4ec36a23df483acd8064f`  
		Last Modified: Tue, 07 Apr 2026 01:47:40 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30f5ae27807c86131f52043e0b40768ca4f1c7a25dcc881f1291509aa82ff6d`  
		Last Modified: Tue, 07 Apr 2026 01:47:44 GMT  
		Size: 119.2 MB (119206605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd91dbbb5dbe60f875643aa470c3f1488f4f5848c37b41f17ccf3e0c72a084cc`  
		Last Modified: Tue, 07 Apr 2026 01:47:41 GMT  
		Size: 10.0 KB (9970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5518a82e1bedf5341842e2a47bd19dac64c5af630ab7188d1827cdb2c8431858`  
		Last Modified: Tue, 07 Apr 2026 01:47:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662b694071c83271e718094904199c8d7747d996ab3467aecc29043b3bc2e94e`  
		Last Modified: Tue, 07 Apr 2026 01:47:41 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8bae3b4a649938c19390ee7bec75164a0c38f8b0f4e01e00ce2df9467b418b`  
		Last Modified: Tue, 07 Apr 2026 01:47:42 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a647dad8d4cfc90bc6c85805c762d7c805d24eeaf8b34c5037e83c6565cdff`  
		Last Modified: Tue, 07 Apr 2026 01:47:42 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4b1d32d150e14bb24309b2b04662b63119d16ed3f17f966f5cef320996c09627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5979048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a626677d15f97e39f79169b517acf2da9b705f5b3186f6dad3dd8f19bf7f57`

```dockerfile
```

-	Layers:
	-	`sha256:dcc6a240e0dc2145dcd20c001e121668699da0a76de90a4168f59824a8b2aa35`  
		Last Modified: Tue, 07 Apr 2026 01:47:39 GMT  
		Size: 5.9 MB (5925796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8516e0f8d8a7a384d0dbd9d179a2d628f0e50e217312eb18b85e9b5919efa38`  
		Last Modified: Tue, 07 Apr 2026 01:47:39 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:0f2f5d8b53fe05d954ae60c47ffe7d3be612be4d7bb03b1b400ed197d2cf380b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153892128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7eb611a163356bfb236d158e10eb722ccd38e8511cc31ab94fb8867ad832d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 08:36:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 08:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 08:37:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 08:37:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 08:37:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 08:37:45 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 08:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 08:38:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 08:38:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 08:38:08 GMT
ENV PG_MAJOR=16
# Tue, 07 Apr 2026 08:38:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 07 Apr 2026 08:38:08 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Tue, 07 Apr 2026 12:11:11 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 12:11:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 12:11:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 12:11:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 12:11:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 12:11:17 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 12:11:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 12:11:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 12:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 12:11:20 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 12:11:20 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 12:11:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7377a524ccdc918cca6272a35a48618805ffa8fb443fe7f687971509cb1f8d53`  
		Last Modified: Tue, 07 Apr 2026 00:10:05 GMT  
		Size: 28.5 MB (28526285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577deaa1ee6306b521ee5d84ddaf65f0450bfb69e5e2e10ace88d337c6cba4f`  
		Last Modified: Tue, 07 Apr 2026 09:51:03 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2193f14079132665de93d8fc43dbccb2d7e4a15aa9874d91ad7b6e9774f5548b`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 4.5 MB (4475247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9d1210a9eb3ea5aff9a27d0fed962b67d985e781ebf9b4aeae64f122914c0`  
		Last Modified: Tue, 07 Apr 2026 09:51:03 GMT  
		Size: 1.2 MB (1159244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e47fef44ca5ddd3d584b459d7fa9e53ad74dda9d20319868217ecaefd5e4ead`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 8.1 MB (8066561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64e531094ee8eda299eb99703ce16f6ccb0dec62e0d8395c5229bdf89943ae6`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 1.2 MB (1182905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66a1323700edb806f7d1852762ef08ab512cd2cb6d3d752c4ce5cc357bab520`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09b94ca6add0648b12298fad493162ceca74e3a56abda4b44871cf3d96266d`  
		Last Modified: Tue, 07 Apr 2026 09:51:05 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a353ad5990547999c3f4a135bab9eb32cf27cfd4c4d1c4660f4a845e1b899deb`  
		Last Modified: Tue, 07 Apr 2026 12:13:26 GMT  
		Size: 110.5 MB (110461155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9dbf2e6f17f2ee8f2d634cbd204299c265024da5e787d6846eba9712bbc7ca`  
		Last Modified: Tue, 07 Apr 2026 12:13:14 GMT  
		Size: 10.0 KB (9971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6f6891826b88d0dea0156cd961f4cd8733431e8a571a4ae232dc665f3b8059`  
		Last Modified: Tue, 07 Apr 2026 12:13:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95829cb73fb4ffb1ead92f0d4a1d551a02837b68a77b5d6f431810d7b02594c0`  
		Last Modified: Tue, 07 Apr 2026 12:13:14 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3a23ff0d7edd8149c74c7ab730ab67cacd254fd035d67f804b8373a6d3678c`  
		Last Modified: Tue, 07 Apr 2026 12:13:16 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485960aa78f0701d469d8e0f9bfceb55a4913f6a57a2af7b8d3ece9c96e5b8d6`  
		Last Modified: Tue, 07 Apr 2026 12:13:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d24312cc45781eb63dbc9962ba97e569eed4ac651118e4b0ba77c824ec3001e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c72ef9e7afa8bc96385ceebfd5a90ee1a42c69319c855c31b0a842d39bd9e33`

```dockerfile
```

-	Layers:
	-	`sha256:d761b92d42e0acd42f0d824d1eb4c7b7dec7bd8d97067b2cc3cd4d708c6c0e02`  
		Last Modified: Tue, 07 Apr 2026 12:13:14 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:99ba581fe787f46618e097155b54c6225ddbed03787614f976febcb8fe843b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167786580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bde10efd5908bcfb8f64c182f44d302c7da258d407f2cf9eed5b219adccbee7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:01:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 04:01:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:01:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 04:01:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 04:01:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 04:01:43 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 04:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:01:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 04:01:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PG_MAJOR=16
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Tue, 07 Apr 2026 04:05:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 04:05:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 04:05:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 04:05:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 07 Apr 2026 04:05:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 07 Apr 2026 04:05:52 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 07 Apr 2026 04:05:55 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 04:05:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 04:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 04:05:58 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 04:05:58 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 04:05:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c73a4e80f8eee9e890cb47bedd35d02c67ef5bcca2b473c6d3e00a80965b06a`  
		Last Modified: Tue, 07 Apr 2026 04:04:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7947f119f83a299b47ca573148739e01949d18cbaa9318e7ab4a40e85e5823df`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 5.4 MB (5368665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2363b8d0c3c8477a5c830c8f04da66b6b2dbe1de9983fe4475a83363c62b90`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 1.2 MB (1208247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73441d3fd6b801869bfe2128fece0f8cfd3dae11351c3d17ba334f6a60758933`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 8.1 MB (8066577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825f5e783521a55f9a2725ca3ae6863c9ebc88d6eeb23db6ad9f4a50720cb7f`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 1.3 MB (1283671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255852130442a8dd66f03e76d6c53fb783681b9f0b0f0deb8976c69d771ebc43`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b958c25dd0ceaa8626e0e80c7b5ef496a8edd59a35e667fc15c63e5053d77b`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda398bd92d8b972fed35defd31d76be9d11c04570150d465248efe33442599d`  
		Last Modified: Tue, 07 Apr 2026 04:06:44 GMT  
		Size: 119.8 MB (119760238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7da54f026855b5b8426dfba52298abb862acdd542bfaaba2f6d316ade48097`  
		Last Modified: Tue, 07 Apr 2026 04:06:41 GMT  
		Size: 10.0 KB (9970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f3e4fcca4baf44bc7744e214139bff6b1ea5f9d659782bf40b82aa10e31e09`  
		Last Modified: Tue, 07 Apr 2026 04:06:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e323d8e7a68ea4ce4cadefe872eb0b42b3a85690e2c8c484f3da4b9e257c1ce`  
		Last Modified: Tue, 07 Apr 2026 04:06:41 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d4bf73ac6a642032c0c1c93f11d31c0b4e5b6aa83bd74c43413bd202193af`  
		Last Modified: Tue, 07 Apr 2026 04:06:42 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922605a1bb5bb746d6430014632a095a60ae5a3fe4e6f86e9d449571fbc9ce83`  
		Last Modified: Tue, 07 Apr 2026 04:06:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:dcd25039317bea6535a680d179fc082a5bdff0ad7c516f206258fd85312cd58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aa11cf74c69ffccf121d131d0426776e2366b257de0613dcb32bc4e332fcea`

```dockerfile
```

-	Layers:
	-	`sha256:efa5d11d9ba54bb6483c1594d5ea1117de524f226e131579907f867cf9287039`  
		Last Modified: Tue, 07 Apr 2026 04:06:41 GMT  
		Size: 5.9 MB (5916917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30bba257d8ba4776713daeedf4d1659c891550837005ea875e15efaa603019a6`  
		Last Modified: Tue, 07 Apr 2026 04:06:40 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:a36e052e4678f44322cad32a66774f915f308d06033bdb3214abb52d78679d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164267711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0cd16169876b7d51bbbf5c4094d2990c75931afba4c9b31d6c15458b7dee2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:57:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:57:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:58:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:58:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:58:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:58:09 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:58:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:58:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:58:13 GMT
ENV PG_MAJOR=16
# Wed, 22 Apr 2026 01:58:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 22 Apr 2026 01:58:13 GMT
ENV PG_VERSION=16.13-1.pgdg12+1
# Wed, 22 Apr 2026 02:23:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 02:23:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 02:23:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 02:23:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 22 Apr 2026 02:23:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 22 Apr 2026 02:23:16 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 22 Apr 2026 02:23:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:23:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 02:23:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:23:16 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 02:23:16 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 02:23:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902f96924f46ebf5f9f8ede07708f5b0c8adeebd2738997fa3533ddf09a9dbd2`  
		Last Modified: Wed, 22 Apr 2026 02:11:50 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd6b3c43306aab3a4d709a248ab52f9fcf51cea15d3562af15efab3e151778c`  
		Last Modified: Wed, 22 Apr 2026 02:11:50 GMT  
		Size: 4.4 MB (4391190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c975be715805f88cd7ca53c71cf4ad87abe05611622dbe51758f202354ccdf20`  
		Last Modified: Wed, 22 Apr 2026 02:11:50 GMT  
		Size: 1.2 MB (1222850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fb7898d62d3b5cc45226935beb6ef98f3b90ac1aa7a351b722965f433d5b91`  
		Last Modified: Wed, 22 Apr 2026 02:11:51 GMT  
		Size: 8.1 MB (8120734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa45b451fd41ac0fc29f0036aee5af47adbf50d0dbeba4bb9747a561a4ba57c`  
		Last Modified: Wed, 22 Apr 2026 02:11:51 GMT  
		Size: 1.1 MB (1097057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2886a6b125298c89789fc412cbff612f6352a3a79466fbc3688d9700b0204c`  
		Last Modified: Wed, 22 Apr 2026 02:11:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e4cbd2baa5dc3fe9ddda001bbb8dc69add1a85f600ca7ef0a8682c1462e32`  
		Last Modified: Wed, 22 Apr 2026 02:11:51 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de11a4441c538fb179ed422711e9e710a0de3244c517af26b7c19b93730b16c7`  
		Last Modified: Wed, 22 Apr 2026 02:23:51 GMT  
		Size: 122.5 MB (122523339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12476c31805761a556b1f56d938fbeb76e20319ebcba2e012c6d0e5739cb9e6`  
		Last Modified: Wed, 22 Apr 2026 02:23:49 GMT  
		Size: 10.0 KB (9972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449f68488cd1b7f3806f7c8ab6a5558852e22f37e78d1ff07d268562bfd9d2b7`  
		Last Modified: Wed, 22 Apr 2026 02:23:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f38078c4cd0d2bd6546cac12f68c575e525eba5c62874ed694a121d3a2e67a`  
		Last Modified: Wed, 22 Apr 2026 02:23:48 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f148418643f9bc7baac2699fd2669e8a3e9c2db96ede3c00417f7b65ed1f987`  
		Last Modified: Wed, 22 Apr 2026 02:23:50 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfe39bcb4396553adc5053ccaf16cf4c9ee3eafe99b4ab5c1784321ca24d516`  
		Last Modified: Wed, 22 Apr 2026 02:23:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d9ffcf9e4af8590c4374bab7f4fdd801da65a840689e582f5310fadd15f8b74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2608137b780bccb66fbc2ca6b4a86780ab844c82d57c0e41eac9f5e573d4de71`

```dockerfile
```

-	Layers:
	-	`sha256:2c35f870afa7fc11dbf5ff39dacf483607836fac4065a336a6869348f2dd0e6f`  
		Last Modified: Wed, 22 Apr 2026 02:23:49 GMT  
		Size: 5.9 MB (5922272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51cc0f8039f818034881cdaaee47a9d05cba9d13e9c727c9b62654f57bd2d3d7`  
		Last Modified: Wed, 22 Apr 2026 02:23:49 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
