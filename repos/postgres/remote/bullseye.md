## `postgres:bullseye`

```console
$ docker pull postgres@sha256:4db14a820126a0759e9b2372180dcf3e6d3762de0ad6e33d000afa091f6b5627
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `postgres:bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:f3ec4e6b0b0bb146662726cc17d68ca8ff9a1abfb52c7b47044b7821ea4efe18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150587533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d61dd48ca55a32ec528f7b4196f6d8ccdea2f59a79038eb2e55f3e7b10eedf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PG_MAJOR=17
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PG_VERSION=17.4-1.pgdg110+2
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:59:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:59:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:59:30 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:59:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:59:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c38097bd773fe746e79d2eb3a9ad6c6d4a0ae5afcca2176d0a248c4c321f2b`  
		Last Modified: Sat, 22 Feb 2025 00:28:15 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e43af330563e2b75222883bac09c9965ad5b32492a0400dcb526634c5752c5b`  
		Last Modified: Sat, 22 Feb 2025 00:28:15 GMT  
		Size: 4.3 MB (4308130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509a14c13215a9e05f50596cc218b796efd1fc542442e79edc7658031e494a5b`  
		Last Modified: Sat, 22 Feb 2025 00:28:15 GMT  
		Size: 1.5 MB (1472180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28186ef5c8e738fc7d8bc51a66b198bd9b4e683bf82d0e5b62ae757653c3549b`  
		Last Modified: Sat, 22 Feb 2025 00:28:15 GMT  
		Size: 8.0 MB (8044384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09016c0573782bc6e41e373db26563feaf0febf153870e44e75865332dc0fe13`  
		Last Modified: Sat, 22 Feb 2025 00:28:16 GMT  
		Size: 1.0 MB (1038342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2effff9e06d5b542b3efb2cd572d14911aa281d944d89ae9fbb3755638322059`  
		Last Modified: Sat, 22 Feb 2025 00:28:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009a9c0e252f1f92ee0cdaefbb9469f8856debb2bf5a79e960d87a8b00af306c`  
		Last Modified: Sat, 22 Feb 2025 00:28:16 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc68a022fadfce49bc9883f311720edb0f48e442916e2dfeb952359fc1010ce1`  
		Last Modified: Sat, 22 Feb 2025 00:28:17 GMT  
		Size: 105.5 MB (105450838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcb7dad6735d1deb3fc241ac4c73c290059ad8dd1e384d376d93a4d436e3fd9`  
		Last Modified: Sat, 22 Feb 2025 00:28:16 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc83ee494fcecbebc12dad05c970404a3d57199f31e0e4c111436ec5d45db3`  
		Last Modified: Sat, 22 Feb 2025 00:28:16 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e49c64e16fb82de811a64c1765065509109333c126e705a1add8b264ac3168`  
		Last Modified: Sat, 22 Feb 2025 00:28:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e7a38190baac007ac9affaa99363c373421dab944f095bea427f8a4939a4f8`  
		Last Modified: Sat, 22 Feb 2025 00:28:17 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c425c604dda77bc6e8d30802f679f65074d2c18a7239639e0cc8d427fc1c4fbb`  
		Last Modified: Sat, 22 Feb 2025 00:28:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d139fc830d90d19161660255bd3f83b0da904f08566d8bbe39be3097d6afacbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6119064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb248b15d36b574aeff9ac53da9a89da2ed4da3f1a08553c96ef6cec4ffc4ca`

```dockerfile
```

-	Layers:
	-	`sha256:2dac74cd76bbb728399358167f3dfa5f46a62a33575633a3175949d5a473e39d`  
		Last Modified: Sat, 22 Feb 2025 00:28:15 GMT  
		Size: 6.1 MB (6065272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbbffd60bb105e96b5ce0306685abc87cc7117ea53dce54f312338804b27744a`  
		Last Modified: Sat, 22 Feb 2025 00:28:15 GMT  
		Size: 53.8 KB (53792 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:fd0feb96f47f51a1c63ba600dab8e1029f960fcd93571d004cc991916f37481a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138762910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d486d265e16346e0ddddc7173cbc5d0b76c158582a9af06587be3078902664e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PG_MAJOR=17
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PG_VERSION=17.4-1.pgdg110+2
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:59:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:59:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:59:30 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:59:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:59:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 01:38:07 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58757938f9c4aa50dbc78e022bbdaa24d21099a039910f446209a779868b80e`  
		Last Modified: Tue, 04 Feb 2025 08:22:35 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62775880bddc861108aa9f905791f6a3771e3653ba8b7d4d10bcd4ba90c29a2`  
		Last Modified: Tue, 04 Feb 2025 08:22:35 GMT  
		Size: 3.6 MB (3601780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0f4c44e421a4e93937a077a296f3ebc4f1ef3d241a191f9f0d0aa60140db88`  
		Last Modified: Tue, 04 Feb 2025 08:22:35 GMT  
		Size: 1.4 MB (1439324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165c94191e8ff6def5554f08ab11e45e520d6c978676371a7a3f49e3588e0adc`  
		Last Modified: Tue, 04 Feb 2025 08:22:36 GMT  
		Size: 8.0 MB (8044548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca6fd9675bb8eb2bb071085178e577d32b1efa16ad993abeaeacfeec533a93`  
		Last Modified: Tue, 04 Feb 2025 08:22:36 GMT  
		Size: 908.7 KB (908666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d52c9086f5bf4998da3823aa55355ab2ef7a22afbafda64d9ec7b91c05273`  
		Last Modified: Tue, 04 Feb 2025 08:22:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5e6cfc1e56108a8465fafbd38c207a134683e6e9310e0edfe9f34bf75df401`  
		Last Modified: Tue, 04 Feb 2025 08:22:36 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6e4cfe8246aecd61b4b56d18cbe18a47cd1297f341a7a130f7d98ed6438c16`  
		Last Modified: Sat, 22 Feb 2025 00:59:51 GMT  
		Size: 99.2 MB (99213641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c800b7bae9323c68d29f12e3aeac3c3d677633f92064f48e3d8305164059c385`  
		Last Modified: Sat, 22 Feb 2025 00:59:48 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54de2ae7744dbeec21f94a6ef5d55e0c9f0c21fe75e64e7545788b2292fcff4c`  
		Last Modified: Sat, 22 Feb 2025 00:59:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e83ac5f9d93dbede6b28e885cde1e7e84483b637c119d4494f58ae77ce9c52f`  
		Last Modified: Sat, 22 Feb 2025 00:59:48 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fe532639a7be98f8faee975a2b7eba7e21b2c262c7a7269fe9cd35f3fb9385`  
		Last Modified: Sat, 22 Feb 2025 00:59:49 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c57b54c90dbd2ff67668e9434e273ca4283844789c795a04e1d4a47b59cbd99`  
		Last Modified: Sat, 22 Feb 2025 00:59:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:db59e598acbf9d45a8e0665ecda3db1aadb1065a32a6eac82af88921879988dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6136454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae77d83494d5d029d2bcdce69abeccbcf4bab1cd5605e27032f0addbf94cb0ff`

```dockerfile
```

-	Layers:
	-	`sha256:d23239d5d289851cd1f5fd015022a4a6c6fa4e8aef9ec0e75c83a3b1eb837600`  
		Last Modified: Sat, 22 Feb 2025 00:59:49 GMT  
		Size: 6.1 MB (6082465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e0e6d081e416108f82a79e9041291aec483c196d0e0336e782f5b561ac2e7ef`  
		Last Modified: Sat, 22 Feb 2025 00:59:48 GMT  
		Size: 54.0 KB (53989 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:138b0a569af053160c5cbfc80c0a15003ded33f053f0931bfdf9412132e13d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147587109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91787c1d4d55944e38dc52d72fd6eaa5354966a281ee6b4b9f03953fd6709cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PG_MAJOR=17
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PG_VERSION=17.4-1.pgdg110+2
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:59:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:59:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:59:30 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:59:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:59:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851fb9604468f4d3d1f2d0f531d013bfc5d6b95d99e8a7f640ca42325df3ca7`  
		Last Modified: Wed, 05 Feb 2025 00:53:52 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb22dd44be99186db58182b681f83eae665de75553f6b64937c426586a26883`  
		Last Modified: Wed, 05 Feb 2025 00:53:52 GMT  
		Size: 4.3 MB (4312866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586dc470881d6f1e9635736743d9217602147a7fb0f59e762c76b6e021d8d233`  
		Last Modified: Wed, 05 Feb 2025 00:53:52 GMT  
		Size: 1.4 MB (1404143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c26d7f7fc835a31f3a2df64bad52775e6c8589d5877ac1a6b42c6389dcb31f`  
		Last Modified: Wed, 05 Feb 2025 00:53:52 GMT  
		Size: 8.0 MB (8044431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ac90b2904f37b8728a970638c180d074e41e20b7888dd23f5a9c93f83cf29`  
		Last Modified: Wed, 05 Feb 2025 00:53:53 GMT  
		Size: 1.0 MB (1026615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a9c2f7e28227ab51a02af4e0fbb24857d3fc9df77dd25bc975eb7dd110fbd8`  
		Last Modified: Wed, 05 Feb 2025 00:53:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b6b9c08bb7c8a6bc35d1728a35f2d4e1dfeaa1ec4183abc2d6e2c5928eb684`  
		Last Modified: Wed, 05 Feb 2025 00:53:53 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb5fb4a98800a8bfc32156cece073ab3a3755b86b80987240c47c444462fee3`  
		Last Modified: Sat, 22 Feb 2025 00:36:02 GMT  
		Size: 104.0 MB (104033176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f794d377dec744a781f6b71941b4012ce015943ff723d34ad2df243e835f12`  
		Last Modified: Sat, 22 Feb 2025 00:35:59 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36eb360b4d1aa6f139902348f2ef3f5351f2ebe27c3bf992c8a9a846daa8de8`  
		Last Modified: Sat, 22 Feb 2025 00:35:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e48e246b158d444ca62ce67bdba2c13c309cb356ab44a836947f308f3e61ab9`  
		Last Modified: Sat, 22 Feb 2025 00:35:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9b291180c555445dc8afd428b6e0bdb0ec0bf821dbb4896d2becee7a952260`  
		Last Modified: Sat, 22 Feb 2025 00:36:00 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e63e283570d6aaf2010b77e793028f86ab1fd26f414632b961af44bc46746`  
		Last Modified: Sat, 22 Feb 2025 00:36:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:3f43a1d0d43ed80d76e98fbbadd60dd91979f140761456e515458f73e19772c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6125622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c49c304e0330fd8f0e9378118858930ca62b196665c83ea0fc05ad16b740d1`

```dockerfile
```

-	Layers:
	-	`sha256:aff8e7f5ce9eb9cf8dc4b82ef5fac89c69a03ae21987f4eda66b29ae10f2ed74`  
		Last Modified: Sat, 22 Feb 2025 00:35:59 GMT  
		Size: 6.1 MB (6071572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a649b60f84ee25db8407b658e8fb705b1408549160e86da81bfac134b76df1cc`  
		Last Modified: Sat, 22 Feb 2025 00:35:59 GMT  
		Size: 54.0 KB (54050 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bullseye` - linux; 386

```console
$ docker pull postgres@sha256:497b4933279c1deb5ac394727d471a6439f4e3cc165bb431e075e9326c5c7655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158814315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1572451ed1db5a0839ea0383c7fb2fb9649a31644e24778fd2ed9f19d24e1f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PG_MAJOR=17
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PG_VERSION=17.4-1.pgdg110+2
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:59:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:59:30 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:59:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:59:30 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:59:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:59:30 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02d6b47c2536a29d40deb874d8c9f8323dc767af4a8934f7df1e1044b8fd75a`  
		Last Modified: Sat, 22 Feb 2025 00:41:53 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6deb70a3a6e65d1a7d2c19002ebc32a5f6ccb599587caa338af3e7ecfa4081`  
		Last Modified: Sat, 22 Feb 2025 00:41:54 GMT  
		Size: 4.7 MB (4719712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbbcf849292fa713091d5390a99237c5b2d2c0f4e6d6b57ba82bf04500b7d40`  
		Last Modified: Sat, 22 Feb 2025 00:41:53 GMT  
		Size: 1.4 MB (1447778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837e9e2fdf5331c44e1b2e381a784e99060e4dddb807485fedb915a1e9c7d813`  
		Last Modified: Sat, 22 Feb 2025 00:41:54 GMT  
		Size: 8.0 MB (8044440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6336cddeb03affe2bcbc1371bb06e41532112bcb3322203d1dc551b7199440e9`  
		Last Modified: Sat, 22 Feb 2025 00:41:55 GMT  
		Size: 1.0 MB (1028967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8bd63516e7e0b6f4cf870be57b791482b508336cd31c2dd6382e062bd50c55`  
		Last Modified: Sat, 22 Feb 2025 00:28:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f7b07d824dfb44e4ffa28350b0e648d6bc3e59746e2782514684c59d37c2d8`  
		Last Modified: Sat, 22 Feb 2025 00:41:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80509b55416372b36e49a06a92971b7732c21a55f36f337c01c6ad0324a654df`  
		Last Modified: Sat, 22 Feb 2025 00:42:01 GMT  
		Size: 112.4 MB (112373477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4562af7678f68a80c2baaafcdab4e827a384720e9f2860b88ebd5287e6bb4d86`  
		Last Modified: Sat, 22 Feb 2025 00:41:56 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074fe39ed05461d3cc93345a7afe4f8c48520204644acb04bd438d32e4cc87d3`  
		Last Modified: Sat, 22 Feb 2025 00:41:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ea5e99634062e6ddc83eb7b7d155edbbd3dcab786785b711a0eb8fb9461714`  
		Last Modified: Sat, 22 Feb 2025 00:41:57 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857b85caae2d7df2164c0591f8ec4e3604ed10960b2e009af1d0721074117202`  
		Last Modified: Sat, 22 Feb 2025 00:41:58 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bf947a93f12ddf061abf9845dca10ca9e883758976398b4738de6895d0c350`  
		Last Modified: Sat, 22 Feb 2025 00:41:58 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5f3a29871f6fcf3c7f4c1e3b59768fc63b9847498047e91cf81e585c93423c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6133971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a87236dcc04feb73a751a93e7d3182b4c4ca986e131ea09d659bf8cb13daf8`

```dockerfile
```

-	Layers:
	-	`sha256:0b65757d65a60ae646d927d8540a47d2c1f2c806d3f26ecdf0f22ac82ddd5253`  
		Last Modified: Sat, 22 Feb 2025 00:41:54 GMT  
		Size: 6.1 MB (6080227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fd78370a6f6e4977fca7519a2434a76bc63b1e3cd970393167c53b92c004c17`  
		Last Modified: Sat, 22 Feb 2025 00:41:53 GMT  
		Size: 53.7 KB (53744 bytes)  
		MIME: application/vnd.in-toto+json
