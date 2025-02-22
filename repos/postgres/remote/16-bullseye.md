## `postgres:16-bullseye`

```console
$ docker pull postgres@sha256:ef15f22d1ce0b2ee3980cace1c293f355e2a92df6162edc643c8ff692cf7511b
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

### `postgres:16-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:c4c745b003c92a36a7155e99e21b4d6fd772f36a9c74fabc38f6e69c4550b96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149392338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09469c3aa6ebdfaefdd52dea92760c86b6080ee4eadefa877a25be5ef0c24fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PG_MAJOR=16
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:44:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:44:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:44:40 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:44:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:44:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f9f48b95722fe93c5603f484e387ebed38828f1516f8e19163c496611fe5b6`  
		Last Modified: Sat, 22 Feb 2025 00:28:46 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd30734cc2e47e4e6a6f5a7cf18348fd4ddbf0d8f47b98ab54f14b9b541db696`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 4.3 MB (4308133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d23e8a734d5a70530d23cbbd68b55099194342605f5c52f4abb4c4897498cb9`  
		Last Modified: Sat, 22 Feb 2025 00:28:46 GMT  
		Size: 1.5 MB (1472191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51efd366fc28ea87ad5a3c7420f954329ca7994017440ad0a17cf7f964ce1401`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 8.0 MB (8044532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07073034ebcbb73a692d0e985753211fd7400d69621a6d723fd7a859da417f81`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 1.0 MB (1038364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07f92f5827eab6e5499a748b03c6867399933c8a83ae71f9f3646497727e049`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcd98bafcebab03b2e1520d5a238059043ee4985105b86c3646f6857a9dffe7`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d714a434381c7e064abbb95a5bb0f07cceb84544bf1b31da537eec731d3c69`  
		Last Modified: Sat, 22 Feb 2025 00:28:50 GMT  
		Size: 104.3 MB (104255777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e8f6bdaa7ad5474146922dd81bd3dab1f072625fa907b2a97219b85295901f`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 9.9 KB (9913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca5a0c056355c2f77028354ca0ed9b4108035f45f4bfb58ce0585ad51fa2b34`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a561a2b0a724584dbed036318364cc5c315900f3942b652fb935c5e54f4184`  
		Last Modified: Sat, 22 Feb 2025 00:28:49 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0372bca58261ae63c89be55970c3ae47d7092b7d9e57b929622c250cc9faa1ae`  
		Last Modified: Sat, 22 Feb 2025 00:28:49 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60143ab5b453a8fabd18e01b7c7472e8ced24aad9a4cca420162cca60e657aae`  
		Last Modified: Sat, 22 Feb 2025 00:28:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:923d976de0ccbc596615778b1e9030f7aa0b4afe8009c1df77d9d072182a43af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00507254a821768f86780a74281b8230dc2f21eb2f9059c8ea349d39c6a2aab2`

```dockerfile
```

-	Layers:
	-	`sha256:d449f6999078386584435b8c48527bd72f9fa583e37b85beb27339b701679f62`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 6.0 MB (6048778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c96661dc51757f29e5585e2804778a4230dfd8f957c669753c046462a1a5e85`  
		Last Modified: Sat, 22 Feb 2025 00:28:47 GMT  
		Size: 53.5 KB (53482 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:764b78b0869cc49ff9378d133f83aa1d81b02c82a5f14933a75513fe62afac5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137611646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875c7baee177963dcd26e79ead69b70d156929e14e441358699253246c5e4f77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PG_MAJOR=16
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:44:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:44:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:44:40 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:44:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:44:40 GMT
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
	-	`sha256:9013fadc14ee8fbc0912953e5eb01186371e09b0b603d63df96978f98999a265`  
		Last Modified: Sat, 22 Feb 2025 01:44:17 GMT  
		Size: 98.1 MB (98062694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4484c0af3c784d80a6191a2b4c705d631b3f9867943c7ca9796aab89ec4d432`  
		Last Modified: Sat, 22 Feb 2025 01:44:14 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e627b4048ca301807c6391aa580216053d6ff8d74175757c62473529c249994`  
		Last Modified: Sat, 22 Feb 2025 01:44:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f762a270c4276d5d01b01d0baa2ea168198b1ac5924b7888e3a0aa1a05e715`  
		Last Modified: Sat, 22 Feb 2025 01:44:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294ceab0022aace6ae1015384629d7a57d7ffd19a275c528316dcdd9667c907a`  
		Last Modified: Sat, 22 Feb 2025 01:44:15 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7210ebbb985b9aa88f80a881882128bd7ec84bbf83daf21786142680991068`  
		Last Modified: Sat, 22 Feb 2025 01:44:15 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:138f4ef971ce9de843f9cf63e5ea077c472535585083344cc219d30275a268ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6117905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef9c9a542140ab6c6182cb80f7bf9cd12a86724a532645fdfe6eb58e953ec4d`

```dockerfile
```

-	Layers:
	-	`sha256:127051e9644961d7c93cde17703df3a7bf81dbcf3552e15edc022b25726e211e`  
		Last Modified: Sat, 22 Feb 2025 01:44:15 GMT  
		Size: 6.1 MB (6064235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ffb907522061cbcef924a621f99fe11ed47613788f86bff0bc0d2b85c76a6ea`  
		Last Modified: Sat, 22 Feb 2025 01:44:14 GMT  
		Size: 53.7 KB (53670 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:7996f939c913a6e1d498a579056c5c57cca533637eed395f0e13bb7e176d316f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146399190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4163dc5418e665e55d405d12cb67eac50db0a367dbcf89096a3359e3b7ca660d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PG_MAJOR=16
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:44:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:44:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:44:40 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:44:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:44:40 GMT
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
	-	`sha256:ca9097e8674117d1595e7f50c9bb84092962b69f31d087c3c0ef38289a081c2e`  
		Last Modified: Sat, 22 Feb 2025 00:45:19 GMT  
		Size: 102.8 MB (102845570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6ece8df9300f2ecc5394444e6f2a842af814cd0b2c4f8628e752565e276ef9`  
		Last Modified: Sat, 22 Feb 2025 00:45:16 GMT  
		Size: 9.9 KB (9918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9567ee696b5217e3812da29a9546d77ac470a3081f4e5fc59be048ae216c1f3d`  
		Last Modified: Sat, 22 Feb 2025 00:45:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01b782f936ed4a00fa7ab82ec9ac4db05d8c302d9dfc55b761c153d03e54a32`  
		Last Modified: Sat, 22 Feb 2025 00:45:16 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2972fc350ad090fa03102e45744674a98a69f527cfe109a998649c2757124416`  
		Last Modified: Sat, 22 Feb 2025 00:45:17 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d047a6605dc8f8994b4fed758c64aee2183bb48b0eacf9997d0e43847fd4978`  
		Last Modified: Sat, 22 Feb 2025 00:45:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:9edac1147f4fbaa1a2e5a62b904cd9bc1d9797f304fbbfafdea56ac855160ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6108793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dac9d907cf177937d3240be0de1e9bf4363f90d08065ba936509a860635ec32`

```dockerfile
```

-	Layers:
	-	`sha256:894df7f73ad32c95bbba3646702461817afd6522ff2e80d4bb4dcbc3c690cf86`  
		Last Modified: Sat, 22 Feb 2025 00:45:17 GMT  
		Size: 6.1 MB (6055066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21dca9cc8da8d4b93d8ba35ffbb8a6d3b0a41e6cb49c134775153e7b3f37120`  
		Last Modified: Sat, 22 Feb 2025 00:45:16 GMT  
		Size: 53.7 KB (53727 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:e6e1ceb38d23ae86215fb5ee2d450293e3ed3df9bff0e0dc9576649ca2a88756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157593237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87268afd7b7ec1d9955abbd6aa046e08ce944dbc37fac31527da2cb8923e47d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV GOSU_VERSION=1.17
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV LANG=en_US.utf8
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PG_MAJOR=16
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PG_VERSION=16.8-1.pgdg110+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 20 Feb 2025 19:44:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 20 Feb 2025 19:44:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 20 Feb 2025 19:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Feb 2025 19:44:40 GMT
STOPSIGNAL SIGINT
# Thu, 20 Feb 2025 19:44:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 20 Feb 2025 19:44:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acc2ca181bf2abad5f383ff408ec07947a94cf96ee2db7d6fc8900767d809e5`  
		Last Modified: Sat, 22 Feb 2025 00:40:20 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4f1a06a95812afed9e4b3b358748a86582d5a8c468b351483a70cdb404dfc1`  
		Last Modified: Sat, 22 Feb 2025 00:40:45 GMT  
		Size: 4.7 MB (4719730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0871ead6afd774552962c026fa1955bf3fac34ff0ba54e908f0bf710aa67f861`  
		Last Modified: Sat, 22 Feb 2025 00:40:45 GMT  
		Size: 1.4 MB (1447790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85ee341232a6a4ee6aa484a73d6daf8b866316256c0a032bbba930723574c73`  
		Last Modified: Sat, 22 Feb 2025 00:40:45 GMT  
		Size: 8.0 MB (8044443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a568b1232dc2f434e34212af22e1724360c77205a720a159e232969b19b57e`  
		Last Modified: Sat, 22 Feb 2025 00:40:45 GMT  
		Size: 1.0 MB (1028923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed28fc097e2fd58335aa4227a391047f85a4284dad789316ea69073b4aafe89`  
		Last Modified: Sat, 22 Feb 2025 00:40:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c25aeddff097b03a67b7c0d5e2281ed23c4e8a747961365950bac4317f5e706`  
		Last Modified: Sat, 22 Feb 2025 00:40:46 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cea9e6b18fc985cef87cbeb1e54f8da9f455c121cd7ce75dcc1d09712133ae1`  
		Last Modified: Sat, 22 Feb 2025 00:40:49 GMT  
		Size: 111.2 MB (111152727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf6d0a02aa96dc72cf173870a29db000c2eebfdc817ad87ca31c50f8df3b06b`  
		Last Modified: Sat, 22 Feb 2025 00:40:46 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b47a756c4531195b41a2c3318da02f8a13af7cd923e15e8fbf7e7ecb36eff4`  
		Last Modified: Sat, 22 Feb 2025 00:40:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da40069ee3872362e1d7e96079c069d016b246de834a57ae2613b37fa957230`  
		Last Modified: Sat, 22 Feb 2025 00:40:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba8dd8b5b9ca1cbe049364d1854cf931f1e4d8b12cca9de548e7ca2425b8439`  
		Last Modified: Sat, 22 Feb 2025 00:40:47 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1cb73b546beebb686fb2086fca75223f9b7db4fe6c6ab8302cdeebdfae6460`  
		Last Modified: Sat, 22 Feb 2025 00:40:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d25a9168cbc4a567c7cd646296cb0f5f6345b4def55fadb0c53d0e5747b1746c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6115448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd6b7b1cadbea5b8071fe7f8709c3c4b96edf7f1f17334c860e6f44021cebad`

```dockerfile
```

-	Layers:
	-	`sha256:0951c367d9c155364e5668c08e588913833767151247d3b07e2b08ac17fd35ff`  
		Last Modified: Sat, 22 Feb 2025 00:40:45 GMT  
		Size: 6.1 MB (6062010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b69972e4922ac05270ec546aa362040899f6f1fadc65657ea9d2c37115cd977`  
		Last Modified: Sat, 22 Feb 2025 00:40:45 GMT  
		Size: 53.4 KB (53438 bytes)  
		MIME: application/vnd.in-toto+json
