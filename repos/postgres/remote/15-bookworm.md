## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:67862c7f772463809ef77c182bb66e08eee2e895e8e07ccbf476d8376b384ea6
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

### `postgres:15-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:9010f897603ef2bd8aa668ecde230fc9eb4d564961569fee243bc919b1f07b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.0 MB (152982483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020c0daefebb449a68e7e8348aba4f44cdbbdc73f73a69e461d066beac891f86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:16:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:16:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:16:42 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:16:42 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:16:46 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:16:46 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:16:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:16:49 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:16:50 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:16:50 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:16:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:16:50 GMT
ENV PG_VERSION=15.18-1.pgdg12+1
# Tue, 19 May 2026 23:17:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:17:02 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:17:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:17:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:17:02 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:17:02 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:17:02 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:17:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:17:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:17:02 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:17:02 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:17:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924bcc7392585441a22938467471200d94236f7eac7cf696245d05ded557933f`  
		Last Modified: Tue, 19 May 2026 23:17:21 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea4ebf0fc6844b522eccc92beb1140c1046511c93c8d47ecdac5280644a7f4d`  
		Last Modified: Tue, 19 May 2026 23:17:22 GMT  
		Size: 4.5 MB (4534253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddea298be3ab41c0ad9f9f886e4f2516ec7925c25bb23698ded37581a21ea34d`  
		Last Modified: Tue, 19 May 2026 23:17:22 GMT  
		Size: 1.2 MB (1249554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbc17768e8724a84ab20f8b885920db66ba6ed31308d68e455accf05fa142b5`  
		Last Modified: Tue, 19 May 2026 23:17:22 GMT  
		Size: 8.1 MB (8066440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7eb41a6117378946e51215c52c6b23d4daf451f18293e2516e1062be456a26`  
		Last Modified: Tue, 19 May 2026 23:17:23 GMT  
		Size: 1.2 MB (1196420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f471f8bbc237d36a0d6255fe4756152d2322b3fcdfbe46c0140e75ed6e3b317`  
		Last Modified: Tue, 19 May 2026 23:17:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d594328e1e98705e336928af08816413b179912267e81127d1461156264ea6cd`  
		Last Modified: Tue, 19 May 2026 23:17:23 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2daea66337fac8700fe3fcd22e0a921c1bab1fb1fd2c95efd2e569bb71f509f`  
		Last Modified: Tue, 19 May 2026 23:17:27 GMT  
		Size: 109.7 MB (109681486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8834d0e99fe10284297baeb00e3ed6854f2c6035cc63af4b42d2828560ab3f3c`  
		Last Modified: Tue, 19 May 2026 23:17:24 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaae1e62c8ce4fe47bcef54a1714f0314092ecd0be08e73742cc8ceccb0b0b57`  
		Last Modified: Tue, 19 May 2026 23:17:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b26195318c616ff4c62d856e068e63c1bf5c0ed4d1abe424a13981e2f23426`  
		Last Modified: Tue, 19 May 2026 23:17:25 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abaff324c538e8c6a8eed0e1d751fc1f07e4a7e086279be1d09db4daa035b06`  
		Last Modified: Tue, 19 May 2026 23:17:25 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6a523f90ce9b136783b6c87468c4850c74f389986cb22ee8793b1e1351faee`  
		Last Modified: Tue, 19 May 2026 23:17:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e5bbc9a9640f0b3db0bdc9b3f3d575b9216a5439bf3ef8a8cef9b5cdfbb34e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fa178795ee771ef96cb5d8ab8c1f45c531c6d231cf996c4e21fe80b7557371`

```dockerfile
```

-	Layers:
	-	`sha256:046b4f3492983d8eaca3e3b210be361364468f25d0fef6303fb77bcd6641fc29`  
		Last Modified: Tue, 19 May 2026 23:17:22 GMT  
		Size: 5.8 MB (5843366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a47a71eaea6630de5c19bdbf001e925da4b109171a208d043ed3afcfa37d64`  
		Last Modified: Tue, 19 May 2026 23:17:22 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:5826b73b5830c6018360a403aaf953abc085ed95f9dfda81ee4ec56e17085c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145927081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcd2f40d1592fc9326e00b9c7d16ee651931196a3e39fd0e867c54a6f2179a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:29:17 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:29:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:29:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:29:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:29:41 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:29:41 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:29:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:29:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:29:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:29:47 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:29:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:29:47 GMT
ENV PG_VERSION=15.18-1.pgdg12+1
# Tue, 19 May 2026 23:44:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:44:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:44:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:44:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:44:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:44:43 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:44:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:44:43 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:44:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:44:43 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:44:43 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:44:43 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3544dbf04bef6535b70ef042eb05c2c4752aa8a7648b6eececa7f479f499b9`  
		Last Modified: Tue, 19 May 2026 23:45:02 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdc47f3cce9c868c3d3f1c863406f70ab3d5b6e492ceb9d2f5c1bd9fad6ad9a`  
		Last Modified: Tue, 19 May 2026 23:45:05 GMT  
		Size: 4.2 MB (4151247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abf96ee3ea6ede95234c97416999306adc1ee848b3e4c0734bc9258bc373185`  
		Last Modified: Tue, 19 May 2026 23:45:02 GMT  
		Size: 1.2 MB (1220113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab060f98d89ae414c0f69aeb11c5a6145987a06bd9e43f79499da6d8e9999e7`  
		Last Modified: Tue, 19 May 2026 23:45:06 GMT  
		Size: 8.1 MB (8066558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189e6fd1b6ba7dfa86c081d12ae090955218f7ca3f177bf648fbf5756aeda6ad`  
		Last Modified: Tue, 19 May 2026 23:45:06 GMT  
		Size: 1.2 MB (1195071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f308ac8236d2cde79ac9142193003a88394bfada3d19396e40e884442ccef4`  
		Last Modified: Tue, 19 May 2026 23:45:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb3c3a6050503e47692c48d6fe897c34a823ebca143f1666cf1b5149ef2a66c`  
		Last Modified: Tue, 19 May 2026 23:45:06 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1053adeff8508ec8ccae672434cef7b9fed1f7177e59450200a60cedff4d8fc`  
		Last Modified: Tue, 19 May 2026 23:45:37 GMT  
		Size: 105.5 MB (105505014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d088db9cb4cd74a687bbaa504329e654636f5e00ff76db368f1f3758ab73f10f`  
		Last Modified: Tue, 19 May 2026 23:45:10 GMT  
		Size: 9.8 KB (9784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ac990fa8c36647c2aaa7e47b2e7152283dcc1e7ceb7e763ed11ee3583e24b3`  
		Last Modified: Tue, 19 May 2026 23:45:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4c10f25cc6b1d92826d2aa36c210bb5e7f0659c44884d48c30edf46f20bf21`  
		Last Modified: Tue, 19 May 2026 23:45:10 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc6c84a2dc1cfcff1c9822272b538f6efecc48513cb2b348183476b8a2d2482`  
		Last Modified: Tue, 19 May 2026 23:45:13 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00181bcaa93103f33f4c117b408ec0d81c4402ee78397b02eb5c16448774f3c`  
		Last Modified: Tue, 19 May 2026 23:45:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:957efd2b3ac43e46a5b8e9db9dc75d3163977d08da4d2ab386561c099d004e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12c3e872f7f6ff9a772c0e9fd90e4ae6440993a11df0864cf9d13dc2099fc68`

```dockerfile
```

-	Layers:
	-	`sha256:b6109d38a403d37a56082ca7586b24ce82590606b3c1778f3c8c2e00e1053960`  
		Last Modified: Tue, 19 May 2026 23:45:05 GMT  
		Size: 5.9 MB (5857467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a8f2cbf77e35ca5fef91a59e1a86aa0701feec14a1f5c1793c81f7dd31da8c6`  
		Last Modified: Tue, 19 May 2026 23:45:02 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:6263fc1c9047df4f1d265f395177d484273072518cb25bc14923be459519e189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140979672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad6b0939c450fe3206a86dc0208ae2097b18750d07b8ea0a7049eb1f876e5cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:45:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:45:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:45:58 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:45:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:46:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:46:03 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:46:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:46:07 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:46:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:46:08 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:46:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:46:08 GMT
ENV PG_VERSION=15.18-1.pgdg12+1
# Wed, 20 May 2026 00:00:13 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 00:00:13 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 00:00:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 00:00:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 00:00:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 00:00:14 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 00:00:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:00:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 00:00:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 00:00:14 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 00:00:14 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 00:00:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f39c32c1a22f06f05f9c40b6a0f8d2f3b70fb8135dc65ca259458f4e3328847`  
		Last Modified: Wed, 20 May 2026 00:00:31 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a674382d9fa5d91bf1027c3f6c5a0e0b5a534ab801381b73a6550c5346d5411`  
		Last Modified: Wed, 20 May 2026 00:00:31 GMT  
		Size: 3.7 MB (3742686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3d8719595fef400464d4cd3d32a81129faa56e521a18d07baf1fcf2d5a0c9b`  
		Last Modified: Wed, 20 May 2026 00:00:31 GMT  
		Size: 1.2 MB (1216034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44651a593a5060b7e15d8a68fa9ceab3e7833216dd3e5e1b83145b2a076e0f`  
		Last Modified: Wed, 20 May 2026 00:00:32 GMT  
		Size: 8.1 MB (8066466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e7bb7d80c2f2fd9298c9c7dce4c8e6827ab922dc570440547c4b16d32bba3a`  
		Last Modified: Wed, 20 May 2026 00:00:33 GMT  
		Size: 1.1 MB (1067265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709afa4816d2593bccffe1ac5829f302d3bf223bafcec02438afb16e86cae27d`  
		Last Modified: Wed, 20 May 2026 00:00:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777c88a5859baa925eb76dc0ec40792c5ce4ede91a5d686793d1459159b001e2`  
		Last Modified: Wed, 20 May 2026 00:00:33 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0416d1d89ef396ab0f55b30584d326d486a6d4211607369c93e9fc2c72460781`  
		Last Modified: Wed, 20 May 2026 00:00:43 GMT  
		Size: 102.9 MB (102924791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91873360395ff7a49b313987db83a688f2f0016c44cc22844fad3294226de506`  
		Last Modified: Wed, 20 May 2026 00:00:34 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7148ca38c417506bc720af107c3086b6354b63488d76c186c51a70cdfd84f32`  
		Last Modified: Wed, 20 May 2026 00:00:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f376731010afbe45b7f2129f57e43aff4cd904271c9c4a47bb3a832446a7e2`  
		Last Modified: Wed, 20 May 2026 00:00:35 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb253c78c19dca2c5ee8a074b4aa5794f17c370b6756425b1d0acefdbf53ee16`  
		Last Modified: Wed, 20 May 2026 00:00:35 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9c69922cd21e4e92ffabf42df5e38bd95262555611df4ffd521295bbfafa2a`  
		Last Modified: Wed, 20 May 2026 00:00:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:df2fe304497e8139aead61f8e57f8284539bb00461c4fff4820479c3d17b1079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5910225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8468ce89ee4dc2b39140c7692fa04857f16b67dc9dc2fae68c695ef8cba9857f`

```dockerfile
```

-	Layers:
	-	`sha256:607c5fb21ca3aff75d82d42b64bb7a5bba13cadc84d560845bce4ee22e0033c4`  
		Last Modified: Wed, 20 May 2026 00:00:32 GMT  
		Size: 5.9 MB (5856722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b256c7429d0188bf00ec75bb92ce7fea5cd1c7cf259a045d86b2d886be9eab`  
		Last Modified: Wed, 20 May 2026 00:00:31 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:990e14655b8f76edd4704f944788060b18117551a6a7a295f46a86fa3fbb053a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150983899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5954dac8e2ecf74e52d8ae13143b93551b499f66a7e2ef3cbfa03d1d46c47ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:19:09 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:19:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:19:21 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:19:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:19:26 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:19:26 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:19:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:19:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:19:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:19:29 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:19:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:19:29 GMT
ENV PG_VERSION=15.18-1.pgdg12+1
# Tue, 19 May 2026 23:19:41 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:19:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:19:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:19:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:19:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:19:42 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:19:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:19:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:19:42 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:19:42 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:19:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2820e2ff1153ca549d336f7ad88e90d932758fc7d8c8da84f2d6333a8883e651`  
		Last Modified: Tue, 19 May 2026 23:20:01 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed780ebd36c43ea45fea4812464309967c2d00efc4babd4b5f97d523cde1dca`  
		Last Modified: Tue, 19 May 2026 23:20:01 GMT  
		Size: 4.5 MB (4519559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ebbe867b34a5ca453f39fefe78cb751c0c23d2269bac4bdb6a03a1c55e898d`  
		Last Modified: Tue, 19 May 2026 23:20:01 GMT  
		Size: 1.2 MB (1203323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a44b60a5101c6196e711594d03359fe80e14c7a24724c71752802b95976cb`  
		Last Modified: Tue, 19 May 2026 23:20:01 GMT  
		Size: 8.1 MB (8066455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577243fa2b24cf13637ebbd3dfd283078a0732d7319e2a070b3544c3acd6b579`  
		Last Modified: Tue, 19 May 2026 23:20:02 GMT  
		Size: 1.1 MB (1109072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4668feb5fd1082a49a2164fe847b84c39008ed62c4da18528d9e3ea7454abbdd`  
		Last Modified: Tue, 19 May 2026 23:20:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2ec8d76ab1d081daf8f9edf163d7e861a4db9b7714841a0c9083a0087a98dd`  
		Last Modified: Tue, 19 May 2026 23:20:03 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2673a6f121eac64a41edf6a046c24f91d2a985b2df21dd789c2c90db639cad8`  
		Last Modified: Tue, 19 May 2026 23:20:05 GMT  
		Size: 107.9 MB (107949671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9daafa8ed71cf19e32d307d06c04f3d0049a10f8287a3b10faa567426cb4447`  
		Last Modified: Tue, 19 May 2026 23:20:03 GMT  
		Size: 9.8 KB (9780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcad71e675d17565b223f32ae439cbd7ec1c2ddef6ece600ae15984c427cee`  
		Last Modified: Tue, 19 May 2026 23:20:04 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b606ae3ebc9eb5f9c7a2b186da8292b31ff5c9c77ab4b19ca31fc1a92b100988`  
		Last Modified: Tue, 19 May 2026 23:20:04 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f31c9bc870f32e6c2399e3ab0cb99e80cdc899d96df4fdbfe130d1e80d73100`  
		Last Modified: Tue, 19 May 2026 23:20:05 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e376441b6ebeaef9560801f6be0439f991dab8e64b0dedc9e29c6a11b2888f0`  
		Last Modified: Tue, 19 May 2026 23:20:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:cf7d41a7a3bafb02a1509c04ed5c06eaf9329fb5a24d04776f40f3662ee0a771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5903216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeaf5435badd57e62aff12e59111acd775ff205bb41648f39073b2bac43e57a5`

```dockerfile
```

-	Layers:
	-	`sha256:0228a7e796ed22e57ec4496c90f2fac17b0fa69e7c373bfb853906c86743fa51`  
		Last Modified: Tue, 19 May 2026 23:20:01 GMT  
		Size: 5.8 MB (5849677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed39a1a35682dc11ddd295afb5ecacbc0b7044edd7f372a1f28ac6ff1961be3`  
		Last Modified: Tue, 19 May 2026 23:20:01 GMT  
		Size: 53.5 KB (53539 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:1049dffc55ebeb88f69627b03df703901fe2df16c6002c09d846f041e9f97a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161688609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ed288c41520f09155554386ac6cca746a27134b0735dec3a607619a85a7ecc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:14:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:14:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:14:32 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:14:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:14:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:14:37 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:14:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:14:41 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:14:41 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:14:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:14:41 GMT
ENV PG_VERSION=15.18-1.pgdg12+1
# Tue, 19 May 2026 23:25:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:25:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:25:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:25:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:25:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:25:16 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:25:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:25:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:25:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:25:16 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:25:16 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:25:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e282e02a26dd9d5fd3d9378de5c847c196f96f781245ca44cb135ceb954c17ad`  
		Last Modified: Tue, 19 May 2026 23:25:36 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818a730a38919b4f2eb2c0343c41cab1066dd30350df3473811a84ce574933e0`  
		Last Modified: Tue, 19 May 2026 23:25:36 GMT  
		Size: 5.0 MB (4966065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb9e546eac681ef9c949b5668e237f3eadb242402a6a3830d3960b661db3acb`  
		Last Modified: Tue, 19 May 2026 23:25:36 GMT  
		Size: 1.2 MB (1218619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9300e6996993720dc392d4ec3960a0b48f61ff4ce0a8cf8ffc8da8807a2b274f`  
		Last Modified: Tue, 19 May 2026 23:25:36 GMT  
		Size: 8.1 MB (8066413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef28f96ff261dd3db301adf39eed69b76cba0f1f41394f09eb8456e6ed8e26c`  
		Last Modified: Tue, 19 May 2026 23:25:37 GMT  
		Size: 1.1 MB (1137471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b71d9e23cde08ac985a12857e02dc876c4fd9eb47f55ec57523404fc41e0fe8`  
		Last Modified: Tue, 19 May 2026 23:25:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1b618d97cb538da4535ff97b9de8053f3cd6501f195d7064aafdad4fa7f74e`  
		Last Modified: Tue, 19 May 2026 23:25:37 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e143cd208ee6bdda74b168d31ff41cc9105415120002bff3dbb115b46f60173`  
		Last Modified: Tue, 19 May 2026 23:25:40 GMT  
		Size: 117.1 MB (117060650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b44548736a6f94382a958129796825f56c15540a034f3bb66970c3f06ebf6dc`  
		Last Modified: Tue, 19 May 2026 23:25:38 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d92b12d73e5003ae6a20f7a4c0a23bae9df031c4296f9d2cba3649bc5cf5753`  
		Last Modified: Tue, 19 May 2026 23:25:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b447d61c6be6ab117a5b032eee937c8a35d6b2f6f58061bebfc8d4204872db`  
		Last Modified: Tue, 19 May 2026 23:25:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839a237834c1074b1f209ff2894311554276d8f6f11177aa699a4a4ca7f689c0`  
		Last Modified: Tue, 19 May 2026 23:25:39 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2502866d8b29498bbf264bcc6ce3757890cc171992cff0390cc735496e78cd`  
		Last Modified: Tue, 19 May 2026 23:25:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:42a86b96d39c5ec3dfd977d467c6619074b844bfd43cafef28351b627810bb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88815aa6579b0b0002b09018ca6dc0a451fdb66414015fdf7c260f0b1d0eef2`

```dockerfile
```

-	Layers:
	-	`sha256:2ebc458943fabebf9087101ddca77354a93b515f34d4cce2977630c08836a682`  
		Last Modified: Tue, 19 May 2026 23:25:36 GMT  
		Size: 5.9 MB (5855610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12b9ddc1213dda2d9369e4364620d348bd792fd751eb94a5f02bfaaacbf23580`  
		Last Modified: Tue, 19 May 2026 23:25:35 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:c3a656ebb6ce5cb43d8244a7b8d8eeea86a4fd834667d2664339789364ef455c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.8 MB (151783660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf5136db8833f2b08efb1723fc3469f35a4d46d08774fd4d21bec8a0674da95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 00:06:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 09 May 2026 00:06:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:07:14 GMT
ENV GOSU_VERSION=1.19
# Sat, 09 May 2026 00:07:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 09 May 2026 00:07:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 09 May 2026 00:07:42 GMT
ENV LANG=en_US.utf8
# Sat, 09 May 2026 00:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:08:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 09 May 2026 00:08:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 09 May 2026 00:08:05 GMT
ENV PG_MAJOR=15
# Sat, 09 May 2026 00:08:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Sat, 09 May 2026 00:08:05 GMT
ENV PG_VERSION=15.18-1.pgdg12+1
# Thu, 14 May 2026 23:43:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 May 2026 23:43:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 23:43:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 23:43:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 23:43:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 23:43:55 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 23:43:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 23:43:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 23:43:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 23:43:58 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 23:43:58 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 23:43:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8e1a6f4f5a9e9628f902e3c8df639d1691d7f1000dc904f820155d1b9b2fa2ff`  
		Last Modified: Fri, 08 May 2026 18:20:04 GMT  
		Size: 28.5 MB (28526280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd791120c9d0fd5ae541f4efa02eac6975d5d521dc7713c7c0a5580ce265c4a`  
		Last Modified: Sat, 09 May 2026 01:22:41 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadbfdae50a5c8aa838603ee76bf9e1fc8ec6b440308f4db99142611dc5993e1`  
		Last Modified: Sat, 09 May 2026 01:22:42 GMT  
		Size: 4.5 MB (4475224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b923703b3af581ebee9e4272469b019a1b7c32026c82e2e5bceb9fe34f99e7b`  
		Last Modified: Sat, 09 May 2026 01:22:41 GMT  
		Size: 1.2 MB (1159237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b79102effcd09fd07d148fe64add7df15e3fd82ad665383ab1497a3dbb472c`  
		Last Modified: Sat, 09 May 2026 01:22:42 GMT  
		Size: 8.1 MB (8066715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1edfe569d18ce1b4a1ff0a80ffb62bdb50d73a0907b94ba210053462a9123ca`  
		Last Modified: Sat, 09 May 2026 01:22:42 GMT  
		Size: 1.2 MB (1182949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a94ef0e8381b9e5f5762910a868bf0ff569db77c3db867fb3fb03a4b4f12cda`  
		Last Modified: Sat, 09 May 2026 01:22:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3144afc30e2cc8cbb96a6cbb6e4779570c8f8913d38f069dca79e86d70e260c4`  
		Last Modified: Sat, 09 May 2026 01:22:43 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8e2a7efa96cd70bc6ecf0c0a2edfc1d465baa00a9cfc0b237d8706409dd7ca`  
		Last Modified: Thu, 14 May 2026 23:46:00 GMT  
		Size: 108.4 MB (108352444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c1b642307ab9eec8ead8c7120df1f6783e35dc79464b578dd7a6b1acffa2e0`  
		Last Modified: Thu, 14 May 2026 23:45:49 GMT  
		Size: 9.8 KB (9795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fa47d5546925b1946e682d123ac3ddf67f65861aed6c08adfeeb9a9def159`  
		Last Modified: Thu, 14 May 2026 23:45:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba5f1550fb062e9b4b3638042ee0e338bd8e5dcf8ae7395d068bb170911e6ca`  
		Last Modified: Thu, 14 May 2026 23:45:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d9416aa787770610a4fdfbd2e655da52b289c757e398ee3eee9c6e6e002768`  
		Last Modified: Thu, 14 May 2026 23:45:51 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c1eaadb922f5c9dc6fb58770b032ea30e7423e2c235f026bacd9360b2a3a5a`  
		Last Modified: Thu, 14 May 2026 23:45:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:142531acbf9f1bdc04a6b6facc0216b773e285fa1ab9b723040858077111ba27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f25f80eda2ecbad60b72698451035b397b61fdc6d1ef4a8f03ac05b1c0fa31`

```dockerfile
```

-	Layers:
	-	`sha256:ac39887c6931ce63b14c0a6552e88bcb12baaf4ef107fb6e625e7b6577bee4c9`  
		Last Modified: Thu, 14 May 2026 23:45:49 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:76a0f0f9f30746ddad4abd07935b4cf7a5a221ca1f2ca25e8e4a09e9af797884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165712252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd39a2edb777c03fdec17ba7d2053b0c29aab235b2d1f3ebe6dc14fe7617b697`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:54:56 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 20 May 2026 00:55:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:55:19 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 00:55:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 00:55:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 20 May 2026 00:55:28 GMT
ENV LANG=en_US.utf8
# Wed, 20 May 2026 00:55:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:55:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 00:55:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 20 May 2026 00:55:36 GMT
ENV PG_MAJOR=15
# Wed, 20 May 2026 00:55:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 20 May 2026 00:55:36 GMT
ENV PG_VERSION=15.18-1.pgdg12+1
# Wed, 20 May 2026 01:00:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 01:00:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 01:00:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 01:00:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 01:00:41 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 01:00:41 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 01:00:41 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 01:00:41 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 01:00:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 01:00:41 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 01:00:41 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 01:00:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce87ef6f1a5847b278239303e6b089da44d7a69824f6cfe040383cad9c3992c2`  
		Last Modified: Wed, 20 May 2026 00:56:52 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdae2aab66573294d2fcc04d501289426669ccb0bc353022e4c72da06d162241`  
		Last Modified: Wed, 20 May 2026 00:56:53 GMT  
		Size: 5.4 MB (5368572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a553d4b217c22cbbc8a14b1d6c1654c49bdbb2d010c2e36a1c5bb9113dfb5f89`  
		Last Modified: Wed, 20 May 2026 00:56:52 GMT  
		Size: 1.2 MB (1208168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654c472e3936e298a8ba1664efdb8192df3c9d1e9f791c763838c95a24d3dfcd`  
		Last Modified: Wed, 20 May 2026 00:56:53 GMT  
		Size: 8.1 MB (8066498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e8ae067614dbf4c9e50c65a6c1225017e3a70dc00692e6dc3e95d8726e8a0d`  
		Last Modified: Wed, 20 May 2026 00:56:53 GMT  
		Size: 1.3 MB (1283632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f019cff237b5fde7d065a46017e8f8b30a1c7407dd67f08c0edfe29445fe14d`  
		Last Modified: Wed, 20 May 2026 00:56:54 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5523beddb72fec062b4eb265a14bb9530bb2acc7e5ec344037c613e1ab3b15`  
		Last Modified: Wed, 20 May 2026 00:56:54 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dec69bcfbf80c9f80c9b920fa25d3909602a8f15c074bc21e3bba1a1ffdd5f`  
		Last Modified: Wed, 20 May 2026 01:01:25 GMT  
		Size: 117.7 MB (117688864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fd923c6ee35d474cc35f0fc3b173e7e1354da2b848d918317a7494e0c8ce92`  
		Last Modified: Wed, 20 May 2026 01:01:22 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab795c3099f8cdc76ecb2bc0f1e48744eeee6dbb24f876f0c1b148af2eae69ba`  
		Last Modified: Wed, 20 May 2026 01:01:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e2aec0708423ffec49ef58ba8c52d4604987e815ed9fbd96c99300a6806b53`  
		Last Modified: Wed, 20 May 2026 01:01:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa2a852b9d24d486ef3e30051ce856fa84a20d44290841d31fef87406a2d5d6`  
		Last Modified: Wed, 20 May 2026 01:01:23 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f2f23b0609912ddbcc1cb04692a3912739475950e90927eeeef17ea418e35f`  
		Last Modified: Wed, 20 May 2026 01:01:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4888821ba67db52b64aa96235c26b2edbf3e1152d541be25188c35b2d17676d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c13ca2b38b1f199c38b9b432dfd3185fd620db02047eaee2e0fb7984c4510c2`

```dockerfile
```

-	Layers:
	-	`sha256:e99e2b6fb083ce655d8e4cebb56a01e099de3f05befb288a221784462a2c4548`  
		Last Modified: Wed, 20 May 2026 01:01:21 GMT  
		Size: 5.9 MB (5850727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3fc55f3768d59025a988f3663deb44dc75ff7a321db9084005197a546607411`  
		Last Modified: Wed, 20 May 2026 01:01:21 GMT  
		Size: 53.3 KB (53349 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:2526155284f2b73c6c30d06bd927fef639f5c49436f572bdf19f0bc0441d4909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162148972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c5f162f45230276d26fea21694b87c2b1a3fc1adae42cc8249c568982459fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:43:23 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:43:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:43:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:43:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:43:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:43:39 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:43:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:43:42 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:43:42 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:43:42 GMT
ENV PG_MAJOR=15
# Tue, 19 May 2026 23:43:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Tue, 19 May 2026 23:43:42 GMT
ENV PG_VERSION=15.18-1.pgdg12+1
# Wed, 20 May 2026 00:09:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 00:09:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 00:09:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 00:09:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 00:09:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 00:09:54 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 00:09:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:09:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 00:09:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 00:09:54 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 00:09:54 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 00:09:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b006f6ae0182de902bcd3fe912ec830a3a66ebb8d2db3aebff7cd91c2d3a3e`  
		Last Modified: Tue, 19 May 2026 23:57:14 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09eb8fe49218a2ec93d5c0557a572c5f56347926c0f0f71f448f02fbb57c7886`  
		Last Modified: Tue, 19 May 2026 23:57:14 GMT  
		Size: 4.4 MB (4391180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b19a008846fc5c75ab35f84b480bab358cdf7bcf47ce5bf2b4a27805a4bf47`  
		Last Modified: Tue, 19 May 2026 23:57:14 GMT  
		Size: 1.2 MB (1222832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc42137609b6ed8fd14fa8bd491ffbda7f254c2bc6144e609171c78f8f55d27`  
		Last Modified: Tue, 19 May 2026 23:57:14 GMT  
		Size: 8.1 MB (8120766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575e5ccc4a661fdbda075fe96841ed90f34b0afc7d198f488e0eb5d64e652259`  
		Last Modified: Tue, 19 May 2026 23:57:15 GMT  
		Size: 1.1 MB (1097081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18aa2a7e208dc02c585a55d7da0236adead6219eb224ea22adf1648e677d53e6`  
		Last Modified: Tue, 19 May 2026 23:57:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b93e00c15b8e343e276d05dc9f141a2180ea2514659c27bdee95deeb015aa`  
		Last Modified: Tue, 19 May 2026 23:57:15 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054be05efd4eae7fdd44217754a6c5116980b0bef48cef3c0460cc1a48e4c847`  
		Last Modified: Wed, 20 May 2026 00:10:28 GMT  
		Size: 120.4 MB (120407729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be088d851d32a57f61cbcb450ad8eaa76332e3e1a71478e357f52fc92f7b79a`  
		Last Modified: Wed, 20 May 2026 00:10:25 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec710d14b6811d27418d557019869c848511cbe48757081a053f3785117ca5ec`  
		Last Modified: Wed, 20 May 2026 00:10:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d329bb37e31a8e8c814ff27c2234c138d4bc804286b8b25eea0d5c11a536f349`  
		Last Modified: Wed, 20 May 2026 00:10:25 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dc0466edd348450531c8d689f78a7d2b6269d6d4249bfaa9e39d7db4d7b77c`  
		Last Modified: Wed, 20 May 2026 00:10:26 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f897cfe1d06eda12ba3eb0c229a8e87d9d587d55801685daacd486eac4c36a`  
		Last Modified: Wed, 20 May 2026 00:10:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8a547c71f586b177729961c612f1d6274f621750d8c777009487ddca4a3ab5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7041ef75ef919926bc89c5457a196802cd296568f3e00e3c29df595547c90025`

```dockerfile
```

-	Layers:
	-	`sha256:c2bd2fb8061324f4770ed3830836d63baabfbf0eec501c56ae9c980c500600b6`  
		Last Modified: Wed, 20 May 2026 00:10:25 GMT  
		Size: 5.9 MB (5852086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac7f1e243bbc0033692728925171a9806666464dba96b41486f3132a00da34d`  
		Last Modified: Wed, 20 May 2026 00:10:25 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
