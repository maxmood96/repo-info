## `postgres:17-trixie`

```console
$ docker pull postgres@sha256:19488ac7059d8259960d046e27c56995cfb8b2272459fc30b78efd6f03e0ef3d
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

### `postgres:17-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:9c1534cbf839ec70409508a874f4c02bf4739de2f32f77efe080eef1cfd34bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161213518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f76768a0c956d6e9bddbcdb3c2be7fd9fd45ee6174a26873f8219fccbad65d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:44 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:45:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:57 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:45:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:46:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:46:01 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:46:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:46:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:46:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:46:05 GMT
ENV PG_MAJOR=17
# Wed, 24 Jun 2026 01:46:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 24 Jun 2026 01:46:05 GMT
ENV PG_VERSION=17.10-1.pgdg13+1
# Wed, 24 Jun 2026 01:46:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:46:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:46:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:46:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 01:46:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 01:46:18 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 01:46:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:46:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:46:18 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:46:18 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:46:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38152547e42eafff29a4055892075fa261a8992960e8c2db61e7a9743d31ea3f`  
		Last Modified: Wed, 24 Jun 2026 01:46:39 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d062ec8fea4fe50dc382020465afe29a68171273a4e13ed10fd2479b3c157d41`  
		Last Modified: Wed, 24 Jun 2026 01:46:39 GMT  
		Size: 6.4 MB (6443065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3d59e883a0a5aaf2e566d086e652edd0dda70aec91d3e870c153cfa346bdf`  
		Last Modified: Wed, 24 Jun 2026 01:46:39 GMT  
		Size: 1.3 MB (1256767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534fe585f4dc58ea1899f07886ae10ebb589bccb7da9adaf7e701c887b5b4d82`  
		Last Modified: Wed, 24 Jun 2026 01:46:39 GMT  
		Size: 8.2 MB (8203907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4891673997178e3592eac84e52965d8eaa5fb3f0f686cd57bc10778e71d6c2fe`  
		Last Modified: Wed, 24 Jun 2026 01:46:40 GMT  
		Size: 1.3 MB (1311656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4568948a1fd5ef8286c5083f0f64c2b0fffc87f843fa878f5b7f07dbede8a7a1`  
		Last Modified: Wed, 24 Jun 2026 01:46:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4839f71271cd25bbc9b3471084725ba90a84e46c75e93fc39c4ffc2fe037eca4`  
		Last Modified: Wed, 24 Jun 2026 01:46:40 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bfd0bf3c7ac81d22e3e59391b6ac740c226922713a9c0aea70c251d808232d`  
		Last Modified: Wed, 24 Jun 2026 01:46:43 GMT  
		Size: 114.2 MB (114191311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb634303aa40cad2e6a22156c4f21d8ae1a29d819b8e43fbf548790a2e02941`  
		Last Modified: Wed, 24 Jun 2026 01:46:41 GMT  
		Size: 10.4 KB (10397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444edd01ecc141cc3a38660bec426633eabfd843cd1ffc0dbdcbb80fe16c59ff`  
		Last Modified: Wed, 24 Jun 2026 01:46:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03771fe89717aa2fe1a5784fe47ff6e7a4639c55eb4a361e10ff58c192c47be4`  
		Last Modified: Wed, 24 Jun 2026 01:46:42 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9339eae16e526a2ff6737b61ad82947c9fb86eb5520466f505abcc171a495eaf`  
		Last Modified: Wed, 24 Jun 2026 01:46:42 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11962e37fe65cc563b3185b01ec7052c5500c41dc470cbe7fd18a3ee8f52d35`  
		Last Modified: Wed, 24 Jun 2026 01:46:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:c99dacd699de5a1b84c208e6cef83ccebbcc585eac14f243c19272dd3be1173a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5780697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ad85d0649cf9bae6fee34023f77d416490dc6ed176049712dcc95f1c04692c`

```dockerfile
```

-	Layers:
	-	`sha256:e840c0037fa486079e0c1fcfce23428a5faabc06085a2edd346179a315b12fde`  
		Last Modified: Wed, 24 Jun 2026 01:46:39 GMT  
		Size: 5.7 MB (5726828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb957384b1e80148dadfb9a444cdf18b647694404182644a70c4c9b3c89ad827`  
		Last Modified: Wed, 24 Jun 2026 01:46:39 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:848933d01c6ac2caff5100b4841956e43bd05d370b0d28f99624aa8c52c92df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155238066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b713b40feafbc54d5fdcf5ccc496514199d1e14ce25bb25903bc07221d1f888`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:47:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:47:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:47:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:47:28 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:47:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:47:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:35 GMT
ENV PG_MAJOR=17
# Thu, 11 Jun 2026 00:47:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 11 Jun 2026 00:47:35 GMT
ENV PG_VERSION=17.10-1.pgdg13+1
# Thu, 11 Jun 2026 01:04:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:04:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:04:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:04:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:04:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:04:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:04:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:04:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:04:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:04:57 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:04:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:04:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737a85241c9b5aeb96ef71cfaef6adbd9aa823612dda6bed0579a93678d5ad51`  
		Last Modified: Thu, 11 Jun 2026 01:05:15 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c399cb5ce37e9b1f707ad1afc129b33cf0e4aca88343dcca753807b9833ac1b3`  
		Last Modified: Thu, 11 Jun 2026 01:05:16 GMT  
		Size: 5.9 MB (5932390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e244dd8068512c488f86e50ac67b2b1a572f2cce3c78fb08878f268a8fd81a18`  
		Last Modified: Thu, 11 Jun 2026 01:05:16 GMT  
		Size: 1.2 MB (1227550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e918f38f9b286d810ea2322053b531c2f65784b5d6e14ce604b7960603302f`  
		Last Modified: Thu, 11 Jun 2026 01:05:16 GMT  
		Size: 8.2 MB (8204336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bda4475b2c61c0aa9acbf32bc6bf2f8f5575a52fb9fd1378beca8f38cb3db6c`  
		Last Modified: Thu, 11 Jun 2026 01:05:17 GMT  
		Size: 1.3 MB (1317326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0365e9fa058a4d968471291859f0e3feeb50b40b0e84f411bd73f96c4acf56`  
		Last Modified: Thu, 11 Jun 2026 01:05:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a0b25a347ab23b053520e4f4d1d8e0afe495dcf1621c09b3339262800cbf89`  
		Last Modified: Thu, 11 Jun 2026 01:05:17 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5208bfb23273c317ab412c3c53fe7a3e6343816eee76fb2818104805509905e0`  
		Last Modified: Thu, 11 Jun 2026 01:05:20 GMT  
		Size: 110.6 MB (110575878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a188a469875da082f26a6984857eabd95e564a59d237be7f311daae3437631`  
		Last Modified: Thu, 11 Jun 2026 01:05:18 GMT  
		Size: 10.4 KB (10385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5f8180489ebb09326e47317397bacde221938a626f8f0bfc3ca75bb077fec6`  
		Last Modified: Thu, 11 Jun 2026 01:05:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d0f672fa5e47672c95b110ea19453fcfbffa743533bd523a4ec8b261b114ed`  
		Last Modified: Thu, 11 Jun 2026 01:05:19 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d07e2162571add6fd2ded126968caaa423fc88ea7b1fe36bc398c816fb4d6fc`  
		Last Modified: Thu, 11 Jun 2026 01:05:20 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71993b3e92af3dbcc92d649a0a23b437a920746b225a6e1806532e0f4cfd0e14`  
		Last Modified: Thu, 11 Jun 2026 01:05:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:e93c1be67a714e316b4a714be8ac4190038fe91101ef9f813f36887307e50e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23163bcf130caefe4eb67fa362c5a8f5af16c2c6bbb6f3bc9e6e53baf6d4bc55`

```dockerfile
```

-	Layers:
	-	`sha256:e4030e667d7450c56c8af6c36a4873acf40342a8c4e28da73ff71bd6f1c26f61`  
		Last Modified: Thu, 11 Jun 2026 01:05:16 GMT  
		Size: 5.7 MB (5741748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1ed1c270758f6d8064260720138db8dceeb339ff95e32750d4e625df71ba3f`  
		Last Modified: Thu, 11 Jun 2026 01:05:15 GMT  
		Size: 54.1 KB (54091 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:d9e5c2533434ec5b9113ee99911311d8fb19695e03745e89951930e443b80b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150246713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1c110a2624ddf50c92fddff11c80286e327af23855b00b20d1414527ebeab6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:59:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:59:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:59:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:59:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:59:59 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:59:59 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 01:00:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:00:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 01:00:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 01:00:05 GMT
ENV PG_MAJOR=17
# Thu, 11 Jun 2026 01:00:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 11 Jun 2026 01:00:05 GMT
ENV PG_VERSION=17.10-1.pgdg13+1
# Thu, 11 Jun 2026 01:16:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:16:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:16:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:16:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:16:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:16:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:16:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:16:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:16:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:16:12 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:16:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:16:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a2b57683b3a61c72ae7abdb462e655d1f39fa56de06ec96af6e93d66903c20`  
		Last Modified: Thu, 11 Jun 2026 01:16:30 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c055e879882b90aa32579f6c49ba1bb1787760bf681d9a8ec8b97db2936ab238`  
		Last Modified: Thu, 11 Jun 2026 01:16:31 GMT  
		Size: 5.5 MB (5497319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc52d5934c4fcc948224fef0b7367fab4e1f551d60c745c7eff484e56d37d1db`  
		Last Modified: Thu, 11 Jun 2026 01:16:30 GMT  
		Size: 1.2 MB (1222439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0a48399957932d6943c83c62585926cd1c5ce6161468906b3741f8c80f01fa`  
		Last Modified: Thu, 11 Jun 2026 01:16:31 GMT  
		Size: 8.2 MB (8204126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad42941183642ec488212ffbd73403b92ce4a2b26903c14f785a6f2d862f252`  
		Last Modified: Thu, 11 Jun 2026 01:16:32 GMT  
		Size: 1.2 MB (1172658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7190d347ef8703e1ea140aacc0f35d4cb530f3292eef7023e3de1f604564c2f7`  
		Last Modified: Thu, 11 Jun 2026 01:16:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c68b04a52c643feb1ddd36ab2c5cedfbe78bbf02bf1a035b2a46439a4fa6b52`  
		Last Modified: Thu, 11 Jun 2026 01:16:32 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef2266c70bf07add8256fd175dc228f595274f33c4ca33aa085f90fe4370335`  
		Last Modified: Thu, 11 Jun 2026 01:16:35 GMT  
		Size: 107.9 MB (107917758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96e64706f5a02b6c6c1aff7276a00970489329dfe3d72dcbed4e8083502c1f2`  
		Last Modified: Thu, 11 Jun 2026 01:16:33 GMT  
		Size: 10.4 KB (10408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216585d44265c84e6b464dd4e8354610b6a2a0609bdab46c05fdca93d39536cc`  
		Last Modified: Thu, 11 Jun 2026 01:16:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9af59bc18bedcab2ccec5d6aa9a7d0147f212a52e0a02f9a19b052d9558cd`  
		Last Modified: Thu, 11 Jun 2026 01:16:34 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b97d8aee2a9e2e026479cfd6522624f07d25d572122bd01c5731c5f98d5265`  
		Last Modified: Thu, 11 Jun 2026 01:16:34 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0506cb5978361d7ac5d2caa87dd2620cb0959c4eb745d6e2d6f99c3fbb96ffd7`  
		Last Modified: Thu, 11 Jun 2026 01:16:35 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:156ddc8c34d9a179c50843f592e965a673164c886360feb80696f9a8071a1493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff45fe3f28ee5395f837a354a3d528af1fa8c3945ac6974a7d9aa4729bafe684`

```dockerfile
```

-	Layers:
	-	`sha256:e6e8b5df9a7a191d0d3a0ec8da1e0e1cf51ffd9dbbe8f16718cedfb2f07a1a60`  
		Last Modified: Thu, 11 Jun 2026 01:16:31 GMT  
		Size: 5.7 MB (5741053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ae06d2e433e9c5c448b963048de2602ae843b5e6e812d387ce758f5a2dd46af`  
		Last Modified: Thu, 11 Jun 2026 01:16:30 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:056a2afd8e4817d5912fd10e3b17192302baa5d41d961da7cbb23a69a73e359a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159847389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbfb5afa81030db7bed0a6ab12ec8a1a10f6545e260b342fb9289c09ad4c4a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:35:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:35:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:33 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:35:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:35:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:35:39 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:35:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:35:43 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:35:43 GMT
ENV PG_MAJOR=17
# Wed, 24 Jun 2026 01:35:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 24 Jun 2026 01:35:43 GMT
ENV PG_VERSION=17.10-1.pgdg13+1
# Wed, 24 Jun 2026 01:35:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:35:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:35:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:35:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 01:35:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 01:35:58 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 01:35:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:35:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:58 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:35:58 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:35:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c57974956d5322d77db25fe16e1db8790cca472805431e879cfdaec12472a05`  
		Last Modified: Wed, 24 Jun 2026 01:36:16 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9eb1c2190a16eb7b1ee0961971a5b1fbf5a54d4618328c8afd58fdf9299ad7e`  
		Last Modified: Wed, 24 Jun 2026 01:36:17 GMT  
		Size: 6.2 MB (6235160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eac3c7663a3aa9defbf0fa8ff4bf344c693a815e58095c55066d360008741f4`  
		Last Modified: Wed, 24 Jun 2026 01:36:17 GMT  
		Size: 1.2 MB (1209567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c5d99632339b847fa752feb3fa0ee96e700336c8123e3754cd5688af33c504`  
		Last Modified: Wed, 24 Jun 2026 01:36:17 GMT  
		Size: 8.2 MB (8204066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83885a9468720f3e0ad19f2398bac5320b47ecaaab10ba0bbbd6686b2977d186`  
		Last Modified: Wed, 24 Jun 2026 01:36:18 GMT  
		Size: 1.2 MB (1220594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec5ce846f7d28a91a8bd7a0cfd6c09ded3ca89b1c41e3ee61d60f620a746e7`  
		Last Modified: Wed, 24 Jun 2026 01:36:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29279dfaf3ca369e2a46673ca1bc8cc498afd725007da9b8071aa8567b685f56`  
		Last Modified: Wed, 24 Jun 2026 01:36:18 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b6e96c3d9855f02ecbac4d5b9d6acdc94ff8445d9bcbe3f045f5f01fc4c417`  
		Last Modified: Wed, 24 Jun 2026 01:36:22 GMT  
		Size: 112.8 MB (112808052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b71c1a0fa46c9d8ec3ec2c00e031fce91c73235d1a911caad0b35afd97f94a8`  
		Last Modified: Wed, 24 Jun 2026 01:36:19 GMT  
		Size: 10.4 KB (10397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bedd7fa67273118a4bf24d76023bd0319ee6a1e940462aeda5d90f89f51714`  
		Last Modified: Wed, 24 Jun 2026 01:36:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6eb2215c57dd356aae33a25cb02b689884fb7a1cd802d39d615fdd0581fa9a`  
		Last Modified: Wed, 24 Jun 2026 01:36:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2b63c7de9f48f2082fe10ac3dfcdab1f76442520cb7701b01565d0e254bf1e`  
		Last Modified: Wed, 24 Jun 2026 01:36:20 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8fe43dbe20ba14b62140bfa1348de12337d40b997edd8ea0ddd6fb87d584f9`  
		Last Modified: Wed, 24 Jun 2026 01:36:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:dcd82e2c73707e6b3f61c4dbd5db47c6ed76be8bbb1148beb020e1ee220a2095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5787304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ac1b129433a4763e979a8160f051bc9b709db73b2a5687bc1dc07f3a580dd3`

```dockerfile
```

-	Layers:
	-	`sha256:9278039528180ff91c7b9012838ea5c988e44b29f7f2cdace9192e83e7481dab`  
		Last Modified: Wed, 24 Jun 2026 01:36:17 GMT  
		Size: 5.7 MB (5733166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44aef2e68a6326fc951c8ae02179467544054bad82644a0063fe56347a9d6142`  
		Last Modified: Wed, 24 Jun 2026 01:36:17 GMT  
		Size: 54.1 KB (54138 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; 386

```console
$ docker pull postgres@sha256:d0fad169a26a3112e550ee7d1f9df2c6caf840da492a117b1434ada77ccc10c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170390291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c284b08c29e2b0ce8b91ff73c184313a40adc58ebf30a1f5f264403718b464ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:31:31 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:31:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:31:45 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:31:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:31:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:31:50 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:31:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:31:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:31:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:31:54 GMT
ENV PG_MAJOR=17
# Wed, 24 Jun 2026 01:31:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 24 Jun 2026 01:31:54 GMT
ENV PG_VERSION=17.10-1.pgdg13+1
# Wed, 24 Jun 2026 01:42:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:42:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:42:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:42:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 01:42:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 01:42:57 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 01:42:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:42:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:42:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:57 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:42:57 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:42:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417789ae0880441e5d722860b0e536695c5650e9bda0ecae1c5f31929752b91f`  
		Last Modified: Wed, 24 Jun 2026 01:43:16 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a476f6c1ee301ce4a7a127d57fb8ffb7b3e18105106948e04d86cddcd547193`  
		Last Modified: Wed, 24 Jun 2026 01:43:17 GMT  
		Size: 6.6 MB (6631415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4280b0aeaf84cf82f90ec38c3612b916c5e18a04cc8fd376be22abbdab64378`  
		Last Modified: Wed, 24 Jun 2026 01:43:16 GMT  
		Size: 1.2 MB (1225859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cef13a0fc00da561f69d8add740d469cc6f2a3bdd11d2778a7a8f8b16485983`  
		Last Modified: Wed, 24 Jun 2026 01:43:17 GMT  
		Size: 8.2 MB (8204098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be5a602ab92bc774ea62b07dc977e2ede6b1412fec550724155d4f08f135ec1`  
		Last Modified: Wed, 24 Jun 2026 01:43:18 GMT  
		Size: 1.3 MB (1308291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd3405905dd81936ebb6586e503a272d793637cd4545f817f526bbd0e439db0`  
		Last Modified: Wed, 24 Jun 2026 01:43:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29478d9b8814ded54106f610e8760b05297456441390b88ba33f82312169b227`  
		Last Modified: Wed, 24 Jun 2026 01:43:18 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453357475c4f703fe13ca75c3106490bd86e411fcb44e0ab6b84489be8d2bfa8`  
		Last Modified: Wed, 24 Jun 2026 01:43:21 GMT  
		Size: 121.7 MB (121698022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cd41a704e1dc5f52de5fc238913c454c97969fa75807c7f9d715a005565682`  
		Last Modified: Wed, 24 Jun 2026 01:43:19 GMT  
		Size: 10.4 KB (10394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd285a633b4d38c412bacdc6c9a93631120208ab45371fea127260f440da791`  
		Last Modified: Wed, 24 Jun 2026 01:43:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e78fcfaa212674026bbbcd0fd363561a7366c46c58acee7be4bd27d4271ade`  
		Last Modified: Wed, 24 Jun 2026 01:43:19 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c9515bf5717794d94629411cc22023ddd8756293ffc34def7e7e9959fd8c56`  
		Last Modified: Wed, 24 Jun 2026 01:43:20 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175a7b66efdd8ca04e484086d6e7dff2e9b1a0a306b9eb4287308e0d260e9dd`  
		Last Modified: Wed, 24 Jun 2026 01:43:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:4a4623b974086ddbaa566530fc961237e4073add46666a30892df751c2eb8d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5794456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2df1bbcbe6efa3e1824d6bf7f1f42f812b7579812e37ec6380a48ea9739650b`

```dockerfile
```

-	Layers:
	-	`sha256:4b2f1716d26768ab62b2d79c65f89b0a5765cb0d90df9335f3e4c82e0c527a7e`  
		Last Modified: Wed, 24 Jun 2026 01:43:16 GMT  
		Size: 5.7 MB (5740641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f190db795e009f0754cd5736655f1720fa7339f0f6da8a5437964ad563488f7`  
		Last Modified: Wed, 24 Jun 2026 01:43:16 GMT  
		Size: 53.8 KB (53815 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:57c76a6c027a3e2ed9b9b9bb1769441fe7a3107c9ef1e77fe43a89c828264739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.6 MB (173565922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783f5229599bd78161656455b92ca2704956325acbe7efa6fa97fc6a26c0ee81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:22:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 04:22:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:22:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 04:22:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 04:22:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 04:22:57 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 04:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:23:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 04:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 04:23:06 GMT
ENV PG_MAJOR=17
# Thu, 11 Jun 2026 04:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 11 Jun 2026 04:23:06 GMT
ENV PG_VERSION=17.10-1.pgdg13+1
# Thu, 11 Jun 2026 04:28:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 04:28:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 04:28:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 04:28:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 04:28:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 04:28:03 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 04:28:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:28:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 04:28:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:28:04 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 04:28:04 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 04:28:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e93abe7480356a6fc8ce6943b71e051b601733a1b3eec3b84b51ba066f7ebb`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e50b953d51df1ad75aa8423fe4c0b925ff04cb0f00fc9bf7d832470c0113811`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 7.1 MB (7076806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b50b5ff568aaa483897ee3a1d850dd075b9e6655d095d44de11470d6f8fc009`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 1.2 MB (1214789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd8cddd4d91d1f798bf8f04a08fd19f0142e2c39271c68c2550b9e9fd0cc832`  
		Last Modified: Thu, 11 Jun 2026 04:24:35 GMT  
		Size: 8.2 MB (8204074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bda34c5d2b40061a1e23c1b4ffa3a2ae3eaf4b9cb20d75b9698f949074d325`  
		Last Modified: Thu, 11 Jun 2026 04:24:36 GMT  
		Size: 1.4 MB (1394935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7053b7edc10475c2c4219fcbafcdaa68460b254fc0f37b9ce94c177fb20f36a2`  
		Last Modified: Thu, 11 Jun 2026 04:24:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc5c991fdba4277fa6991ebe8b974a0fa349af5e7830ce228f1bfac146a2248`  
		Last Modified: Thu, 11 Jun 2026 04:24:36 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9355c5c50ace1dd2ccc6db25b94976ffef733323179ade448bde8972ca27a28`  
		Last Modified: Thu, 11 Jun 2026 04:28:45 GMT  
		Size: 122.0 MB (122047578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71789f78af03d5b64d75ddc85628fa061d91a9dc7ae8f353587d2de2acd9e127`  
		Last Modified: Thu, 11 Jun 2026 04:28:42 GMT  
		Size: 10.4 KB (10397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8a7b9e7e5c76ca415b6a860554e0d5176c387510439e1f6e11b9f3d4e8d9c7`  
		Last Modified: Thu, 11 Jun 2026 04:28:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfb3318f7cd3383164844c455cfec0b92d738cb88586c6f47feb31280fcbdf5`  
		Last Modified: Thu, 11 Jun 2026 04:28:42 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc0973de0bb401827a0c8d7eced6d17cd82118e1ec32640a55e84192a4198a3`  
		Last Modified: Thu, 11 Jun 2026 04:28:43 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf37a08220e574bfc0f0210257406367ff0372023134a2f5ec16fbb6b7c32cc`  
		Last Modified: Thu, 11 Jun 2026 04:28:43 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:b94c02aec1ae36ae5e2c93ad807082eb94bc27ea1f6443704f6dec7623f5a51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5787376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054c17d0fdedaa7e0daf6beb9a154a0a66684082059af461a2f180002666dd17`

```dockerfile
```

-	Layers:
	-	`sha256:ab98d277cb5fa81d493f58323477a6c7485618c7092cf8a781546d824e70b2fa`  
		Last Modified: Thu, 11 Jun 2026 04:28:42 GMT  
		Size: 5.7 MB (5733441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbd69eba7edeab8f4618574c998b848b70e934ae371a4e49689a0d1fa3645b47`  
		Last Modified: Thu, 11 Jun 2026 04:28:42 GMT  
		Size: 53.9 KB (53935 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:ff0c7ff38f1b1a8bc7f4c19db3a100e8bf923bcba48f91a14890ce92f5306e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92261363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38a8a1f5e7b2cbf256b6da84a44ac6126ea666ce726baab98abe8e71ac8c60f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 13:36:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 12 Jun 2026 13:37:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 13:38:18 GMT
ENV GOSU_VERSION=1.19
# Fri, 12 Jun 2026 13:38:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 12 Jun 2026 13:39:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 12 Jun 2026 13:39:20 GMT
ENV LANG=en_US.utf8
# Fri, 12 Jun 2026 13:40:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 13:40:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 12 Jun 2026 13:40:03 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 12 Jun 2026 13:40:03 GMT
ENV PG_MAJOR=17
# Fri, 12 Jun 2026 13:40:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Fri, 12 Jun 2026 13:40:03 GMT
ENV PG_VERSION=17.10-1.pgdg13+1
# Fri, 12 Jun 2026 19:29:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 12 Jun 2026 19:29:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 12 Jun 2026 19:29:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 12 Jun 2026 19:29:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 12 Jun 2026 19:29:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 12 Jun 2026 19:29:56 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 12 Jun 2026 19:29:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 19:29:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 12 Jun 2026 19:29:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 19:29:57 GMT
STOPSIGNAL SIGINT
# Fri, 12 Jun 2026 19:29:57 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 12 Jun 2026 19:29:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c604ade0b6a80a5d5169b84e100e842d24b4f67918a5ac906f1c0d0aa5022a4`  
		Last Modified: Fri, 12 Jun 2026 17:23:03 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dac76a2994d0f440b17af07b6f9dbe3f84c615964fea39af40f8814bb2c8c79`  
		Last Modified: Fri, 12 Jun 2026 17:23:06 GMT  
		Size: 6.3 MB (6292958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac31f6db0842376127148b967b363ed1a2b8f1452eb2a5a5bc939e086a2307`  
		Last Modified: Fri, 12 Jun 2026 17:23:04 GMT  
		Size: 1.2 MB (1202050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4134483cfc20739a930db23479f6b6a303bc538a1de2d4ef6eb0b28eb74716cd`  
		Last Modified: Fri, 12 Jun 2026 17:23:07 GMT  
		Size: 8.2 MB (8203611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f8468820d8c6fdb4e7c65d561c4b485db7b70d63334ffa82b2187b15ac0b96`  
		Last Modified: Fri, 12 Jun 2026 17:23:06 GMT  
		Size: 1.4 MB (1402404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc6a806752ca47859a97d4d1635b4c0bcd5cbd0816107b22327591a2caf65df`  
		Last Modified: Fri, 12 Jun 2026 17:23:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d42f665a394411a573dd31dde673ad6c3582108dce44b1dbb27b63adcffbc49`  
		Last Modified: Fri, 12 Jun 2026 17:23:07 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ef854aee200dfd1dddf405b1c20ad995223ff34c72f00a514cc94aed27637f`  
		Last Modified: Fri, 12 Jun 2026 19:32:31 GMT  
		Size: 46.9 MB (46856623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe5fb75e9ad00e1502537b61c26832f4b64194a88378258c5950ae3507b0069`  
		Last Modified: Fri, 12 Jun 2026 19:32:23 GMT  
		Size: 10.4 KB (10404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346c19d507466a3b3fa23b9e31f88c3db47342bfa55e95238101f0cc655003f4`  
		Last Modified: Fri, 12 Jun 2026 19:32:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084940c5c7b21cee5ba85f3cb93edba37e7a8d8475121885998f59465649781f`  
		Last Modified: Fri, 12 Jun 2026 19:32:23 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a10db367c9162bb4e5b00e8d8033e7baa567d3b5a4c7bde1f9f617d751d727`  
		Last Modified: Fri, 12 Jun 2026 19:32:24 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb001afa7b939a618a9e7359cfef23c1ca1b4d0afd6616a3173809928b3cd45`  
		Last Modified: Fri, 12 Jun 2026 19:32:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:092acb2d63c211c63d73ecc9cfc4f36250d607f557224ee17fbb640947733964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260d21ce2a7e94a35731d0ea82f6b0650a15910451a42c2c7e12b4c8a6efb61d`

```dockerfile
```

-	Layers:
	-	`sha256:6a1afeeca4fd7a15414218bb5528a4b7f903602d8ad9a2cf2567f77726518244`  
		Last Modified: Fri, 12 Jun 2026 19:32:24 GMT  
		Size: 5.1 MB (5084106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a07efe2df338d1c306d783842bc8cdebeb88d1ceb5b56a493d86e23b66b6ed`  
		Last Modified: Fri, 12 Jun 2026 19:32:23 GMT  
		Size: 53.9 KB (53929 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:8210e778b8d2fda02633185a5c8f4a89ed87d46834dbe8af6d563690cd2b547c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175779230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eaf74283f1528a2d84af2c0fab6bb78028b663531cb90c91b0ca621760215d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:57:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:58:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:58:12 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:58:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:58:19 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:58:19 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:58:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:58:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:58:24 GMT
ENV PG_MAJOR=17
# Wed, 24 Jun 2026 01:58:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Wed, 24 Jun 2026 01:58:24 GMT
ENV PG_VERSION=17.10-1.pgdg13+1
# Wed, 24 Jun 2026 02:26:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 02:26:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 02:26:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 02:26:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 02:26:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 02:26:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 02:26:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:26:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 02:26:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:26:28 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 02:26:28 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 02:26:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f8b3edc75b49ced11dab27f4148cad3479e0ca4d1bef3a3372749607386048`  
		Last Modified: Wed, 24 Jun 2026 02:13:10 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9af1a36d970a9aa144153569a33418a335c9f9fa39e21a0cc4822586b42480`  
		Last Modified: Wed, 24 Jun 2026 02:13:11 GMT  
		Size: 6.4 MB (6408505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67240597dd615f7661bbea5c29258b345c44ac1ab6bb6353553953f634b3b31c`  
		Last Modified: Wed, 24 Jun 2026 02:13:10 GMT  
		Size: 1.2 MB (1230274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe0ebce0cd5e64ec821f7bc63f955b565a014c44a3e15ddbf8fb5de3b298b72`  
		Last Modified: Wed, 24 Jun 2026 02:13:11 GMT  
		Size: 8.3 MB (8258957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b62f6fa5bb2b55a8c5023e16a41664043d46f4d418a482eb291c58f249ad3f7`  
		Last Modified: Wed, 24 Jun 2026 02:13:12 GMT  
		Size: 1.4 MB (1398189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e3b23c8c098994d89f5ec00fd029fe0265f484d55050145dd15dc6dc11ad6d`  
		Last Modified: Wed, 24 Jun 2026 02:13:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5a3c3534096eaaed44cd33e5dc26c06d3585042dbe09953547256135f24b66`  
		Last Modified: Wed, 24 Jun 2026 02:13:12 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2c6688b112af54374b31af2a7906f4c68337cce73c3960328b467ebf002bff`  
		Last Modified: Wed, 24 Jun 2026 02:27:00 GMT  
		Size: 128.6 MB (128610521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d51ab742d4c522db86e383ab73cc8113108ea2c2d18237e25dd12611e8a55d9`  
		Last Modified: Wed, 24 Jun 2026 02:26:58 GMT  
		Size: 10.4 KB (10396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2494138e0c4fc9af43531efd31ac6c5ec37004830cdb9ffcaa9cdd7c32df7db`  
		Last Modified: Wed, 24 Jun 2026 02:26:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64350f4581c13f59f45f98e40c7e669a2325702e72d72bb66e3bb8184325516`  
		Last Modified: Wed, 24 Jun 2026 02:26:58 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b047bd6661390c5a0d13bce5483dfa5cbf6e729e8482ff090eac6ecde3a79108`  
		Last Modified: Wed, 24 Jun 2026 02:26:59 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84738f35296028b5753a490f0c0050e2fa736ebd39dd7e772a4fb2a56e9c5db`  
		Last Modified: Wed, 24 Jun 2026 02:26:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:715f6abf86194d00968e898a14becba01ea32093e73cbed3703544ddf39f9d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5795648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5192fb949161b0538d9567ab634d7acd0b54bafc38d54477fc26ddae8fa17540`

```dockerfile
```

-	Layers:
	-	`sha256:84461378a75f76c88afac848e03e9499cb0132cd95feec132bdefd3d2689f1bf`  
		Last Modified: Wed, 24 Jun 2026 02:26:58 GMT  
		Size: 5.7 MB (5741779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354679fcffdd8da8ec824d29a21b4e797838d00c10815d5c7ed102f5a3434243`  
		Last Modified: Wed, 24 Jun 2026 02:26:58 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json
