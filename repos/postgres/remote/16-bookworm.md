## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:70e9e457f70602fa7a6bc38054accbcb54a3a966c633b1f91e8d84d6b078346a
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
$ docker pull postgres@sha256:7f8b7164ab4ec5b5c4f75be76870c7a8d9d0779b520301d2f713886c5ff5a4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155236823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed30edf810c3c8c7e464c56d89ed6b6205d025b1caa08de0dfb5e39573952759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Feb 2025 19:44:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
ENV PG_VERSION=16.8-1.pgdg120+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9dabc29a097c8378396241e39365808cee8731861af54500494734d8864d378`  
		Last Modified: Tue, 25 Feb 2025 02:24:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04e3fce08507feff066238611db25b16b61ad34ceb29a2e988a752c26795235`  
		Last Modified: Tue, 25 Feb 2025 02:24:29 GMT  
		Size: 4.5 MB (4533730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01c3042d3555e6b84e1a0a6e66998d3a4c327f7453fbc89da270aa6e5349798`  
		Last Modified: Tue, 25 Feb 2025 02:24:29 GMT  
		Size: 1.4 MB (1446690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c42220db2f408190013f0c40298bbfd917acd6f823f199f618dd236c842bc`  
		Last Modified: Tue, 25 Feb 2025 02:24:29 GMT  
		Size: 8.1 MB (8066302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4124e19302b93bd6f537ddeffc0ed3b4d9b2580d4ad074082dd1c820a20f5cae`  
		Last Modified: Tue, 25 Feb 2025 02:24:30 GMT  
		Size: 1.2 MB (1196072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1938a14a35550bd4b52acda1c5db3883ec2c923dc58b2e388397977ac2925f34`  
		Last Modified: Tue, 25 Feb 2025 02:24:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5efac87c38ee94f67dc3a833af460da955d5bad76216159ca11f3adcafcc86`  
		Last Modified: Tue, 25 Feb 2025 02:24:30 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0350ae76d0afc931e9ff995cfc42ecee5ce6341bcf0d877aa3367f9683431a`  
		Last Modified: Tue, 25 Feb 2025 02:24:31 GMT  
		Size: 111.8 MB (111754488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2805a4a597395dc44423f9cd9adf289046743c1988a4b7c7b539e25db323101`  
		Last Modified: Tue, 25 Feb 2025 02:24:30 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5339c8466c9fbb61ed5349f34e384b89989e763f394d26ab9cb55fb5286db0`  
		Last Modified: Tue, 25 Feb 2025 02:24:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028f0b318409f2cddbb82182e2868dc295b50fef7f2513e9a02e36fe0fd40fed`  
		Last Modified: Tue, 25 Feb 2025 02:24:31 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2201f15ced55a918924bca608d9afde3c0dc1c94603a672ebf145049771c6f23`  
		Last Modified: Tue, 25 Feb 2025 02:24:31 GMT  
		Size: 5.4 KB (5415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d850ce22085c2d86f7f85007d9aa119cd3be0046da2b761ae9a592db0b549e`  
		Last Modified: Tue, 25 Feb 2025 02:24:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:facafe05932eababa135323d14df63b26f1e91c90035ba9441ff001710c6c9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ec4c3eeeefb864299214a4fd31cf3e83e959a4d890f82c7fa6f27567c2a0fe`

```dockerfile
```

-	Layers:
	-	`sha256:d43c9e7b89f486b6b05a1ddcc540fd9bb73c954ca9d38172dd708a0bdfd6c513`  
		Last Modified: Tue, 25 Feb 2025 02:24:29 GMT  
		Size: 5.8 MB (5801849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19011eec95f733e4b1f6f3029d9d5d1f7c14f3020d3d4b15fcd52e588eb5be89`  
		Last Modified: Tue, 25 Feb 2025 02:24:29 GMT  
		Size: 54.1 KB (54074 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:88972d2d1982ef9325e4e4c736fe4ec0dfda3103f5118fe24728e3d7efe0505a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148299083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f8fa17e7df006217685cc4c891a087826838df00ed01c2c2cd342dbc6f948c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Feb 2025 19:44:40 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
ENV PG_VERSION=16.8-1.pgdg120+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ae6e8a56f74f787b0f7d9aacaa13d7b6ddf781a6f4ad61fce864e911f8d5eb`  
		Last Modified: Tue, 25 Feb 2025 04:07:17 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7e5c1eb3eed5a4a7533ef45712de74bcdf7f12a622e29c36426ce933d0103d`  
		Last Modified: Tue, 25 Feb 2025 04:07:17 GMT  
		Size: 4.2 MB (4150963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56a7a98a42d1a7c378de936bdc8454809227da584ea5bef2b083e497eaa5c43`  
		Last Modified: Tue, 25 Feb 2025 04:07:17 GMT  
		Size: 1.4 MB (1423891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67d002c2bf3c5b50f61f0640d5aca352133a5dc309e2762537c449a3aca845f`  
		Last Modified: Tue, 25 Feb 2025 04:07:18 GMT  
		Size: 8.1 MB (8066428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c3bbd93e97b9c314fd0cdcd835f599dcfaf56503d8b1b05d433b17aaf9acdc`  
		Last Modified: Tue, 25 Feb 2025 04:07:18 GMT  
		Size: 1.2 MB (1194896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60a6013dc8012881f58cdc518550e78876486822e65bc24f835046246937f4f`  
		Last Modified: Tue, 25 Feb 2025 04:07:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e491b6f06d34de84c3d46761533989f0ba58103527e7315fd02ca1307d404efd`  
		Last Modified: Tue, 25 Feb 2025 04:07:19 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d11b25e6ecd5817fd8a29d4d7eb9c0d0670ec00a5ff6c4bc3b555759aa48c47`  
		Last Modified: Tue, 25 Feb 2025 04:23:48 GMT  
		Size: 107.7 MB (107702027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c82f06ce9e0394ef2f01645b3dfa53795de3e7f03a2cc815a4dbe19be3a452`  
		Last Modified: Tue, 25 Feb 2025 04:23:43 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33d07a2ab7a6acedd39abb8fbcaec357c3a0ba2ea0862c9365bc7991bfec82c`  
		Last Modified: Tue, 25 Feb 2025 04:23:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3034fd3759f96458b7093655501d7aaa09428a544e447592448dd22716c626`  
		Last Modified: Tue, 25 Feb 2025 04:23:43 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af647d9ea6371c4fe1d6cdccd0b66ebce3bd8a1eb24f6a307e2feff6adc1c40`  
		Last Modified: Tue, 25 Feb 2025 04:23:44 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd7c95018cc738de76fc35086063e4ae23634755c2e40eb74c649565913034b`  
		Last Modified: Tue, 25 Feb 2025 04:23:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fd0665ffe5ec4c0303d4b91c6a3dd039db3d0bcd814953980b28850a13ed9f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5872071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b003b88001106ca75c445107a33396168d7a7a20ca9e6507b36c0a28d2da00`

```dockerfile
```

-	Layers:
	-	`sha256:e8e41fe76c4dbc89abbe5b0d3755424170e58fc8a4fe5cdc38958d2f623790ac`  
		Last Modified: Tue, 25 Feb 2025 04:23:44 GMT  
		Size: 5.8 MB (5817778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68880cafaf791724925a157b5dd86c00b8576a6e5c055d4d899dd6acc5700d22`  
		Last Modified: Tue, 25 Feb 2025 04:23:43 GMT  
		Size: 54.3 KB (54293 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3eb765134ea145fa2411ed8bf3a5a74ba8da81e20724278cfa28c070318f98b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143315116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a4d137c5996bde1c2ed5abd4e9ddb9c599609a8c6f8607b572f9a1c8b7bc25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Feb 2025 19:44:40 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
ENV PG_VERSION=16.8-1.pgdg120+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef1a62fea3591817dd52ef79c2559e3f123f349e3cfb5daa531aa5cca19b472`  
		Last Modified: Tue, 25 Feb 2025 04:46:30 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7fcd67935c62da60cf72e0773d008569b0b74d953aaaa47cec7fa02c053e2b`  
		Last Modified: Tue, 25 Feb 2025 04:46:31 GMT  
		Size: 3.7 MB (3742519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c33114712a5394935dc60fd5476e337fceb02111c95d54574d741be93394edc`  
		Last Modified: Tue, 25 Feb 2025 04:46:31 GMT  
		Size: 1.4 MB (1413606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c45fc13a8ea6d2ff0d390feb17e5cecc553b36e92d0af9cec523c5b41f507eb`  
		Last Modified: Tue, 25 Feb 2025 04:46:31 GMT  
		Size: 8.1 MB (8066258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4108b27ebae515afd276a5c91e82f4b9db92464f3b632141345c92ebf2c145f`  
		Last Modified: Tue, 25 Feb 2025 04:46:32 GMT  
		Size: 1.1 MB (1066952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1741afe59bc11a091b636d1e593e15ff354fad80b9671c6764f5f460651d5544`  
		Last Modified: Tue, 25 Feb 2025 04:46:32 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe23fb58710d0e592960dbee784d541353764b757bafb7ff6025d09df4197991`  
		Last Modified: Tue, 25 Feb 2025 04:46:32 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872f2caab08db7c7abda5233e0299184416e95c821555c9d6a03f6d4d1c9b673`  
		Last Modified: Tue, 25 Feb 2025 05:17:29 GMT  
		Size: 105.1 MB (105085805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a533e9cd49633da2a8bb2d1ef24792358b0d418b604705ec42312328ca184d`  
		Last Modified: Tue, 25 Feb 2025 05:17:24 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52f01d7057cc8abdbe685a5950146cac0d5c4f7dbf460981fc1e5b18cd11471`  
		Last Modified: Tue, 25 Feb 2025 05:17:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3fe85469fa73fe87fc2a021d645ae0ab7ebcbe447e39212fd31c824f78eead`  
		Last Modified: Tue, 25 Feb 2025 05:17:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aced27024a2859c637d7aa05522d895584dff9e54cea69db6a813f26d852611`  
		Last Modified: Tue, 25 Feb 2025 05:17:25 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aeb976b7025b94896e942d7cc9afcf2f48c8e9447ce4f42d08a41c5382eb33`  
		Last Modified: Tue, 25 Feb 2025 05:17:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d9aa08c0d8ca2c1f4d7334698662fe54cf564442ecffdb98b4c463a39bf377bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5871642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96cf63b4bac46249e4cf58823aaa024ce05783177aa163e6117ae442d1933ed`

```dockerfile
```

-	Layers:
	-	`sha256:9c8e9d015d13e635c5c3c498beec31a47f44aa0e479ddb8e2a4c0827c88f1aa7`  
		Last Modified: Tue, 25 Feb 2025 05:17:25 GMT  
		Size: 5.8 MB (5817349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e09b88e1cdbfcc0171bb981e0cfe2ef1ab7ed8f297506a4ae4c04df5cfc40ce`  
		Last Modified: Tue, 25 Feb 2025 05:17:24 GMT  
		Size: 54.3 KB (54293 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:2ac53a8c535d183c6c69a54a29ace1b12df39d39e7e3f47a334856a900f42bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153062172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d9c1a3070ef1d6f7bfbec1bf4c81d63222255cac9146e6ed326529fa330bb2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Feb 2025 19:44:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
ENV PG_VERSION=16.8-1.pgdg120+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774c54d2d309bc0d9f02c69b29d119216a5a164fbf6cec3480052d097e25f9ea`  
		Last Modified: Tue, 25 Feb 2025 04:57:16 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f36104e57cc5d7fd06391de5bb22aeddbffecb409917d7ecc608c2e3f9c80`  
		Last Modified: Tue, 25 Feb 2025 04:57:17 GMT  
		Size: 4.5 MB (4499142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1655e767f751e08409bb39b05f82292ac7689e09a26a6871442725c24b57d8b0`  
		Last Modified: Tue, 25 Feb 2025 04:57:17 GMT  
		Size: 1.4 MB (1378737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8078a8a245e2f42169dc661d903d811d08a63cf566346516a68aa7477130ae`  
		Last Modified: Tue, 25 Feb 2025 04:57:17 GMT  
		Size: 8.1 MB (8066359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b1b7588421aa8a2178678ef8042b65a9bfc5ade9fea7c685f5a674906db062`  
		Last Modified: Tue, 25 Feb 2025 04:57:18 GMT  
		Size: 1.1 MB (1108728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8417b4134b63cf9697a07dcf7dc6b1801e18389ca122d20a2f66d86fb9d102`  
		Last Modified: Tue, 25 Feb 2025 04:57:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce779fa8f65c91ffc6e60cbc07d1381a8fea05e88f239cd5eb2c1000bd14884e`  
		Last Modified: Tue, 25 Feb 2025 04:57:18 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d39cdac6f886636dd2ddf9162a333ba18b86147f14fa4b117daf95eea07f025`  
		Last Modified: Tue, 25 Feb 2025 04:59:25 GMT  
		Size: 109.9 MB (109940546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cff983bc20c94678b6aba977ef9cb2bfcad8654ec77a649fb13dfcbbb9d3c6`  
		Last Modified: Tue, 25 Feb 2025 04:59:21 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecd1fe066dfbe4a3a49d8362a1d7a5ff9c4363c6100b756e750b9abdfa3b743`  
		Last Modified: Tue, 25 Feb 2025 04:59:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cf3b85b4334a1bc90d707185e88c2a80808f5d2ff3ac09b544cfb283915f60`  
		Last Modified: Tue, 25 Feb 2025 04:59:21 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7de1c49c076dcd9b4583b3fafe98fcf72d262fe6c0873e854212b52cbef0dd`  
		Last Modified: Tue, 25 Feb 2025 04:59:22 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1478a2fc4bda297fa502bd3dda967a0c80e673c7edfc92a463274c3aa54f830a`  
		Last Modified: Tue, 25 Feb 2025 04:59:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:f8934bce19cc87406bc748dbad2f5ac09c71e655366d274933bc2bb7de009117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5862531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef82739ed45f44f75895e6faa2a1e6277c5c228133d1fdd96a52d54f5c9e7d2`

```dockerfile
```

-	Layers:
	-	`sha256:f685b385c183b420c7670b3d84f72f385d1f283d1e77156018d173ecdd764648`  
		Last Modified: Tue, 25 Feb 2025 04:59:22 GMT  
		Size: 5.8 MB (5808188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a49daddbcdf79f1da0176a68811744143cd02b6dc7be0de3bf1b64e8d59141`  
		Last Modified: Tue, 25 Feb 2025 04:59:21 GMT  
		Size: 54.3 KB (54343 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:7d1f4feae808bd270cffc2df87dc0be81442ffd325428f136242f831bae77f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164100659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63772806f9965af4827b24a9d77ac0ffd09fe08b57df617d6722a8433ec44eda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Feb 2025 19:44:40 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
ENV PG_VERSION=16.8-1.pgdg120+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0353b2a402e1faa135c63425a248fe36603427b4c93b6e24e6ba8c87392ebcd0`  
		Last Modified: Tue, 25 Feb 2025 02:36:41 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8fcd1368f2108934ae95c120018355ee5e01f2be63c4721f70f0de37cce664`  
		Last Modified: Tue, 25 Feb 2025 02:36:41 GMT  
		Size: 5.0 MB (4965040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d956a22b540177cbd138202006616690f9e9912ac958d12f095696d4945cd7d`  
		Last Modified: Tue, 25 Feb 2025 02:36:41 GMT  
		Size: 1.4 MB (1422152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41672cc18fb1ee7fc08de343b248fbfa39f5598769cba2824405217d86e52d4`  
		Last Modified: Tue, 25 Feb 2025 02:36:41 GMT  
		Size: 8.1 MB (8066261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bde7954adbd413058b66ba0317cd41f6bf207c3d1b37317799139dba3f201`  
		Last Modified: Tue, 25 Feb 2025 02:36:42 GMT  
		Size: 1.1 MB (1137181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168af9cf12dcf0a844a47628b319ed2ae691604241872b9fb01971b97ba798ca`  
		Last Modified: Tue, 25 Feb 2025 02:36:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e241aa85bf41bfd90887eb5e9c16f1f639b83787f1b5a02b183b1a82c9c972`  
		Last Modified: Tue, 25 Feb 2025 02:36:42 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d583c1b70095739ceff89060f12aec807a16d3d79b16c3eaed4b27f2f2576aee`  
		Last Modified: Tue, 25 Feb 2025 02:36:46 GMT  
		Size: 119.3 MB (119295189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630827bb6e6a31b4f836e0532fa321ffb90e2a0c370bfe38a729afd0ccbaff70`  
		Last Modified: Tue, 25 Feb 2025 02:36:43 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29db592fd4ba8b5ca167ab8ea56dd637237824ca8a1811efbe3709fe62c578c0`  
		Last Modified: Tue, 25 Feb 2025 02:36:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df922668932d0d72945468502964b16851ffd3c41daa9f35b7898e342a471339`  
		Last Modified: Tue, 25 Feb 2025 02:36:43 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943ac1f2accec6d7418cda8b7ea794d6f1fc8e95e8ca6d5339bf2a1e6aa8c601`  
		Last Modified: Tue, 25 Feb 2025 02:36:44 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0415e39288bb567ed6885cc8d2e42e1ee9396e4d26d44ff87f0a8108fcc2b437`  
		Last Modified: Tue, 25 Feb 2025 02:36:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:57370b399e30f8c09a19ecf11f1fdb4bdd2441cfbf791f76cc0d524f0de35e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a395b58b9dfc72a8272a9e9c070b80cd9bdde22402559202b003f79583ea39`

```dockerfile
```

-	Layers:
	-	`sha256:6bec5f1fd0a57d42eb31e0e1a371bbdd90386a5d00c3e67af8f1558c048a06c9`  
		Last Modified: Tue, 25 Feb 2025 02:36:41 GMT  
		Size: 5.8 MB (5815816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11c8bc6838c503747f1f33bc727963d4caf880307015c6be13ff0697a13ae605`  
		Last Modified: Tue, 25 Feb 2025 02:36:41 GMT  
		Size: 54.0 KB (54019 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:fe923047db6eea03ad82cf0a8f1f8043654049834889c882ca8ef2577029ff76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154090610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bf8423f562922638293109127e5652812b17475fd11836aa81e3395071e4c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
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
ENV PG_VERSION=16.8-1.pgdg120+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 01:38:47 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7719e8dd642635cc80cc6a9201e3e12b43c5f81b8b96b4826617eb3a26ef6296`  
		Last Modified: Tue, 04 Feb 2025 14:29:34 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb1203be53afacdadc0f86ebda1b96bdf67fe99f6d6b9312982859db9ddc62a`  
		Last Modified: Tue, 04 Feb 2025 14:29:34 GMT  
		Size: 4.5 MB (4475093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ad73e52814e3b5584157bc395cc6e78a6e29ae72deb1f0b28c57ea4a88b45`  
		Last Modified: Tue, 04 Feb 2025 14:29:34 GMT  
		Size: 1.3 MB (1333770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f690f3824ef93097d65c0de409702fe1686f77be8b24f9fad85c2958516e1aa5`  
		Last Modified: Tue, 04 Feb 2025 14:29:35 GMT  
		Size: 8.1 MB (8066470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc420e36068670a1196d49557b6cd53eee48327c745a919656afa4d3f2a1a2`  
		Last Modified: Tue, 04 Feb 2025 14:29:35 GMT  
		Size: 1.2 MB (1182594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bff00c1df4e776710c790789bb6291046ed640138fb8637f289fdbd789ac820`  
		Last Modified: Tue, 04 Feb 2025 14:29:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b8bad5a58592332fd97ab300c9375cabad82d5f47ff89fcfba0bd8319bda0e`  
		Last Modified: Tue, 04 Feb 2025 14:29:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacd32bdb8f8765b611b09d26717e72baa99d186b1d9f205572ea23dbbe0dd84`  
		Last Modified: Sat, 22 Feb 2025 03:00:40 GMT  
		Size: 110.5 MB (110525855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb00ef89a0039c2b35d291bf4e3105fd41ecf1a812109089e07ad16eed30d1d`  
		Last Modified: Sat, 22 Feb 2025 03:00:30 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcb90da538af3cd175817b15aa9d1da74b6048a89426e84572e28384cd7c3ae`  
		Last Modified: Sat, 22 Feb 2025 03:00:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaaea03cd04d739d152491de9347f11b2b3ae84e452ac64d86c47dee710dfb8`  
		Last Modified: Sat, 22 Feb 2025 03:00:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73484dd3396d2921cc28b2ba697ced56fbb9fb6c67925087066e542600bf966b`  
		Last Modified: Sat, 22 Feb 2025 03:00:31 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1683fa6670e745d2683372bb3b8bc463f5b83078872bb2cd98f559700ef827d5`  
		Last Modified: Sat, 22 Feb 2025 03:00:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:64ce3d2690ae825f0ee4e484395b6d3277739da2bfd65a50cfdba5234b4458b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 KB (53958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad4d1aea55a0c730e251eeceddc49cf98e5b644768dd896a7391d4ae14e18fd`

```dockerfile
```

-	Layers:
	-	`sha256:686a62675eb0f35d8c0e642010535e7ad13e7d9bc6373776cd4d46271339e72c`  
		Last Modified: Sat, 22 Feb 2025 03:00:30 GMT  
		Size: 54.0 KB (53958 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:ff4ffe8bdd13e65590c3457503ee7829599a61b63e420cb30195d5a78db190f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (167954552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec40d0722821c0a1eeb5b3cefef64c19926b1dfe861da1d90bddc2ed1b92859`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Feb 2025 19:44:40 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
ENV PG_VERSION=16.8-1.pgdg120+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac954bd36cb4d3caebe7e61de9d51f58c1ffaedc4cda3c904297558eab9ce36b`  
		Last Modified: Tue, 25 Feb 2025 03:58:02 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8e2ed2c480eb31e9a5576d38bceb6fa9dd377e634b7ff8b0f5d3cc42e7db6c`  
		Last Modified: Tue, 25 Feb 2025 03:58:03 GMT  
		Size: 5.4 MB (5368256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09570715ce0677b2b7b2e018987af73073b0122db22458a72f57b914a0874d42`  
		Last Modified: Tue, 25 Feb 2025 03:58:03 GMT  
		Size: 1.4 MB (1368690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed6fca48ebab6c7ac4a548551eca931bfac28e13a607ee9e398157384c1638f`  
		Last Modified: Tue, 25 Feb 2025 03:58:03 GMT  
		Size: 8.1 MB (8066406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bba706fadc2087d66a1bca0e5cdd71a9aa301cedcab29ddcd37ea8e2dbb363`  
		Last Modified: Tue, 25 Feb 2025 03:58:04 GMT  
		Size: 1.3 MB (1283536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d62b37b54dd01e35b1f6313a3012f7d1609ad004f64d8241b75a9466274b89b`  
		Last Modified: Tue, 25 Feb 2025 03:58:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfc2180e0627edc5acdad7d7376200cb70b92811ce71ff3c832e1f544695a8a`  
		Last Modified: Tue, 25 Feb 2025 03:58:04 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28765ec0c9a94a69cd809bbf9fe2f7120675cd29052b51badd3b21330ba2dcc8`  
		Last Modified: Tue, 25 Feb 2025 03:59:47 GMT  
		Size: 119.8 MB (119795111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2f268d58f14a71b08bbbb56d8076cf58bb5ece0bd8793d495aeb7e9873ba46`  
		Last Modified: Tue, 25 Feb 2025 03:59:43 GMT  
		Size: 9.9 KB (9917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5168bd4dcd6094a094544e833a9f31899c3afe257d565ba1d56703c90d6f8a85`  
		Last Modified: Tue, 25 Feb 2025 03:59:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1d93ec8f96e874838283163311aa822e30ac1f1bc54ad4fb8059fb5b22047e`  
		Last Modified: Tue, 25 Feb 2025 03:59:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be0cc3cef94fd24fe96fde8356839dafed1d0ffdf8f413700f884222c4bf4da`  
		Last Modified: Tue, 25 Feb 2025 03:59:44 GMT  
		Size: 5.4 KB (5414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791b5bdf9ad68dbfcf253601457a502afb1d28e6019b566d9198bdc43468f551`  
		Last Modified: Tue, 25 Feb 2025 03:59:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:465d0bff7a14447d93b33ea57b86aa94ccf2b369092ec44c5dd4d77acbd93ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5863238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a25f8bc6a50d029a1b7ee85c674520bc7f37d14ef17a800f6996884cac93835`

```dockerfile
```

-	Layers:
	-	`sha256:ecc6874b2def9489e8c76d6fd5454241bfe170ccf890eb3139d75eabc3eab22d`  
		Last Modified: Tue, 25 Feb 2025 03:59:43 GMT  
		Size: 5.8 MB (5809098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88bf0c451d86563b6d2031f8ade0d77567cc7eeea0b32136814d742dd8ea64bb`  
		Last Modified: Tue, 25 Feb 2025 03:59:43 GMT  
		Size: 54.1 KB (54140 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:c4a6f7a1df2f04669d2ffe61b8747f97e398734f85d83d878a34c2e6118c5ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164347929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7723f675beac7e380aad4a717c0357268d76143819043249bcf38390ecb56518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 20 Feb 2025 19:44:40 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
ENV PG_VERSION=16.8-1.pgdg120+1
# Thu, 20 Feb 2025 19:44:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c0aa600752d291a77bfc958eb9eb6772726703221cc4fcf99a44665fc1cfe`  
		Last Modified: Tue, 25 Feb 2025 03:42:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a63e50d66d5cd10e3a8c18df9c8befe4268834fd1eb1869ba5240c6e600beb9`  
		Last Modified: Tue, 25 Feb 2025 03:42:04 GMT  
		Size: 4.4 MB (4390981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b052f44a4679e17525e1bc75b685a791e2b73345c61054f1185f42b857d09e3`  
		Last Modified: Tue, 25 Feb 2025 03:42:04 GMT  
		Size: 1.4 MB (1412657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0c7a8a0744c5aecd4d8342daf0f3ff3cb5f530c3f956f740f475b3d2d3992c`  
		Last Modified: Tue, 25 Feb 2025 03:42:04 GMT  
		Size: 8.1 MB (8120431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed4ea1e6d4feccb2fc26d3befb3c8930e35940c91c70249901ef79b1afdda73`  
		Last Modified: Tue, 25 Feb 2025 03:42:05 GMT  
		Size: 1.1 MB (1096725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6c6185839c1a9d559d3638afcd2598ea4b67f1333615c69a77218deddc2bb6`  
		Last Modified: Tue, 25 Feb 2025 03:42:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bbb1611de92b6ac803ffcd04142e37784bd4e69d4ced471a3208040d73199a`  
		Last Modified: Tue, 25 Feb 2025 03:42:05 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829a21f1527adadb3660a042abe82eb6d5df2970414f5f2b0551bf82e46bfdee`  
		Last Modified: Tue, 25 Feb 2025 03:43:22 GMT  
		Size: 122.4 MB (122442058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b31694f450b1d9e856afc45735e3cd82e6e4098cec6cd0c7b085ee4d676453a`  
		Last Modified: Tue, 25 Feb 2025 03:43:19 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b575fd93d0704051b878cd2c46d8c4c69bfbba4aff40c53ea9f643b4e30177c`  
		Last Modified: Tue, 25 Feb 2025 03:43:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff57019ea46e4ca41c027d1c339c3b6d65e55b29ca79a0874fdbdaae4dd868e`  
		Last Modified: Tue, 25 Feb 2025 03:43:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e053d6841de1c890b23f1ee9240db1da33595710da3b7ce5601d1b5db3e252`  
		Last Modified: Tue, 25 Feb 2025 03:43:20 GMT  
		Size: 5.4 KB (5413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89e56919166a652ed9b517427a580c5d43ba54176927e8d37ac80a6b9911751`  
		Last Modified: Tue, 25 Feb 2025 03:43:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:463f4097c14a169baa28e9ae15c88f330e0035a0e6880d4ce1b8fe83c70bcf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6f529a2f75c374e5cd3003f42e1b676e5afa42206cdebed7f2c6e2d5822960`

```dockerfile
```

-	Layers:
	-	`sha256:14b1b2ddac167e4147554d9e98ac05cb99d7611ac56e0d95dc824af5e9fdf421`  
		Last Modified: Tue, 25 Feb 2025 03:43:19 GMT  
		Size: 5.8 MB (5801132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba52429ddb7d75ff0e2ddec4c2d598ad4865710781d765de6412f8f9e660cbac`  
		Last Modified: Tue, 25 Feb 2025 03:43:19 GMT  
		Size: 54.1 KB (54074 bytes)  
		MIME: application/vnd.in-toto+json
