## `postgres:16-bullseye`

```console
$ docker pull postgres@sha256:5f0431377729e673d13f81c881a2cfb79486ab95c4e9982bc0ce1a686516cfdd
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
$ docker pull postgres@sha256:844c3e620fd186efd1759d6d2993c66832c35991db50a6177653afde54a7f026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149243763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d316ffd0421e6e7efdbea32c64b92ccb432b6e81b4fcb7710294c45b057d7c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:14:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6-1.pgdg110+1
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92dc2eb367be8cc0cba9bfb3489b08711459c953babd541306dbd379074ead`  
		Last Modified: Tue, 03 Dec 2024 02:28:01 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a911ef18988b55a11eec7d2d58257f563fedeb930bb04782722160e997dfacef`  
		Last Modified: Tue, 03 Dec 2024 02:28:02 GMT  
		Size: 4.3 MB (4308157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd875b586bf63203fa81261a8ef994cc70d4bd2625254117a9a30196e8af89d2`  
		Last Modified: Tue, 03 Dec 2024 02:28:02 GMT  
		Size: 1.5 MB (1472214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b606effe188e2db71aa614afc6296e5ac5e76af627a7c27e3e79caa66b33aa`  
		Last Modified: Tue, 03 Dec 2024 02:28:02 GMT  
		Size: 8.0 MB (8044534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b20fe2397c17bafe5524cfa4d9c49f3d3088bdbf4c12168db2b416b4e681ea3`  
		Last Modified: Tue, 03 Dec 2024 02:28:02 GMT  
		Size: 1.0 MB (1038335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006f0e9d7d8014976c595e9185cf64c373075788df993354eeed86a34c6cfbbd`  
		Last Modified: Tue, 03 Dec 2024 02:28:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d302c6b75a17915e74291636c46d30eff23e621fca807196e990c4987138108`  
		Last Modified: Tue, 03 Dec 2024 02:28:03 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b251a4cb8686a44523e9b7e61b99ba9e8010dd0e7b8e63564dc48179691add55`  
		Last Modified: Tue, 03 Dec 2024 02:28:05 GMT  
		Size: 104.1 MB (104107121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ad93845193eaed01efc2c2141fdc3224a5bbdecd5f56ff8b67048ced8d1cf5`  
		Last Modified: Tue, 03 Dec 2024 02:28:03 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daea8749ff5c8ce7139970e76a8bca70ecc475819227c659b7de88b2cfdd36d0`  
		Last Modified: Tue, 03 Dec 2024 02:28:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579ec538a4efb853a68578ba3c0729da5307c7c0954615edb75eea0eaf184e13`  
		Last Modified: Tue, 03 Dec 2024 02:28:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdeed9fbf1bc0285248d7ac2381e9ccaeb916c876b6154fee325bd764fccacb`  
		Last Modified: Tue, 03 Dec 2024 02:28:04 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356cb3c8719a8b626f601e75749bbdba6c0d5d47bd173d2f3e4390b94434540f`  
		Last Modified: Tue, 03 Dec 2024 02:28:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b74555b819fd6e71495bdc0ae096718a1675ece51fa7c273ab16ef1a42baf89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6080489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3623c8e10269765f57917f224103bedd5d8d6ec05974d2c478db6d683e432cc5`

```dockerfile
```

-	Layers:
	-	`sha256:a745cb2475d1b0576bae73812cd4400291eff08b3ffc198345ffb4911dea8b7d`  
		Last Modified: Tue, 03 Dec 2024 02:28:02 GMT  
		Size: 6.0 MB (6026503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31094c83ed84b3bc547de8e40fa282527c4e94ba6410284f8fd7c04e942c7590`  
		Last Modified: Tue, 03 Dec 2024 02:28:02 GMT  
		Size: 54.0 KB (53986 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7a0d5c774d6cf750106f32a8fa4ad883dbb7751662fee4f59396e5ca54f0b85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138556554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d2f3e193fa7207b8d8a4daed966126425beed6b3c665fe62045be8eb66246e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6-1.pgdg110+1
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbaa022ef9e0b119beb47d4a40af03cbd55afe3bf050a7353d06e43694cf5c25`  
		Last Modified: Tue, 12 Nov 2024 00:57:51 GMT  
		Size: 26.6 MB (26609257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996a8e55d17d62205dceee91515111eae9b32877a15584574b4fbb1ffd893d14`  
		Last Modified: Tue, 12 Nov 2024 11:37:58 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79085ce56ecea899420a90c1faa994c6e2a6be5b0d2c699b8dc9cad2163a194e`  
		Last Modified: Tue, 12 Nov 2024 11:37:59 GMT  
		Size: 3.6 MB (3601838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a612d84717c6022a49b864ab6154e8e40ecf168a31cca66c1c431f214d4ff440`  
		Last Modified: Tue, 12 Nov 2024 11:37:58 GMT  
		Size: 1.4 MB (1439292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb31a8313e6740a7df864869a720ce58a2a1afd0be22b1c5a4faca6f2c36aa17`  
		Last Modified: Tue, 12 Nov 2024 11:37:59 GMT  
		Size: 8.0 MB (8044516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce631e44ea85e5d5b5aeb686756fc11367dab2cf1a7d7b3b02920538c8241fc8`  
		Last Modified: Tue, 12 Nov 2024 11:37:59 GMT  
		Size: 908.7 KB (908690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fd50a77adf6fc2423ae28b58b90372af285845471bd629289f1c450fedd682`  
		Last Modified: Tue, 12 Nov 2024 11:37:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21772a558953dbe1c63d70a7e8ae5302ece83606f990cbdd2fa63c395d8eee95`  
		Last Modified: Tue, 12 Nov 2024 11:38:00 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3520576606523cc207827c22091c1647f0a326acca53bff05bca0a052bbed075`  
		Last Modified: Fri, 22 Nov 2024 21:37:49 GMT  
		Size: 97.9 MB (97932198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f255bf524d0aa9c0865107a00f8a8e4f3d4a1a7d1fb2495ad6a47c997be7e8f`  
		Last Modified: Fri, 22 Nov 2024 21:37:46 GMT  
		Size: 9.9 KB (9926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415aff5aa8dd47adc3ccdd72d5b8f9a623fbbed25ec5821e69085776034049d8`  
		Last Modified: Fri, 22 Nov 2024 21:37:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be8db37cbf08a405ea7368e5e28a361b6682b54ae86633d0be6fea45fa6af3`  
		Last Modified: Fri, 22 Nov 2024 21:37:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a64fed4919fa516af0fc704b048b7838db04bc0c81392188be1b8ee7ce691c`  
		Last Modified: Fri, 22 Nov 2024 21:37:47 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b3a25e19ab168d673cc996503363576433e76e0f9f4d81e09f5bf73517bf8a`  
		Last Modified: Fri, 22 Nov 2024 21:37:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:39e79bf9d8266fca1c2400ced2a80dca562362b0f86c5a30c2dd56f411cf329d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6097856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04990c2e687d86a1abaad66b3c88edd7d76cf653d9242ccaa098f8bda796b0b1`

```dockerfile
```

-	Layers:
	-	`sha256:0d4311d592320a44f7c9a8e1ece706dfd1ef59ef3de49b22e63e1427d3ee64a1`  
		Last Modified: Fri, 22 Nov 2024 21:37:47 GMT  
		Size: 6.0 MB (6043682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8d1da54e7bd96bd5405bc69c5a74d1d70b1d40461d1b1d343c6640fa63bf0b`  
		Last Modified: Fri, 22 Nov 2024 21:37:46 GMT  
		Size: 54.2 KB (54174 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:4ab4d67f516a05773e5e917403d2976ad54610d7b4e7517e5e54712cfe3ef2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146261277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c8e63216972d243f4451b1e13f16f23e35c1d53944839a73dd602b9eb422b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:14:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6-1.pgdg110+1
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8b80562b98380f4d25ff0e1ec437b36e11db387f2dea5dce6a19a4837bf1ab`  
		Last Modified: Tue, 03 Dec 2024 04:53:32 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eb784e6609ceacd3cf1cde63437ff62c716a86087589a3b7c299e8ea7f77fc`  
		Last Modified: Tue, 03 Dec 2024 04:53:33 GMT  
		Size: 4.3 MB (4312809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2153d0d5e5df27b45cb7b5ccb871564967fa58f7de67908e6fc2e3a060d2cedc`  
		Last Modified: Tue, 03 Dec 2024 04:53:33 GMT  
		Size: 1.4 MB (1404093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83d68bdff67a2c31fef8a93a01a8607cd4826cdd4f7c18b6586b8b8b2e6f9a0`  
		Last Modified: Tue, 03 Dec 2024 04:53:33 GMT  
		Size: 8.0 MB (8044485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d616d99ca3e54d6bf8a2544191d8797a5c2126f8cd2c15c4cef7c456590d36`  
		Last Modified: Tue, 03 Dec 2024 04:53:34 GMT  
		Size: 1.0 MB (1026573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9e28c761f3931f06ea9a80edce984b81e122f8049d96b9907ed38eaf14fa13`  
		Last Modified: Tue, 03 Dec 2024 04:53:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4e526653713b8164164922c64bc2ac8ac74040c69985865622e19158539e67`  
		Last Modified: Tue, 03 Dec 2024 04:53:34 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ddf2999d4d89b9ea5b8c71d99601a395c385a71699a602a90ab43dca315b18`  
		Last Modified: Tue, 03 Dec 2024 04:55:07 GMT  
		Size: 102.7 MB (102707634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d63e29f4704767d8dbe0e8eff76fbf97b7c35fbb5a7da7f12843d48e757c5c`  
		Last Modified: Tue, 03 Dec 2024 04:55:03 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574a7680edeadd7bf910f159e9f015eeb3a67ddaeb2aacd55dc777cf4484f57f`  
		Last Modified: Tue, 03 Dec 2024 04:55:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af626168849a8a54d635b414006a0d4088ae59e1d5b16698706081892547906`  
		Last Modified: Tue, 03 Dec 2024 04:55:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5855f9c41726abc088f74c445eb4a7fe9301d8c6920fa0902e0648121f068c2f`  
		Last Modified: Tue, 03 Dec 2024 04:55:04 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f032905dc50a8d4fa8ddc26850b675a02c8a9e3e7383f2bb1bdfbefeade2968f`  
		Last Modified: Tue, 03 Dec 2024 04:55:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:a942ba3d44961a366d7764be70dff190e17a8ed466524967c68e2864db568fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b2a0a788acc6a25599b5d8cddfdcf6ec61e1f87f59573fdc7eddd7307aabb7`

```dockerfile
```

-	Layers:
	-	`sha256:533e699c7ea9a1eda13046e8f7c25d96b6bd78cc99d75ad979e1e2bcfb456f53`  
		Last Modified: Tue, 03 Dec 2024 04:55:03 GMT  
		Size: 6.0 MB (6032797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff3a08a7b7bbd6d127ff88772f59c485af56fcc33cdd4ea051c14688743200f`  
		Last Modified: Tue, 03 Dec 2024 04:55:02 GMT  
		Size: 54.2 KB (54231 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:3fd67e0912e9d6bb49789c1b9c3425a7a080fc6d2297a5b8da38784f3b74cc8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157447587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b022cf99df70706446ba42bb9ff50b22e1110c816e0da18d5e1e62ae80b72eb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 21 Nov 2024 20:14:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV GOSU_VERSION=1.17
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV LANG=en_US.utf8
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_MAJOR=16
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PG_VERSION=16.6-1.pgdg110+1
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Nov 2024 20:14:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Nov 2024 20:14:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 Nov 2024 20:14:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Nov 2024 20:14:24 GMT
STOPSIGNAL SIGINT
# Thu, 21 Nov 2024 20:14:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 Nov 2024 20:14:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17915f03451009c7e622ee70739324efc84190b50d8d75e382fa7ac4adefc661`  
		Last Modified: Tue, 03 Dec 2024 02:37:22 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276ceb680db13bb33fea21f3b86f3e076519ec2053a4cd4ead23d7c7deb9fec3`  
		Last Modified: Tue, 03 Dec 2024 02:37:23 GMT  
		Size: 4.7 MB (4719688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fda0bc08b3b9eb8e053bc90cc5d146151c37acd5c01b727308ac3af56e2df2`  
		Last Modified: Tue, 03 Dec 2024 02:37:22 GMT  
		Size: 1.4 MB (1447754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5f0aec49f3f6d72e23fd80f5c98c1272d22860ff6ed541c8a0ee8bf7b5a086`  
		Last Modified: Tue, 03 Dec 2024 02:37:23 GMT  
		Size: 8.0 MB (8044283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9595e0b9f16cce8073085299a18f3893b4d1affd35bea6cb540c363b474ce0`  
		Last Modified: Tue, 03 Dec 2024 02:37:23 GMT  
		Size: 1.0 MB (1028894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384447528a0f19857c43c60fa791a90a602cf97c5d38a119e93247607832eb03`  
		Last Modified: Tue, 03 Dec 2024 02:37:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34d3510d036a52822d921d28d9fb99d9091929b6d9610607621b06e63f3bf84`  
		Last Modified: Tue, 03 Dec 2024 02:37:23 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b234f5c0fd19335eb5f1026c7e73574d72014e076a5563031be6717b5c9d71`  
		Last Modified: Tue, 03 Dec 2024 02:37:26 GMT  
		Size: 111.0 MB (111007150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e832a48646ccca63ba02bacc47284b65fa222f65adb959aa2c815ea20a00b9e`  
		Last Modified: Tue, 03 Dec 2024 02:37:24 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55451ccca91da3ecf50bff0e56972419a1bfbd7599337c9d8025d39363d0684e`  
		Last Modified: Tue, 03 Dec 2024 02:37:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f3ada332bb702af848d07524bcc05ff7d7b10f27051c4b7f95ae1bf159ac64`  
		Last Modified: Tue, 03 Dec 2024 02:37:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91e59ccc8a70e91095155a19e517f0db1df8369d7b5e3f67332d1469b6b1635`  
		Last Modified: Tue, 03 Dec 2024 02:37:25 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4b45b35ffff31afa2a06d2486272eea8cf5631664d7df40af9214b66234cf0`  
		Last Modified: Tue, 03 Dec 2024 02:37:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:9e015e2bd243d79fae8e1189483a13bbeb317b950d50a46a569684037621b596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6093526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f490ef7a4c11b1336573c5987d929cd6e227fe45863d438f9d2fac2bcb508fb5`

```dockerfile
```

-	Layers:
	-	`sha256:06fd7a5aec21505dbc308c0eceebb3303ac84220dc6c439718dfaa2194c13292`  
		Last Modified: Tue, 03 Dec 2024 02:37:23 GMT  
		Size: 6.0 MB (6039584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda1fe6a336ed202240bc9060d3b26fb12b48e8c777857c5e47034c301383dbf`  
		Last Modified: Tue, 03 Dec 2024 02:37:22 GMT  
		Size: 53.9 KB (53942 bytes)  
		MIME: application/vnd.in-toto+json
