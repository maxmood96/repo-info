## `postgres:15-trixie`

```console
$ docker pull postgres@sha256:76f2c4482aad1d614f25a729a0011974aea9277c2adba1e25a6ff0dd5f0ae82a
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:15-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:d9bd24fd2cf9681006b14f93d7bad1eca6e00220692151ad05c68fcc1d6c56c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158293607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18f711b0debf507cb7444a8cab1048ed560953c24d14babb29b02ee6db9dae8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1352279344c6078b55aaeeda1957e9972504efec3666c541c6889fe23672f`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56e480b4c77181e0e4674ade9ef5cb6f56edfb744b0c15d20492b36adf0f703`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 6.4 MB (6436561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a421874e67d98391e745984a6334d3fec4b0198f157f6c92c8a30acdc8b4d073`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 1.5 MB (1454199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3001e6144e88e05d39b7c8361f163b676af3e126f906a73beb3f40789079e2`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 8.2 MB (8203598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad84dee38c6102d7bb73982b464909e174ef29762a4d5324f6d0541ef3ba6ae3`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 1.3 MB (1311359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812f8629a6fe23067feeb54a98a609e673f5e7959c810c0daa374c03c47a0c6d`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d796a572482446c2e649a921dcc91496916425c50b7cca36a3d85c8f035b4af5`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82a6003f51710e6f0d9798798ba3f445972faa50f929db66c1a8c01a9197d7a`  
		Last Modified: Fri, 05 Sep 2025 21:47:10 GMT  
		Size: 111.1 MB (111093878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446859ca5fb2138835221cf19f904c751f10f02f8e5bc9a02c5ca24506b50b75`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ded31e88e046928aed2ca7cae5c33de1cd89b8cb0fc26397aa3705073acd2491`  
		Last Modified: Fri, 05 Sep 2025 21:46:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0802bcb2968a2f3006521207034557905b5e846777211bb58aff35e9fc11bf`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80316f1f66f0dcd55a82ea209c4ce8d8b6b65a2237a515ac0d6481d08596e12`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc522b0e64b5f3e26aaf293fc492c595ee299b8d333d1046e472e572fdad21aa`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:a8193c81466b0bfd58f8392f4ba8f8347d9a6d14648f57482c1d7e2f9199881d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5777524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02d09aa077189c4f746b7bf0d983a975ad782c68a7ef94280b077651079a64d`

```dockerfile
```

-	Layers:
	-	`sha256:43c2b48c2851875bdf2bcd25fb4a57e31dbe75b840b614d7f9ee1e99dcb80cd5`  
		Last Modified: Fri, 05 Sep 2025 23:09:17 GMT  
		Size: 5.7 MB (5723617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7ec143a4cdcd5b714d16db577a5ff7393be2d2a2075f3b55e98d69eca2d3cc`  
		Last Modified: Fri, 05 Sep 2025 23:09:23 GMT  
		Size: 53.9 KB (53907 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:ecfd6b375eb10c817007e5dae86abb7bf13c34966b376b43a667c3a5192058ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152355224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e36a91ac7df285c81b1e19ff713e3ece640fe13a877fdfe0a229078d4062fbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4432fb1dae6dea3ff069bcf6b78616dbaae82227906fd5a0f78837295e0ead`  
		Last Modified: Fri, 05 Sep 2025 22:04:52 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6a7ed26360d23db69f3f4593bc4c7ab1d41f411cc5c91ca56072a07ef64e52`  
		Last Modified: Fri, 05 Sep 2025 22:04:53 GMT  
		Size: 5.9 MB (5928839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25bf61ee6e8f27d20c86a12237a8a52ad22d2103ed159aa4c2a6d37fb82b49d`  
		Last Modified: Fri, 05 Sep 2025 22:04:53 GMT  
		Size: 1.4 MB (1431788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7750201c4bb6a5efedc32f0854ceaebaaa927aaa816fa9e3ef39f5e7c3ae5b4`  
		Last Modified: Fri, 05 Sep 2025 22:04:53 GMT  
		Size: 8.2 MB (8203996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b50d6a3756e7e237f63e13fb3738c1bfcf5f8ab27af34a52d83cb6992f9af5`  
		Last Modified: Fri, 05 Sep 2025 22:04:53 GMT  
		Size: 1.3 MB (1317029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3770071959326969b8ec25932fd50468428af18e1049dff3580a28dcdcf37ca`  
		Last Modified: Fri, 05 Sep 2025 22:04:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458c52382735229a6cb319e67144bd9a355936b0f73c4bdfb06c2d4490633709`  
		Last Modified: Fri, 05 Sep 2025 22:04:54 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cdcb017d59340cca6cb76741b2dc594943e96606996a79df591c710650d287`  
		Last Modified: Fri, 05 Sep 2025 22:04:57 GMT  
		Size: 107.5 MB (107511145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192717fa38e3e585c74d0ba799fedc4125c30c8afa37cb5a1ab7ffdbe5256ec1`  
		Last Modified: Fri, 05 Sep 2025 22:04:49 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b228960c5717e2fbad13c46dd4930159dde39d22e7561b22e47a3a1e571773`  
		Last Modified: Fri, 05 Sep 2025 22:04:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1980baff4236d4f6df377bc7723ec139915aa0be587b1744ed28841bd4e61182`  
		Last Modified: Fri, 05 Sep 2025 22:04:50 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbd97f42ff22aa272d1ffb206de104a88e93af7b7c143cc5dfb8491f3bea88f`  
		Last Modified: Fri, 05 Sep 2025 22:04:50 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2eb7c4997047694bc8b986a9a20055c94d175b5f64d269f34a0b8d3987a31e5`  
		Last Modified: Fri, 05 Sep 2025 22:04:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:8f58806fc6363aa4c2aa935af6fc33f52b2d4e5b4d07e2cc7b99de542bc3ac5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e936854ad8c6ee25866792707245e7afca922d55603038583ea0bdbdd1b1eb`

```dockerfile
```

-	Layers:
	-	`sha256:547259b5e888b6bbdeddd50f8547e79773bcddf6069502a1b6f5a1625be7aa74`  
		Last Modified: Fri, 05 Sep 2025 23:09:30 GMT  
		Size: 5.7 MB (5740223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c9bddf8f5187cb3cf0dfb6f9bd0322a736859eabb035061906722dc1cc34a9a`  
		Last Modified: Fri, 05 Sep 2025 23:09:31 GMT  
		Size: 54.1 KB (54130 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b401a8de2101732e3e6aba869d16572b016517fcd1df6685af89cd7524971dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147439653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e35492440b5086bbd1648fb990675cb2518cc0bca7da06a636878f96e66ad2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87af847ad561e7057496d9640070c580e8f70dfea34ef61e963cf1e3b42d5928`  
		Last Modified: Fri, 05 Sep 2025 22:23:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a96947e1d060196050ca4a70e56bf03fa4c5ac45080d372001fc401301dfce`  
		Last Modified: Fri, 05 Sep 2025 22:23:07 GMT  
		Size: 5.5 MB (5496689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a2d25eac78a8af3f251352aaa1078c2aa1bf4349887c3e13cedba782f7400d`  
		Last Modified: Fri, 05 Sep 2025 22:23:07 GMT  
		Size: 1.4 MB (1421039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaabb9c6eb2e80deddd6c911a05ba39e1f2d0586b3b6d3b3d1a1954aa946208`  
		Last Modified: Fri, 05 Sep 2025 22:23:08 GMT  
		Size: 8.2 MB (8203801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60f1c118d5bd73916b13ec8fcbde6c2947fb92122db067c77b49b154d58e9b4`  
		Last Modified: Fri, 05 Sep 2025 22:23:07 GMT  
		Size: 1.2 MB (1172359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36475229b990e8363c6c70afbe13e650d80c0227c90f437679185146027d6cd3`  
		Last Modified: Fri, 05 Sep 2025 22:23:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1798a5e39d39041fe6974345f30aa5a80613c4b88a72eb20ad3c980af78f231`  
		Last Modified: Fri, 05 Sep 2025 22:23:07 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0473272d97341f04cd86f89ef3437158780fc7f60bd5afa1ea2bfdd8b44a6b1`  
		Last Modified: Fri, 05 Sep 2025 22:23:16 GMT  
		Size: 104.9 MB (104917543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5e645186e9e8380e140221f2cd8392dbf39c056a4b41b9f39402c3c9329838`  
		Last Modified: Fri, 05 Sep 2025 22:23:07 GMT  
		Size: 9.9 KB (9893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa12a7c8633954ce07d2e3fe0d7811a581e4f042f83987ae4a8810c09255eef5`  
		Last Modified: Fri, 05 Sep 2025 22:23:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2d314c418c8e3c7a8ea2a178cdec9a341f34674d0c9670e411f6cf30b2c353`  
		Last Modified: Fri, 05 Sep 2025 22:23:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaea25e4f667160ddf3ebd0af3ca0bb2f5f032b0397973ab697213bdcf80ce3b`  
		Last Modified: Fri, 05 Sep 2025 22:23:10 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7aff9531cfa820496207beaf9822d939b2c133d9e430045226ddaba908fbb7`  
		Last Modified: Fri, 05 Sep 2025 22:23:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:5f183f13e76eced2539be58a8da249a052862bc410457143e0f93bbef3987922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5793666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a65fb7fe9fe36ca1e440f1e273d383ae801ae6bf25f3930fec0a1eb8226a86`

```dockerfile
```

-	Layers:
	-	`sha256:2384ee0d5fbb97003028139f71e7bee2ea232dd9f112ac58cb71c7eaf494d9b9`  
		Last Modified: Fri, 05 Sep 2025 23:10:06 GMT  
		Size: 5.7 MB (5739536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fef36e83931f0897528865887d07f8fe024b7fce8cb4a4a6d70f5f71470431`  
		Last Modified: Fri, 05 Sep 2025 23:10:07 GMT  
		Size: 54.1 KB (54130 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:72d12311f0b3c801bf16a08d574a537bbd2ef1d4ab435dbfb1582e5539e0ef2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156898878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c144c7f3cfc11d0f85286a4a58caf89725f44a1580e588ee1687d468e29639e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65338726d39673c2dc2b289745145b3e731087553d0ce2b26a2ca08530649c2`  
		Last Modified: Fri, 05 Sep 2025 22:02:47 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b55b037667fe8732cc3e57290284653470c1249fca67c9f9f38e9957ef39a1b`  
		Last Modified: Fri, 05 Sep 2025 22:02:47 GMT  
		Size: 6.2 MB (6231904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ee7cdc68c0d048423c481d37226bc389286f428053d24ad2b4a08559b0dcd1`  
		Last Modified: Fri, 05 Sep 2025 22:02:49 GMT  
		Size: 1.4 MB (1386092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d7ce4e2ab820cd4342d1ccfb7712a328ac75350db9a39d06984ab4a3e7669a`  
		Last Modified: Fri, 05 Sep 2025 22:02:49 GMT  
		Size: 8.2 MB (8203760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30419b849281d1257b615d720ef9a93256298a81eff3bb1026337c1e7d20566f`  
		Last Modified: Fri, 05 Sep 2025 22:02:49 GMT  
		Size: 1.2 MB (1220310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba092c4623d8e129a6dd733cb5312ec9ad3c6dca6d46ef520006597f0b86740`  
		Last Modified: Fri, 05 Sep 2025 22:02:49 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1340fecc8ed7454757514ff9a41ca5408497919462b383186f3df97a1316d036`  
		Last Modified: Fri, 05 Sep 2025 22:02:49 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53569a1813d2c7d6cce1c0e3495a0b3577b3e5b0fff31322b92fe9e6fa62d431`  
		Last Modified: Fri, 05 Sep 2025 22:14:54 GMT  
		Size: 109.7 MB (109700046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8557cb39cec19c380fb9e742ad01aba1a168a8950ff56a43bd57832b8c6b5d75`  
		Last Modified: Fri, 05 Sep 2025 22:14:35 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ec1b229971b0213e2d5f84556965ee24b7638556dd38c0ad1181da84a6be56`  
		Last Modified: Fri, 05 Sep 2025 22:14:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff162e456ef28845f2c1bbd27aed899381f9f19fa848ecc2575049d26025939`  
		Last Modified: Fri, 05 Sep 2025 22:14:35 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092b7ef06fc0a8ab0b364b2e5ecc9e25df06ccd0bad34327f1e6f961d70269a1`  
		Last Modified: Fri, 05 Sep 2025 22:14:37 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119d8ae5a6bddee94cf2285584a20fe750f444351eee24a3710f029f8a83ca1c`  
		Last Modified: Fri, 05 Sep 2025 22:14:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:c9d4aefd9bb3f16af374cbca3a542ffe61d40ead16d096826b68469a80535d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5784143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d6bfc9bcc1ac5f41041cab2678f0e5612226372f13c66e73b1f1cf82c76c66`

```dockerfile
```

-	Layers:
	-	`sha256:60295d1ce91deb3c8ef7a633568cf9b8a591da78f544e83c9994f59dcc1c30ca`  
		Last Modified: Fri, 05 Sep 2025 23:09:41 GMT  
		Size: 5.7 MB (5729967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b48b23c453ee0269925777371ff765289dbe02ab73131d50d307c07a06ff5d94`  
		Last Modified: Fri, 05 Sep 2025 23:09:42 GMT  
		Size: 54.2 KB (54176 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; 386

```console
$ docker pull postgres@sha256:cb9784550b232ac696ca2c54f1c99a89d02a8fff14cdd30ed3e4852efa3078e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.4 MB (167421356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9741b47b9e50a6518ae3159421fda595d3b47d77405133de3b11f92631a1f4f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491b5a760cba5ffc0f59ce45f1ac86a44a6bed04a62a3ad1b087fea18f28bf17`  
		Last Modified: Fri, 05 Sep 2025 21:59:46 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54571bc067c310d18948c3f211c19030ede5cd296cd6fbfc6d06ffad0b7293a`  
		Last Modified: Fri, 05 Sep 2025 21:59:47 GMT  
		Size: 6.6 MB (6629458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbdd1f91fdff47bb39ebcb66b72abfe680f4c164a9ea344d87210d972271bdc`  
		Last Modified: Fri, 05 Sep 2025 21:59:46 GMT  
		Size: 1.4 MB (1429214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed51f992e77fbe651e7045e19c6705ea61d7beec2c6a9b694fa2d2376d85fccc`  
		Last Modified: Fri, 05 Sep 2025 21:59:51 GMT  
		Size: 8.2 MB (8203776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b819e839006701aac67fa4ea1756879d9551c94233d28c96be18445200e5c44`  
		Last Modified: Fri, 05 Sep 2025 21:59:46 GMT  
		Size: 1.3 MB (1308029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c3cfd0c66b0c36ca242366dbe6d5e0bced975d0e7e7d4dcada7f90eff14af5`  
		Last Modified: Fri, 05 Sep 2025 21:59:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ae10d52686553f3fd3b256e3d9f1fdb9960e956c4f4bc50c5d7dfb3d382ac`  
		Last Modified: Fri, 05 Sep 2025 21:59:46 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a5142dc86f31acc3d0abbd818b16b7aae48a64ee283700fc0b3fe8e80f70aa`  
		Last Modified: Fri, 05 Sep 2025 21:59:57 GMT  
		Size: 118.5 MB (118540770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0550bfac0e8a03033b93f985f446f30d998b039f861496c70df26f8815821b37`  
		Last Modified: Fri, 05 Sep 2025 21:59:46 GMT  
		Size: 9.9 KB (9887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf33b3f005859996c2a5c866751ce85c416a1dcb56807e12c34201b5a9b946f`  
		Last Modified: Fri, 05 Sep 2025 21:59:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b8d44eef462d94efa647b24c0b09bf62953d87b67ab1108cf19b2071c78eac`  
		Last Modified: Fri, 05 Sep 2025 21:59:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa49035c162c949d4ca433a3cadab88166e55f32b1909c5da73d67a85541a530`  
		Last Modified: Fri, 05 Sep 2025 21:59:46 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045eb9e5c4ec653586844a68172e1d33918b4ad9ba4e3d8810efed60dbdb2715`  
		Last Modified: Fri, 05 Sep 2025 21:59:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:fdb97e8c739bfea9f22470b327e78d94e50571af40a99404cbc381967f884fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ae2fea2276ec81e70e2c7b0f57dd026dfccd78d449f506cefd4c1746a70439`

```dockerfile
```

-	Layers:
	-	`sha256:40b16f87c8e74e89c9f574f953ef0f14d85d5930bd815dec2596e5a284b24970`  
		Last Modified: Fri, 05 Sep 2025 23:09:47 GMT  
		Size: 5.7 MB (5739104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90da494dcdf923624bd2f5249c39045a53b218e52e1aed09ca5433034248cc22`  
		Last Modified: Fri, 05 Sep 2025 23:09:48 GMT  
		Size: 53.9 KB (53853 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:ecacae87ff87968d3f983027f6eae497c82c9d6544f9bc58fa7c0c44acdf04fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170480752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa0d49c57a983aa09257f149b153db5e040c56b2f67c7032f8460f0b6c691e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378e9c083817980020ca293d7055813e697201f5abd1e3b4ab0ac0e028983152`  
		Last Modified: Fri, 05 Sep 2025 22:14:01 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86884dbf4081c813effebfbfa2888412b9a747631b2996530db0fbdd607e82bb`  
		Last Modified: Fri, 05 Sep 2025 22:14:03 GMT  
		Size: 7.1 MB (7075770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b78ced3863ddbbe50f6bd293e4489a166ba1c2d173b06f377b8b33224c34034`  
		Last Modified: Fri, 05 Sep 2025 22:14:01 GMT  
		Size: 1.4 MB (1375561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa92e082819b054be2bb905be0f738f1d33f14fd129352b513d7c537fe753e4`  
		Last Modified: Fri, 05 Sep 2025 22:14:02 GMT  
		Size: 8.2 MB (8203798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5177f4f02613ea03dfaa95326e54a8883d36635c89ee4e0b9671ca37a28b2f0e`  
		Last Modified: Fri, 05 Sep 2025 22:14:01 GMT  
		Size: 1.4 MB (1394678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f11c8cbdddaba4aa3eecdae07cca7dc840bb6d6fca3e1c387df42d143da8c3`  
		Last Modified: Fri, 05 Sep 2025 22:14:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8542ef5d360bf8d211020331f72113d4d375b283ea3994ba3d181aea06473f`  
		Last Modified: Fri, 05 Sep 2025 22:14:03 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32f9f882a042cbe9efa06d7a84b5b587d6553c4214bb8ad764b750bb18cafdb`  
		Last Modified: Fri, 05 Sep 2025 22:36:16 GMT  
		Size: 118.8 MB (118816004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7c0b315255d7d037341355fa4eb27e4999e50a1203ddacf27565a4e0e5af78`  
		Last Modified: Fri, 05 Sep 2025 22:36:02 GMT  
		Size: 9.9 KB (9882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d29a3bd80338a4f247f039af7374924414874a64dbd9ad6a098002c943166b`  
		Last Modified: Fri, 05 Sep 2025 22:36:02 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934b0dccea736bf5ffe4951657435f09a53e743c880d27ba8372a1ed82da7f66`  
		Last Modified: Fri, 05 Sep 2025 22:36:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbde48d3c68dd76d4bbeee0391468fc00bd4ad4a6634bfac0ca965a9047dec8`  
		Last Modified: Fri, 05 Sep 2025 22:36:02 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e89c2cfce81e52bf0d83df4f14c332c61274a113fe07820c3fba1828903832a`  
		Last Modified: Fri, 05 Sep 2025 22:36:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:576e01c3639a0ca555807cb76de2135fc004219483ad02aff233e09bbce87168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5784223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e8de830d8cb5b89276f0f311c7f33e73d2954155a4308ddca06972323997a7`

```dockerfile
```

-	Layers:
	-	`sha256:5caa1d68c3bdb275faf81469498197d9c4f8860dcdbe4c751e5fab3bfd09084a`  
		Last Modified: Fri, 05 Sep 2025 23:10:20 GMT  
		Size: 5.7 MB (5730250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b267bdeb0af7906a5e8d2a26147b2ebb6c15589e491fd047b9dd8736056877`  
		Last Modified: Fri, 05 Sep 2025 23:10:21 GMT  
		Size: 54.0 KB (53973 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:1e3dbcae7f703676c421d6f4b167ff5fa138cc4e6daf08e03b453e714b61970c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90341159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811da3e776611d54d97970f571e22c5944404d2a5f38aeb336f6ae0b2874eec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b0a0fa649236068d28b6d885c7775ab23b869ac6db4e99721c07dca1c50ea4`  
		Last Modified: Thu, 14 Aug 2025 06:16:19 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c311e323901b74143f4ee2884d975ecd86ed8fd237bb96964cf2be91acf129`  
		Last Modified: Thu, 14 Aug 2025 06:16:22 GMT  
		Size: 6.3 MB (6291226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1859f38dc7ac3a34086a8ca21cede764ff373b6b790b7ab2455d25147f08f2c0`  
		Last Modified: Thu, 14 Aug 2025 06:16:24 GMT  
		Size: 1.4 MB (1424731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4263087a9cf57f147ffe4441d83c3d579e380f2b9d478856eafc78d9cc3d071d`  
		Last Modified: Thu, 14 Aug 2025 06:16:27 GMT  
		Size: 8.2 MB (8203378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2955bd53e05478f76ceb79d6badbe79f640f15e6c74ce3d8e259997b9b615ed`  
		Last Modified: Thu, 14 Aug 2025 06:16:29 GMT  
		Size: 1.4 MB (1402099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51ed4fe98001ce8f4bb9728bc68f534f9afa7456ad3875b5c3ded0936775b5d`  
		Last Modified: Thu, 14 Aug 2025 06:16:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e6cca965baba9c5eeea11d99ae81468cb3309fdc4e3408aea55d986b94410`  
		Last Modified: Thu, 14 Aug 2025 06:16:33 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab93f9cd86ab3e2e936fce1e2886ae2709c554f15af0587e694664f2cce24d5`  
		Last Modified: Sat, 16 Aug 2025 20:10:38 GMT  
		Size: 44.7 MB (44727380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401fa73e7ff7f6f04b7289a7498d6b683c1aaf017659a24259d5b77b57e0c446`  
		Last Modified: Sat, 16 Aug 2025 20:10:32 GMT  
		Size: 9.9 KB (9888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761117dbafde4e3557a85162b0f69a37e7f96c1550c52829cf7991bae306999c`  
		Last Modified: Sat, 16 Aug 2025 20:10:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ea8ff076c26dd46a683cea7c71fe2d87691b5a5b5dd9ec8112b38f0bbbb118`  
		Last Modified: Sat, 16 Aug 2025 20:10:32 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0040a1335428e1427cd2a84b0cea5e12dd8e842c7b749a35f0133beac0553b85`  
		Last Modified: Sat, 16 Aug 2025 20:10:33 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc234476df25d2ce6dd00c5022e526f8f8a6311b580d3713c0cb5d92b72ac6b5`  
		Last Modified: Sat, 16 Aug 2025 20:10:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ab45c6b4dba51123cc883ec1a5ec88baa19a5b427c9ccf0ed46ac89484f90bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61db38e72e2092863c67b22ed25418d384e92efa924e4d4a8d60f9acc439e848`

```dockerfile
```

-	Layers:
	-	`sha256:896a3d0564f5e793a0b445ced2177ae88a930579271534451748d4748f1ff1c9`  
		Last Modified: Sat, 16 Aug 2025 23:08:15 GMT  
		Size: 5.1 MB (5101577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa50060bbe89fe6e4b9112b190ae5831a33ce6fcbf4b7c70a43ee41a9a8d3cfb`  
		Last Modified: Sat, 16 Aug 2025 23:08:16 GMT  
		Size: 54.0 KB (53972 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:fc4c188ddb7c6fe5bea825b7b6b7e8187d6fc13dd18382dd62198e62cb45a2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.9 MB (172859106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a4217eaf03de351df9960f759a6ce88b41e3cfdc5a482ce2ce1b430d256c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14-1.pgdg13+1
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25aeb0c2b2f8a403705aaa83b95622da6bd82510bb53cdca36e1272cbd0ce1f`  
		Last Modified: Wed, 13 Aug 2025 01:43:34 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accebcf53414b9dbc815739458083b2a6f98a6550be094ea88b262aa973a97c1`  
		Last Modified: Wed, 13 Aug 2025 01:43:37 GMT  
		Size: 6.4 MB (6408735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8013a86d3b1526e8549f316b857c57782e17fbeb29e3cc082c40db534c04c72`  
		Last Modified: Wed, 13 Aug 2025 01:43:35 GMT  
		Size: 1.4 MB (1420337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c121b022a27f99e36f3ec7756fc794d10502feedd80ffe25571261315a321ff`  
		Last Modified: Wed, 13 Aug 2025 01:43:36 GMT  
		Size: 8.3 MB (8258719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ea94d1cb2c41e7377a60b32002839fec6b81f9ac5c0562df38de557467c43c`  
		Last Modified: Wed, 13 Aug 2025 01:43:35 GMT  
		Size: 1.4 MB (1397988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b56b31422bd8bace2d32e04b3b5bb8ee7424c4986ab5775be804b7a6c9dea05`  
		Last Modified: Wed, 13 Aug 2025 01:43:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c798199c95340171b328eea53ffec29853d8de362608bce1809335c565563d`  
		Last Modified: Wed, 13 Aug 2025 01:43:35 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9b73be04dbc6772af9653f1521c710110e746e274d8c9fc1f74dc1cbd2736d`  
		Last Modified: Thu, 14 Aug 2025 21:32:40 GMT  
		Size: 125.5 MB (125519551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07e77b5dc7ee83cca6ade2c7ea416954eb4c142c33cc94b0ba543fd4f7c88e2`  
		Last Modified: Thu, 14 Aug 2025 21:32:32 GMT  
		Size: 9.9 KB (9885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7646c02215ec4dedac4a2ac4674c1efd831ff52eada0e64031e1d219c172c4e`  
		Last Modified: Thu, 14 Aug 2025 21:32:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e48825d865563b0b7e983b198600797c6e545bf2ca131990413f6190b387359`  
		Last Modified: Thu, 14 Aug 2025 21:32:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551c9e7aced58a5837a6be5353066a9cdc38741a276bb355a3ae9a18e982114b`  
		Last Modified: Thu, 14 Aug 2025 21:32:33 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738b6118aaf1029e186de2525af5ffe44b7a74bda83f7c2e5956ead5fcbe4dee`  
		Last Modified: Thu, 14 Aug 2025 21:32:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:c90fc7384241e2fe6bb2af61f6d0e7187477e7763894ba3531a84f8f74eb0652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae4c7bed0f0ed16b9726efc653e07086a6cab6a2f7482054d90ccb698dd51ab`

```dockerfile
```

-	Layers:
	-	`sha256:9aec8b6a8c49172c0b8c488e973b864a10ac752cccb48a0ffcc05b8027f785e1`  
		Last Modified: Thu, 14 Aug 2025 23:10:40 GMT  
		Size: 5.7 MB (5740192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bab07e5b362d7931013c1cf5fbbb90b70ce1f49e9d51bf5a97d1aba1115be3a`  
		Last Modified: Thu, 14 Aug 2025 23:10:41 GMT  
		Size: 53.9 KB (53912 bytes)  
		MIME: application/vnd.in-toto+json
