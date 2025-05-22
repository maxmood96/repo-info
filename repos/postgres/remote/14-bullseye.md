## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:ee1c9fb48420897538196824e08347d851b91a8e66f24eeb9eba0c3a358a1a23
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

### `postgres:14-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:29df953d9db09fe7f2cf6cded156a7e6bfe96bce9409917cf4ef4215de731cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146088748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b789c9ca40076f9f16d184246ac66589ebd42408a8bfafa35d35b228f2d4da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 08 May 2025 17:29:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg110+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25f607f12f610dc4167f50c6efdc90cfb0ab87907b20b908c61b6522217c380`  
		Last Modified: Wed, 21 May 2025 23:19:57 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073204876f3579c4b9e1cc575d58be449eeab153425285cc36e2d1e8d766200`  
		Last Modified: Wed, 21 May 2025 23:19:57 GMT  
		Size: 4.3 MB (4308203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f9087594733ae2c15a83d36fb59b0392cd5c478d02380b03e477bbd2d1a9ae`  
		Last Modified: Wed, 21 May 2025 23:19:57 GMT  
		Size: 1.5 MB (1473580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03d005b78f949df916d4ac133b03a5854ba6387ea533160fa84c2092b9e323a`  
		Last Modified: Wed, 21 May 2025 23:19:57 GMT  
		Size: 8.0 MB (8045818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599da3578bc514e305ac6a50d1704accc014b61f8e8e5624b4f9cbbd5ce14056`  
		Last Modified: Wed, 21 May 2025 23:19:58 GMT  
		Size: 1.0 MB (1038349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1f00f2a59faddb76b8de31f5fab39739c8bfe2c8d09ee3a99a63a82bc45bdc`  
		Last Modified: Wed, 21 May 2025 23:19:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab6a05075123d62f0aa807990d8099ba720cf6cca7cd8de47bbc6a22971c272`  
		Last Modified: Wed, 21 May 2025 23:19:58 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd6271b1304addb5acc4897acf61e9d39f22f19ad7b6c842e12604264edc411`  
		Last Modified: Wed, 21 May 2025 23:20:00 GMT  
		Size: 100.9 MB (100946449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b4be58e07213a672060c7ba1065ddf69c3e4c0106e45710532fa95c160a37a`  
		Last Modified: Wed, 21 May 2025 23:19:59 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8612c87e7af3390bcf0fbfe90718442f42057f8af0ae00b42886164e8e82b4`  
		Last Modified: Wed, 21 May 2025 23:19:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2fd75b98bed0671231c86d43a2ee7016aaee6ff027d4655e9b8fabba5c62fb`  
		Last Modified: Wed, 21 May 2025 23:19:59 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8df8facc7a89dae4595c8bc2bac65a89c53abda06ee6eaa2a721be7ba2b3693`  
		Last Modified: Wed, 21 May 2025 23:19:59 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c95cd6278f18ce7f11178396d2954536fd6a4ce818130523e1d9c3c0f52f391`  
		Last Modified: Wed, 21 May 2025 23:20:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:9643a13b4666bbcdc0e690218c5dead6149eb07c99af165a7535af33a10ea86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6014944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bacbc94ad7d0e4746da8ec6148f80b7445b0177078182c96a9f8c25db11924`

```dockerfile
```

-	Layers:
	-	`sha256:ad2b8a70e80e1de923dfe813d980d42ab2cab7d41b79ac4dc48ef1f87cebdae9`  
		Last Modified: Wed, 21 May 2025 23:19:57 GMT  
		Size: 6.0 MB (5961472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01ba6a946fce5c405d888e9497bf7bb2409a0766b1aca729c38b1aa6afb3230`  
		Last Modified: Wed, 21 May 2025 23:19:57 GMT  
		Size: 53.5 KB (53472 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:1cff0d69608863818fd9020fd7b81dba30c0bce4b1ca22ceba520db0d1bf8887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.1 MB (138052563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5857a3e196b1c5f9c7b9ddfa3c29f8a488fbef6f638f77272421541ace1b961c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg110+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef24263d8904408d4abf0483982a747bf8153de0d52cbb43862ace352b898c4`  
		Last Modified: Tue, 29 Apr 2025 01:18:46 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be0264bb06c2bcee8451dc94c6f8355978ef236eb1a11e672dd512df9c7e7b9`  
		Last Modified: Tue, 29 Apr 2025 01:18:47 GMT  
		Size: 3.6 MB (3601746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a9051786ef8ca1e9ce4ec47810682bb5f8c26e9d78eb7e1f873f82d85c3f16`  
		Last Modified: Tue, 29 Apr 2025 01:18:46 GMT  
		Size: 1.4 MB (1439251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604c2a9e01f796a5afd8b46c903da93b951474ab34284f961ab4c3e793b7df3c`  
		Last Modified: Tue, 29 Apr 2025 01:18:47 GMT  
		Size: 8.0 MB (8044545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7035eab34ad95006258ce8e6a6d625b8c11281827a56ddc22c8384df5f25bc27`  
		Last Modified: Tue, 29 Apr 2025 01:18:48 GMT  
		Size: 908.6 KB (908650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab74d412aa207d36e88063c7272cd4c92f0e39a1c3df9afd5c17b2c29490b1b5`  
		Last Modified: Tue, 29 Apr 2025 01:18:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb07ab6f9f4f5ffcc3eb65dc7f2c635f65140e5fed60a158d072087f7a348c79`  
		Last Modified: Tue, 29 Apr 2025 01:18:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910b92a6a63816a80a16accb8100f2f31f4e7adf70f46049fe5a563551fa05b5`  
		Last Modified: Thu, 08 May 2025 21:40:31 GMT  
		Size: 98.5 MB (98495517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e069bb780316268c71dc02debbefa63cf384be519fe6edeb35254a89a7cdc917`  
		Last Modified: Thu, 08 May 2025 21:40:28 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb6bf5af31e1948755586d1e51f3b3a762b457dde6ae4c0bf412f9ebd32ef98`  
		Last Modified: Thu, 08 May 2025 21:40:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96260f3357f19573429aad49b76b50d2ee2093564b51329d88662667f00a4c60`  
		Last Modified: Thu, 08 May 2025 21:40:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a1c4b791d251590290016784b631e4dd4637c676ff57724eeedebf09c17d99`  
		Last Modified: Thu, 08 May 2025 21:40:28 GMT  
		Size: 5.5 KB (5474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a674a1c3ed0f94311f0c96de76e5881fc8d3e5f4f61575d09ce54206deafb798`  
		Last Modified: Thu, 08 May 2025 21:40:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:8b05710726bfbf84b693b92ff3d4d7b9a6e6b21aff90f77420bd21d9db233a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5997246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cbc7b9fc047a375704aac5150c7832db5221f1f97eb68c224ca9d9049ed4ec`

```dockerfile
```

-	Layers:
	-	`sha256:e0e69032ec6904964e0740a66979b31b5442714c6eb9dcf54d1e6811e3866a7e`  
		Last Modified: Thu, 08 May 2025 21:40:27 GMT  
		Size: 5.9 MB (5943585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27db80b1f6793b2184b12a788d490a405c72c116b814ced32526ec6df27f7478`  
		Last Modified: Thu, 08 May 2025 21:40:27 GMT  
		Size: 53.7 KB (53661 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:8b3124e05a2a397c43582d44d2b19cc99e18b7a485231931000a736c8ee507eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143109508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c1ae024e9df9dbb4384c318114676b6600e188514fc75ea76a739a85d3ec1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg110+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404bd1a8f8e86427de72f2fbe288e2851e3ca6f66c21f81707af02163eccdb1a`  
		Last Modified: Thu, 08 May 2025 19:18:36 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e4a45419bdc01faa6942d3df7b0056cbe1b3ae807abd905644b484b0b1cbce`  
		Last Modified: Thu, 08 May 2025 19:18:36 GMT  
		Size: 4.3 MB (4312839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11420ff58ade3dfa95b6961a171e1c4cc5b0b5f4dfdcf92dc61dfec37ea35db7`  
		Last Modified: Thu, 08 May 2025 19:18:36 GMT  
		Size: 1.4 MB (1404163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35cb431fc1ff46a71ebd98e929a9c9b13a81a511141864f072f929b67b19c1c`  
		Last Modified: Thu, 08 May 2025 19:18:37 GMT  
		Size: 8.0 MB (8044349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b901d5ef38469caa825d410c5187cea2a9f5571fcc3b52d40856a3adacf7b1`  
		Last Modified: Thu, 08 May 2025 19:18:37 GMT  
		Size: 1.0 MB (1026596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea7bfffc29008aa6a6a5509628f2fcfcb808548a826118e23e89aa29dc1ae68`  
		Last Modified: Thu, 08 May 2025 19:18:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c83b7794bdaaa3390e801accd12567fe82f24d554ec01523f443c09cfcf46`  
		Last Modified: Thu, 08 May 2025 19:18:37 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e7cd4151cf171fcfdd5dc1ac14b988a61d665ac1a44f972f9b8254b153c80e`  
		Last Modified: Thu, 08 May 2025 19:41:33 GMT  
		Size: 99.6 MB (99556491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821eddfeec6b63b7c1b104ce4a3b4c952d8723dd6168e1e635678460576bda8f`  
		Last Modified: Thu, 08 May 2025 19:41:30 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804069e69bebf7eb0ea1a43e79608221dae1b4be28359cdce6fa0e30fb8270c8`  
		Last Modified: Thu, 08 May 2025 19:41:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b58f8cab7a34a75e7b578124e99d8fda9e67c671016ef81e356394ef3ceae5`  
		Last Modified: Thu, 08 May 2025 19:41:30 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754ceb1d71577c5b0547b106f595b924852745f913a009dd5ab2e7c162c2209b`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 5.5 KB (5471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db280671dbe6f83e846e7fa653a6774dc7dbce90d5461760056c05ce31f16cf`  
		Last Modified: Thu, 08 May 2025 19:41:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:2bf5e986ad2543652a26b4975e5aaab543d6e15c5fb82e6e7e5f13859c56b87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5993823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0c4e967f21ab4247ff9a99fbe7cdb27112e9c7c912a00001d4aeaf2457437f`

```dockerfile
```

-	Layers:
	-	`sha256:ae4649ac2653281b32e59f908cb734952b1b870359f00537aea15b102c31436f`  
		Last Modified: Thu, 08 May 2025 19:41:30 GMT  
		Size: 5.9 MB (5940111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a2dbdda7f338f5ebf06e9b6ec1d7641507647fa44ab5ada43fcef63e9f297d7`  
		Last Modified: Thu, 08 May 2025 19:41:30 GMT  
		Size: 53.7 KB (53712 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:c71dd747d001ea598e0f3a66f6e3a41e7d73a8418e773e5b9b7ae12d2cc5fc9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158655394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa0d5d90fcc58b7b508e33f497906548437a09eaa7e713ae2ac24a64791644f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_MAJOR=14
# Thu, 08 May 2025 17:29:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 08 May 2025 17:29:08 GMT
ENV PG_VERSION=14.18-1.pgdg110+1
# Thu, 08 May 2025 17:29:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 May 2025 17:29:08 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 08 May 2025 17:29:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 May 2025 17:29:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 May 2025 17:29:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 May 2025 17:29:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 May 2025 17:29:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 May 2025 17:29:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 May 2025 17:29:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75b977995878cf40bda372dc1d9e6128be8ec25b465b5686929d9ec19394cec`  
		Last Modified: Thu, 08 May 2025 19:26:12 GMT  
		Size: 1.7 KB (1680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58609ae7a60b79705236ad562cace3b47019d1b6cb906566d0b54886a548facd`  
		Last Modified: Thu, 08 May 2025 19:26:12 GMT  
		Size: 4.7 MB (4719710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdc300bd305779c5f69b620ac66fcf18cdc77bc70bf983c662d3d38ed1fd450`  
		Last Modified: Thu, 08 May 2025 19:26:12 GMT  
		Size: 1.4 MB (1447750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bba11a6684c24aa6e8cfca1aa07d098e5cbc6ee9fd0a5cd9304ff16d14184f`  
		Last Modified: Thu, 08 May 2025 19:26:13 GMT  
		Size: 8.0 MB (8044299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5fbfc143c62166009e9df864203d84ad91928487cb1c2a7bc27a4b08bbb282`  
		Last Modified: Thu, 08 May 2025 19:26:13 GMT  
		Size: 1.0 MB (1028929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71a8df96436d84a7149a43f73ebb134915505cd8375c68fb1ee0b1749ead469`  
		Last Modified: Thu, 08 May 2025 19:18:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f204494363e56045180f6b91e0145953a2b1bfdbbd5623c5a6733830b2a1994`  
		Last Modified: Thu, 08 May 2025 19:26:13 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a602ba6a9a784f1212a6be5da3b0d18d4da68fa89d3f0b9e435446896d7eba5a`  
		Last Modified: Thu, 08 May 2025 19:26:17 GMT  
		Size: 112.2 MB (112206401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03464d6177b54e4ef984766d0ff3ccaff824eef02945ac845b0c866e9b5723fe`  
		Last Modified: Thu, 08 May 2025 19:26:14 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97080e648de0dd01aebe5783393fb91e0797d607e8111d389584d9f2d7d55289`  
		Last Modified: Thu, 08 May 2025 19:26:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9779518aae4cbdf96f68bafde904aaf926e3758138fe6efda906440a287fc73d`  
		Last Modified: Thu, 08 May 2025 19:26:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e444a45598c98d519d42f241dc9781b98b8b2c0a362602a23ea1b5fca8c73b26`  
		Last Modified: Thu, 08 May 2025 19:26:15 GMT  
		Size: 5.5 KB (5472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f16633d5c7d54742bfb4190c104a2014d208b4c0bcee10ee5666c3179b8e7d`  
		Last Modified: Thu, 08 May 2025 19:26:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:cc95f578e7e0f2aa7b378c1fc36d931eb2e1552a2394ac6431d79934aecd7f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5994674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeb5175ebec0ec4d662569a836304cdb842ca39764cc18ffc719e63924a0cb6`

```dockerfile
```

-	Layers:
	-	`sha256:d9a1f36156f9946a8b2d63f6ff9f207464a93aac31476c0fa0748a552c4127ee`  
		Last Modified: Thu, 08 May 2025 19:26:12 GMT  
		Size: 5.9 MB (5941245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50b451556abf39cc86e59e19af42b9070e32768476b82037f54ce6b1c4474f66`  
		Last Modified: Thu, 08 May 2025 19:26:12 GMT  
		Size: 53.4 KB (53429 bytes)  
		MIME: application/vnd.in-toto+json
