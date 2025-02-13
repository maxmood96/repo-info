## `postgres:17-bullseye`

```console
$ docker pull postgres@sha256:5af45ac79f38cb3b0584ff4ff222917edbdde309d187aa69aa91671807e6bc61
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

### `postgres:17-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:0f94929f3cd7830c57363479457b78d8c1d818a52bd362f35c5d9b4e8c3aa1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150371060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b8cd84ae6b5f4d10b493236023f42e071271f45edfdd47115947f42b2ada35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=17
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 04:26:31 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7831297fb715c5299effd85f9496c506ffe69eff7a6fc5088e796cb0f774e68d`  
		Last Modified: Wed, 05 Feb 2025 00:16:25 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d785cd26ead684fb02c2a232f3de6518ed73a986ead7a3a8bf19eb41a882d50`  
		Last Modified: Wed, 05 Feb 2025 00:16:25 GMT  
		Size: 4.3 MB (4308181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd1c3f8dbf979d2aa703053728ce031ca648198be3fa3101e8bc19db7518a9a`  
		Last Modified: Wed, 05 Feb 2025 00:49:19 GMT  
		Size: 1.5 MB (1472235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5519e6f202398633d519df1f5c48d803727ff00dbce7d13f2a9e9e876cf4494a`  
		Last Modified: Wed, 05 Feb 2025 00:15:48 GMT  
		Size: 8.0 MB (8044545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7b3dcfbfab989175023c8f337ed60b969eb7941682c39e6d1f19c21f363cde`  
		Last Modified: Wed, 05 Feb 2025 00:30:48 GMT  
		Size: 1.0 MB (1038351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03aec8d388a4ababcb9ec38dd2bf2f27d5d9348e2c26f24baea2cc146aaf3a`  
		Last Modified: Wed, 05 Feb 2025 00:16:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb92191ceee68868bfced70ea6adf4295b6d3c8c3d4310a4023f1e0180dcc22d`  
		Last Modified: Wed, 05 Feb 2025 00:44:24 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a319ce7bc6bf829b8cd69cc4c064abcf65e5686e53aca7825a6e382b007b3c`  
		Last Modified: Wed, 05 Feb 2025 00:16:33 GMT  
		Size: 105.2 MB (105234094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32baad9676a4b3993952bf0a094e5131996b573e9d1a77c9085e9d03bd817d35`  
		Last Modified: Wed, 05 Feb 2025 00:30:49 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a720502d2669d38b5a6b227cf51a02666d9a041134b5d8728f4bd0575d40c337`  
		Last Modified: Wed, 05 Feb 2025 00:16:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c0ee8ac4adfeebe2a656a09b7038cb02ad6cbdb346fda5faa308f5d4f4dc14`  
		Last Modified: Wed, 05 Feb 2025 00:16:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71baa627037857022264657535b4027e93979a2c71d42185066b9bbac3c88e91`  
		Last Modified: Wed, 05 Feb 2025 00:16:29 GMT  
		Size: 5.4 KB (5412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8cb4cf4c05d08affa7305d6bc693e1584fad71aaf57ca7ccc55b6f44b00573`  
		Last Modified: Wed, 05 Feb 2025 00:49:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2417fd11d109b0f55b158782aae585e6e73c362e515991c3abfc9de135222966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c8f4b49992b51d5132998f774fa8cbc81d0abdb6784e6f030c67d27265e26`

```dockerfile
```

-	Layers:
	-	`sha256:c7b58fd33e300b2861963da088ddcae4559e23a21d63933461b4d31978a289e0`  
		Last Modified: Wed, 05 Feb 2025 19:01:28 GMT  
		Size: 6.0 MB (6033534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d75c1ea76d74f8e079ad649833e6c0cf65b3472e609d1ae6fd13b68989b444`  
		Last Modified: Wed, 05 Feb 2025 08:51:38 GMT  
		Size: 53.8 KB (53793 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b862b4ab68d2ac10a57cd62ee512b9c99781d08443cd3ff63da33f69d9760655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138575545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1258759c0ce48d2a253c8395b75b4d185d064aa51001e70a65b24df4da063522`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=17
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 08:24:31 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58757938f9c4aa50dbc78e022bbdaa24d21099a039910f446209a779868b80e`  
		Last Modified: Tue, 04 Feb 2025 22:00:22 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62775880bddc861108aa9f905791f6a3771e3653ba8b7d4d10bcd4ba90c29a2`  
		Last Modified: Wed, 05 Feb 2025 22:00:31 GMT  
		Size: 3.6 MB (3601780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0f4c44e421a4e93937a077a296f3ebc4f1ef3d241a191f9f0d0aa60140db88`  
		Last Modified: Wed, 05 Feb 2025 08:51:36 GMT  
		Size: 1.4 MB (1439324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165c94191e8ff6def5554f08ab11e45e520d6c978676371a7a3f49e3588e0adc`  
		Last Modified: Wed, 05 Feb 2025 22:00:34 GMT  
		Size: 8.0 MB (8044548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca6fd9675bb8eb2bb071085178e577d32b1efa16ad993abeaeacfeec533a93`  
		Last Modified: Tue, 04 Feb 2025 22:00:25 GMT  
		Size: 908.7 KB (908666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d52c9086f5bf4998da3823aa55355ab2ef7a22afbafda64d9ec7b91c05273`  
		Last Modified: Tue, 04 Feb 2025 22:07:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5e6cfc1e56108a8465fafbd38c207a134683e6e9310e0edfe9f34bf75df401`  
		Last Modified: Tue, 04 Feb 2025 22:07:05 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dbab64d21f1ab0908cf2d7333921656938105ef02070c8cec218a6596347c0`  
		Last Modified: Wed, 05 Feb 2025 19:01:34 GMT  
		Size: 99.0 MB (99026287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4620c9fbe646857d01c83653557ea869fb7a712cfadcefce9fd93ada55d683`  
		Last Modified: Wed, 05 Feb 2025 08:51:37 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74649de4969fdecaca9602209b8663a245c4e9751bb56f8fd694a3d8e3837456`  
		Last Modified: Wed, 05 Feb 2025 08:51:37 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99180ab04be820f50275b0a005a731c76f7051586ebcfd0b5c1beb97d91c71c`  
		Last Modified: Thu, 13 Feb 2025 10:07:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a31573962ebed524bacd7b8835be4e8a0daf6a310065e66ecb1a4317bff2b9a`  
		Last Modified: Wed, 05 Feb 2025 08:51:37 GMT  
		Size: 5.4 KB (5407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941f131edcf9b1e28ff96919091db98d4e111b51fe1f43208f88e28c110b1e4f`  
		Last Modified: Wed, 05 Feb 2025 13:47:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:c1cead33344f9d2dbd8ade3632b75c41d1ebc2a924563883ab3ae95b20f735d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec627defe35f835dd77ce7b04dec4c764a38b1f38057e829bc8b7b9e44bc1b1`

```dockerfile
```

-	Layers:
	-	`sha256:2acb3b94947d6bb9797af0a2cfad6bae2c6c85a3014b2a3fc45c07646fe8842d`  
		Last Modified: Wed, 05 Feb 2025 19:01:36 GMT  
		Size: 6.1 MB (6050727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ed926cf4c82e5aec68c1137ef038ed6b7b5368c18e5abeacca131b274c67514`  
		Last Modified: Wed, 05 Feb 2025 08:29:03 GMT  
		Size: 54.0 KB (53988 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f6b5ef746533ac2cafe0130f869261e06a0fa9bf1c045a1e94d8867b7be1c1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147365895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d62e04513490bcf4afec55177d7f5ffdd4ad02363cf6062cafed2f7c05414c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=17
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 04:27:50 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4851fb9604468f4d3d1f2d0f531d013bfc5d6b95d99e8a7f640ca42325df3ca7`  
		Last Modified: Wed, 05 Feb 2025 03:28:18 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb22dd44be99186db58182b681f83eae665de75553f6b64937c426586a26883`  
		Last Modified: Wed, 05 Feb 2025 03:27:33 GMT  
		Size: 4.3 MB (4312866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586dc470881d6f1e9635736743d9217602147a7fb0f59e762c76b6e021d8d233`  
		Last Modified: Wed, 05 Feb 2025 03:10:25 GMT  
		Size: 1.4 MB (1404143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c26d7f7fc835a31f3a2df64bad52775e6c8589d5877ac1a6b42c6389dcb31f`  
		Last Modified: Wed, 05 Feb 2025 03:10:32 GMT  
		Size: 8.0 MB (8044431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ac90b2904f37b8728a970638c180d074e41e20b7888dd23f5a9c93f83cf29`  
		Last Modified: Wed, 05 Feb 2025 03:16:32 GMT  
		Size: 1.0 MB (1026615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a9c2f7e28227ab51a02af4e0fbb24857d3fc9df77dd25bc975eb7dd110fbd8`  
		Last Modified: Wed, 05 Feb 2025 04:53:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b6b9c08bb7c8a6bc35d1728a35f2d4e1dfeaa1ec4183abc2d6e2c5928eb684`  
		Last Modified: Wed, 05 Feb 2025 03:27:32 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2409234d0a6a486b9ef1986b4e623eb5d49182ec1c110156fbf308f04656ec`  
		Last Modified: Wed, 05 Feb 2025 03:11:43 GMT  
		Size: 103.8 MB (103811964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d763cf30bc5b78ef085fa2bb610ecbb338be986d3ac875de0ca3f12160323b09`  
		Last Modified: Wed, 05 Feb 2025 03:11:40 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72146514992ec39ce625e679253407dbcefd494fcad13dc1645bcdd93106bb16`  
		Last Modified: Wed, 05 Feb 2025 05:15:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994d1b6ef30c8cd3fa975ab80f877be64c4f091af1bf8b5227cbce5c30524838`  
		Last Modified: Wed, 05 Feb 2025 04:53:34 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47559809621b04d6fbefda3d6377b890797f8f7ac887e25e218b239783690835`  
		Last Modified: Wed, 05 Feb 2025 06:48:14 GMT  
		Size: 5.4 KB (5410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01b594a2a76257e1d2c0cd764520dd44a319d733599460ca57daa7e975200da`  
		Last Modified: Wed, 05 Feb 2025 03:11:41 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:5066e28c25fa8aa3e3c1de8c68aaa43e510d9e4797b6a9a1f12e997ffe94c917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6093884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c06c1c240f7cc29d504fce99d90828f20a547ef0b78a22d6ac1cf50cb09262`

```dockerfile
```

-	Layers:
	-	`sha256:210a8c73a1e86a6461eb3d486f279baad9c988771468b5fa5d5d564b7e302a23`  
		Last Modified: Thu, 06 Feb 2025 01:00:38 GMT  
		Size: 6.0 MB (6039834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890824d77c092da01b538b84f0f18670791b9063ed150a6fdb64e7b1f73c2432`  
		Last Modified: Thu, 06 Feb 2025 01:00:39 GMT  
		Size: 54.0 KB (54050 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:6f23647d913e43f52be8a77e65ed18acee1dabc23d6e2d971993a9da2474c9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158601852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e43ecc9afb0210181b01b1c380b208df4fe0bbd60cbb3829d69fb2ccc980eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV GOSU_VERSION=1.17
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV LANG=en_US.utf8
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_MAJOR=17
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PG_VERSION=17.2-1.pgdg110+1
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 04 Feb 2025 00:55:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 04 Feb 2025 00:55:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 04 Feb 2025 00:55:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Feb 2025 00:55:44 GMT
STOPSIGNAL SIGINT
# Tue, 04 Feb 2025 00:55:44 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 04 Feb 2025 00:55:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 05:05:20 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e858b7c1cb9651ee8170266fcfb9b2f966fca8c09dc00ccd40e0633305535070`  
		Last Modified: Wed, 05 Feb 2025 13:48:16 GMT  
		Size: 1.7 KB (1676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1594f215269d8b1f5262dff46746c49bed04d3cd4dd0b60330c3215c762197e`  
		Last Modified: Thu, 13 Feb 2025 10:07:04 GMT  
		Size: 4.7 MB (4719619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afe8e649c674d16519f5a9fc9faf0dc7eefa7cbec0469a4cd3f2f5b3b0cbd26`  
		Last Modified: Wed, 05 Feb 2025 19:01:45 GMT  
		Size: 1.4 MB (1447751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f90bd3a93be82a74ac20ef054537d7224a699018ab368e379c6987b7c14442`  
		Last Modified: Wed, 05 Feb 2025 13:47:53 GMT  
		Size: 8.0 MB (8044346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc2bae1bda925ac68d018e143cbf8b87415ef2d887b450ce13a5061b2c867ca`  
		Last Modified: Wed, 05 Feb 2025 01:01:39 GMT  
		Size: 1.0 MB (1028934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcba95080bc1b811e520a8b20e45b74d9c4ec272c38f1c02bbc6ec3857722cb6`  
		Last Modified: Wed, 05 Feb 2025 13:47:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995d70c6ea0832837585a5d9cdd828f74d302efba3ff82c7cd5c5a78984c4fb1`  
		Last Modified: Wed, 05 Feb 2025 01:01:41 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2b12975a151e0082b46ac6e43e98de1431640991f0b11b570947a6345d2ba5`  
		Last Modified: Wed, 05 Feb 2025 08:51:48 GMT  
		Size: 112.2 MB (112161261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca8828cd0a21eefb2d935ac5179ca142bc4cdc339176811ab1678c00ffcc55`  
		Last Modified: Wed, 05 Feb 2025 08:51:42 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a161a71a4de2b731f9c1776db7ca34f91e46e2c63fe80f632aa571337b2c186c`  
		Last Modified: Wed, 05 Feb 2025 01:01:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049f3a789b47635b84a9c64899c5ac6220d5f41e0d0e4bd2d3455d50f4b078d4`  
		Last Modified: Thu, 13 Feb 2025 10:07:06 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f392059362e8a10eef2ce28b6cdf297170103d5327fe5c3bd108e42ba45bb3d0`  
		Last Modified: Wed, 05 Feb 2025 01:01:51 GMT  
		Size: 5.4 KB (5412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cff316d8573256ab90a361bfc26aaf221c190ba76b89e8bf97926b50939da5`  
		Last Modified: Wed, 05 Feb 2025 01:01:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:67b21d2e4dea765ebb8131c7d5c27eb9c9e13b2d1e80e031546a4d79d2b7bbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8880420b5f4faebc1199852c1f9d949808ae756aad330bc33be2bf3f979ce460`

```dockerfile
```

-	Layers:
	-	`sha256:78ce91376ddaa44273ebba5af0131484ed8b9bb07fc805670d1bf7d909a2b673`  
		Last Modified: Wed, 05 Feb 2025 19:01:51 GMT  
		Size: 6.0 MB (6048489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d550856508e86e0aa8103b6d8b26ae171f98646191dbcbe123894dc8ca49c5f8`  
		Last Modified: Thu, 13 Feb 2025 10:07:04 GMT  
		Size: 53.7 KB (53744 bytes)  
		MIME: application/vnd.in-toto+json
