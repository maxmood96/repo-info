## `postgres:13-bullseye`

```console
$ docker pull postgres@sha256:ae9bc7d70ad055c77d19332b623d8699bf01be827963ad4c1f639b3d8d81974f
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

### `postgres:13-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:57497b6701307cc29573e3166855eaabea57bb558d82bb9ea6d573c2e1de499c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144787640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b477786865fa1e7f733d3249c1cd92148daf2000e5b03f3d3979ae10c7f6ae2e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_MAJOR=13
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_VERSION=13.20-1.pgdg110+1
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:02:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:02:25 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:02:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fd27f525cb12d3781fac05b47185c3e89bf83f439606cf60b8b3a5834e96bd`  
		Last Modified: Sat, 22 Feb 2025 00:28:46 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d84c43b3e09a0bc2079b43b3f36e4e43bc42ba2c2f706a654f1f649f5e77a84`  
		Last Modified: Sat, 22 Feb 2025 00:28:46 GMT  
		Size: 4.3 MB (4308117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a1a00b5cec5b35e1a90a79d435ff653c6d9fd1899c3cb0a4a98432161d88d`  
		Last Modified: Sat, 22 Feb 2025 00:28:46 GMT  
		Size: 1.5 MB (1472189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d20ab563d5baee5fbeac530f0d822c6dce4b77630a0bcc84551aedd7c8d2263`  
		Last Modified: Sat, 22 Feb 2025 00:28:46 GMT  
		Size: 8.0 MB (8044404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9badb4af5180357909c22854e6e49b8c0db2ddb59f08b0c1d4ead1aafacc7142`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 1.0 MB (1038358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fc4dba81e1a6fe1ede3b5729c79dbde535562ee38025db1a7d5de686942cfc`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e393c16164ef925e66809416221fca32bcf932bdcf35a650a06dde58a71fe3eb`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c549c2afd895733502ca7a01753022b2194b4346978b71163626448a6a0697b9`  
		Last Modified: Sat, 22 Feb 2025 00:28:49 GMT  
		Size: 99.7 MB (99651800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106d6304645328dd6a16e35edb1c33d6d535aa9925b37013b9c5414bd3b8467c`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454313b1bd7fe7e1b0a245fd28d8b1f6bfc17e91635434c3807515abfc7ec96c`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06f3759962414e3d8d0d36db7e36577747466493b186d1c23ad980799b7b22b`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d921fd0698f4b3babef2a306979062b8b072c1198ceb2cb983fb6dfa53f1160d`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60143ab5b453a8fabd18e01b7c7472e8ced24aad9a4cca420162cca60e657aae`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:fec0bd0cc4bf0508aae856d30073278fb66dd3fe5218fcef0f2ffae444dcfd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5945999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84127a862d6714f06f2aa91b1afb6cbe9361886d19119e2d5193c82a6034fef4`

```dockerfile
```

-	Layers:
	-	`sha256:ce43d80eecd1793090b0751d5d1868480f6090c4eb9a1190441f3668901a5b7d`  
		Last Modified: Sat, 22 Feb 2025 00:28:46 GMT  
		Size: 5.9 MB (5892127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e35b75b701d9c537773191360bd3d4e8a4d4401da612ff4f4122b5eae680275`  
		Last Modified: Sat, 22 Feb 2025 00:28:46 GMT  
		Size: 53.9 KB (53872 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ae6efce080ec27b99da7cd76245c748ed74a32e405164f2ee49a7c6c7943c150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132976131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ec0c7574175ba121b1100ecd0298a2f1e66c720f11bc0b5d739c1ff768cd6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_MAJOR=13
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_VERSION=13.20-1.pgdg110+1
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:02:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:02:25 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:02:25 GMT
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
	-	`sha256:6cab28c2046d38667d110f84d91bb1a7bb9e1ff52c00008a7f869c427cccbcb9`  
		Last Modified: Sat, 22 Feb 2025 04:22:18 GMT  
		Size: 93.4 MB (93427750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b373e5ee74472cca23b101ef42810e54401db16465cc4b43e1926135e360aab`  
		Last Modified: Sat, 22 Feb 2025 04:22:15 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d81d2c5619fd6e01676299d81acb1a4bd791f0fa531c56d9ebbaf3968648f93`  
		Last Modified: Sat, 22 Feb 2025 04:22:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a48c7a08f03311366027919c3d677a0c3bd0662c9a0e1842a9155728ccd633`  
		Last Modified: Sat, 22 Feb 2025 04:22:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c5f54757dc1c61b3c0c4334a9ccfde0d4f7ce28356dee68bd4c5f842841df2`  
		Last Modified: Sat, 22 Feb 2025 04:22:16 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0b038f0939095aebdca8581829596e323e8d09c0ffcc7aae914424776387ac`  
		Last Modified: Sat, 22 Feb 2025 04:22:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b94caa9f0b183fd48390d817ecc8ed4efb82e8c7ea87898f36d4a703bf5cba23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5956858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f517a2072b87868f33bcfca277c8d5d2c543497c0e3d1d24d233cb4bd520da40`

```dockerfile
```

-	Layers:
	-	`sha256:c086eeac459d3e10f520a5a7f0ab75e035510034018dd121c7b7441f174114f9`  
		Last Modified: Sat, 22 Feb 2025 04:22:15 GMT  
		Size: 5.9 MB (5902792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c8372e25d32087c4ebb8b7313efb96b11e9294642b8369766a460569c3fb247`  
		Last Modified: Sat, 22 Feb 2025 04:22:15 GMT  
		Size: 54.1 KB (54066 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:4d70b02ac2e16dcde327e7f2b0fc72a15b8d7ef98a90df440d401bf6f28ba8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141807056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78838480cc60e8252412a77e0509fe865fa62fe63612c4aa33f605f037deec25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_MAJOR=13
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_VERSION=13.20-1.pgdg110+1
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:02:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:02:25 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:02:25 GMT
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
	-	`sha256:fe75b815c05268f77e17d6f464ee4c1aac132fc330ddadf290c38d750ed445de`  
		Last Modified: Sat, 22 Feb 2025 01:55:59 GMT  
		Size: 98.3 MB (98253999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc78f17777190b01b3e97f33196dafbbdb3704ff5bba397f2d39dfd7c4abe531`  
		Last Modified: Sat, 22 Feb 2025 01:55:55 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bbc1452e28f9ad58545fe317810028cb2621d9d0ceef24e4f57e0b9b61d7b5`  
		Last Modified: Sat, 22 Feb 2025 01:55:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5324ea3fea1df40d34b7ba2a284335f0fa70ac1c43e02992cb611ef3578196c`  
		Last Modified: Sat, 22 Feb 2025 01:55:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ac6658346d765368376275314b1f38df5068d8912c4dd9f3fd73d4f47c42f7`  
		Last Modified: Sat, 22 Feb 2025 01:55:56 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbebafcaf3a8ed08ba5a8c6a82fe7551e542d5475ea34e450a02cf4f3e037622`  
		Last Modified: Sat, 22 Feb 2025 01:55:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:3f097867678e0196d5f2b39c9fe09deb68d151b799ce7a96ccaac67baeec893c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5952532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331d70047dea3035961b52d034cef358c801edf1e2c92075a6f7d4f65f5bf66b`

```dockerfile
```

-	Layers:
	-	`sha256:8693a07d519199da184470a3d35ab484c92f7db045ef4f3f892d5aead2d2bf4b`  
		Last Modified: Sat, 22 Feb 2025 01:55:56 GMT  
		Size: 5.9 MB (5898415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53b0cc4cc4f7d1187e74d324c87938ba9f26341b109e417c5e6cbbd08e6c3ee`  
		Last Modified: Sat, 22 Feb 2025 01:55:55 GMT  
		Size: 54.1 KB (54117 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:9b7ad27674e2465cbab6c9b74ba5fe91d36183e93c7d2b62ce12959974374da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152823625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15517861793904134b69fbaa963e0167861b46d5c97416446a0f6f10084ad615`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_MAJOR=13
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PG_VERSION=13.20-1.pgdg110+1
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:02:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:02:25 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:02:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:02:25 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:02:25 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:02:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099ea0a2c0a6009a1783fe23f987af28a0cb0a4911b154eed7c55d5f94e93569`  
		Last Modified: Sat, 22 Feb 2025 00:39:46 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaab2a268a52896f75e4c91c56ce7b430284e80a266fe4cbfdbb9249b7e6f20`  
		Last Modified: Sat, 22 Feb 2025 00:39:46 GMT  
		Size: 4.7 MB (4719662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb57c5021fdcea76c2ddaca9869b55048fffa639f4981a7d3e8549f087c10af`  
		Last Modified: Sat, 22 Feb 2025 00:39:46 GMT  
		Size: 1.4 MB (1447789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2475d5d31bfac4cc338c28de4c70405c79cb36c97c5fc8c1d31db536b2062448`  
		Last Modified: Sat, 22 Feb 2025 00:39:46 GMT  
		Size: 8.0 MB (8044354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91aaa93bdba78da1eca5c77156e87a70ef1d8226b07adf221ba16a58f98024a`  
		Last Modified: Sat, 22 Feb 2025 00:39:47 GMT  
		Size: 1.0 MB (1028959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9ebbcbe73fb84f9430cd3fd488a76946f2fefd15a01abf4221d2db6b99b1d2`  
		Last Modified: Sat, 22 Feb 2025 00:39:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162a80d83fe1835be332d35ab8c231be403b11232e32d7f887fffcd25dc4ac5a`  
		Last Modified: Sat, 22 Feb 2025 00:39:47 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7a649b01c648d5bdb4ba87c5ed40f836e6f74e3a9b88c16a8e4a74165394ef`  
		Last Modified: Sat, 22 Feb 2025 00:39:50 GMT  
		Size: 106.4 MB (106383801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e10977853c06bd7abd5e64e7f6b3646f2494adc140061c08533f7000dd5d95`  
		Last Modified: Sat, 22 Feb 2025 00:39:48 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2fa156652b52ce01cc005e9341f4d20495c47b540005920dca282412714006`  
		Last Modified: Sat, 22 Feb 2025 00:39:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce1c4f42cffcbe0b24080ab7b9f29ff4e296ee8cb6b23577f99b4a6da52d7a0`  
		Last Modified: Sat, 22 Feb 2025 00:39:48 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5569fc6ca8d402a6c2115c8a1fa6940ba5fa0bbb717c039af65e6a3ecb5e55b`  
		Last Modified: Sat, 22 Feb 2025 00:39:48 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61ac7fea3483eebbee70419f96f07fa6712b09a254e98dd5d0a9e9e0e32f464`  
		Last Modified: Sat, 22 Feb 2025 00:39:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:7415d76845782f38d1e6704274facd0e98f413abaaef8a10c8e3445355118615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5954401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a8ce8d315c991cce76c04e880cb563c213754905a6b400a17a009f2ef89165`

```dockerfile
```

-	Layers:
	-	`sha256:750945b0133496fd8f7f4f5b736c3bbbca417d34cb4694e07fba7dddf50784b3`  
		Last Modified: Sat, 22 Feb 2025 00:39:46 GMT  
		Size: 5.9 MB (5900567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69a1a5d46b28d3d5d93b26a011abbcfd38e2322130d7e4d3908383252d9f3bcd`  
		Last Modified: Sat, 22 Feb 2025 00:39:46 GMT  
		Size: 53.8 KB (53834 bytes)  
		MIME: application/vnd.in-toto+json
