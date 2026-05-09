## `postgres:16-trixie`

```console
$ docker pull postgres@sha256:972eeb4e0a5fee4c3046cf868896719227e845aa9e38ff79a353efb3b2b2c10a
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

### `postgres:16-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:3102b2114b39383b61fa194e5929734c72a56ce366dbb391509b1f07aef10f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160133768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ebf09eb01b02bb9904972705248217baeaed03e2a0a7ed24a77740b0aee98c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:33:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:33:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:33:39 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:33:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:33:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:33:44 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:33:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:33:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:33:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:33:48 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 19:33:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 19:33:48 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Fri, 08 May 2026 19:34:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:34:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:34:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:34:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 19:34:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 19:34:01 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 19:34:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:34:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:34:01 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:34:01 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:34:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a683cffcdc0136b539df1300f44790972530bd31131a6d7c3b61f1225750a0`  
		Last Modified: Fri, 08 May 2026 19:34:21 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6f5b1d4fcc7a7e9d2c9cf436a540a5652b30a1a2206681b2b3d68fb488ebd`  
		Last Modified: Fri, 08 May 2026 19:34:22 GMT  
		Size: 6.4 MB (6441174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f810f97521bf3e8f49a7983a08a08284807a51649baa76760f447f47a86f27`  
		Last Modified: Fri, 08 May 2026 19:34:22 GMT  
		Size: 1.3 MB (1256753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c7b001f7c185a25d8d6e6593598dc17b0b6555f1d9be4c6b4a45aef67d5d0f`  
		Last Modified: Fri, 08 May 2026 19:34:22 GMT  
		Size: 8.2 MB (8203807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bd933b3504c1aadaa9c0c723ff41f9c29d6a52d06ea2576d0357e0557e0134`  
		Last Modified: Fri, 08 May 2026 19:34:23 GMT  
		Size: 1.3 MB (1311657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd786e9d2d8807a4db58e3905117d0ac882919d8dfa6dc17f5550711d52db42`  
		Last Modified: Fri, 08 May 2026 19:34:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538b1755faee8ed9e4ba73415d6d2331282e952a5841ad2a9a6d067e56dddd23`  
		Last Modified: Fri, 08 May 2026 19:34:23 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f64d703d8929b401984d5cabd1e42bfd97de46b51b2f13bda6167ab3105195`  
		Last Modified: Fri, 08 May 2026 19:34:26 GMT  
		Size: 113.1 MB (113119080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5321ae1fd2784292944155ad26341c69f12a41539a1f9a5fcfa228e291e77d8`  
		Last Modified: Fri, 08 May 2026 19:34:24 GMT  
		Size: 10.1 KB (10068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ece4c1ed352286f3018b7fc7003b48549f30c50f46066749f281d9aaae83c35`  
		Last Modified: Fri, 08 May 2026 19:34:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec732245c890ff11e62f90a519bf8ffc6ec92e9ad2188090532534500dbebd3a`  
		Last Modified: Fri, 08 May 2026 19:34:25 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40701225891c385428ec5018b9cfea7dcdbaa73dd140b03ccf123d330de2559`  
		Last Modified: Fri, 08 May 2026 19:34:25 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b67bd603bd81ab194f3d96803aefacdb5fa72b5e36950b569df2399b72e0df`  
		Last Modified: Fri, 08 May 2026 19:34:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:efa15bcde0ec2fb9f0c6b617f0406b5bf3184d78995169689094caaa92b3c881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0dad9f960aa26732f55aadd6a75f58be38b332869f3286b5013893a8edef43`

```dockerfile
```

-	Layers:
	-	`sha256:b197e6b67948591895ecc360708937c36eefab2b6c17fb7551a03ce4e30767ab`  
		Last Modified: Fri, 08 May 2026 19:34:22 GMT  
		Size: 5.7 MB (5708762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09397148c9c2013eb5c2127974c2846db9224041a97ef7c7a21dea2d708ca521`  
		Last Modified: Fri, 08 May 2026 19:34:21 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:6515d2741756c4e4e0ee5fe5278d3743df344996b0c97f012c6bc790113e5e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154168899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b9e4fe8e65d4ba51a54d5936b7fdf26e5ecaeb25646ab3b3189a4d96eeac87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:41:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 20:41:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:41:23 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 20:41:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 20:41:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 20:41:31 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 20:41:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:41:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 20:41:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 20:41:38 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 20:41:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 20:41:38 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Fri, 08 May 2026 20:57:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 20:57:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 20:57:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 20:57:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 20:57:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 20:57:42 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 20:57:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:57:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 20:57:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:57:42 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 20:57:42 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 20:57:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac06c31c1ba1e9749a6d7d9b97985ed10609e56520df49ccfd0c7844ca424bb1`  
		Last Modified: Fri, 08 May 2026 20:58:00 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b52a8de7b20e1d16bf1f982f1ab1fc8ac3c7333b9bc6e06920abb5be0b77467`  
		Last Modified: Fri, 08 May 2026 20:58:01 GMT  
		Size: 5.9 MB (5932503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbf54c61d94f5a7651466af5c37b8ae1cf3b694434c97704369e7bc505c4a17`  
		Last Modified: Fri, 08 May 2026 20:58:01 GMT  
		Size: 1.2 MB (1227549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee90f9f5da0cf78cf02eba70d081a64b07d9c05016ede87f94b297ee3299b271`  
		Last Modified: Fri, 08 May 2026 20:58:01 GMT  
		Size: 8.2 MB (8204287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ddb2608e2f5b551c5b7d10a0208e155b6a96e3078ffff37867b748985ac800`  
		Last Modified: Fri, 08 May 2026 20:58:02 GMT  
		Size: 1.3 MB (1317337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1afe2b24d3ea07dcb12d6175eda937b4285ee1d7773c4e8422931069ea17262`  
		Last Modified: Fri, 08 May 2026 20:58:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1833186633243abf77c6ca56bc07a1f2103b357ba8764b91486134ad4141be50`  
		Last Modified: Fri, 08 May 2026 20:58:03 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2367d7b59609fda9691109742a81e44a7fa0c2d6db9261647dcf3d6899bb5e0`  
		Last Modified: Fri, 08 May 2026 20:58:05 GMT  
		Size: 109.5 MB (109517945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54977256514ad0191f8795d0d7f2af2bfaa07eed1c6a13ff4290af5b45bcffb5`  
		Last Modified: Fri, 08 May 2026 20:58:03 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f8d7f9f125047d20a44da53d4321dbdeb4f2e6eb763b4e15a0993d8a645a57`  
		Last Modified: Fri, 08 May 2026 20:58:03 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eefb9951c3216d72f5d9acbb1445c4f4ce427bb891047f85125a7cf210dddb`  
		Last Modified: Fri, 08 May 2026 20:58:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696fe5263726467241fc6fd9ba801504ecc5d5611f3e99fdd8e2096b8885a7a2`  
		Last Modified: Fri, 08 May 2026 20:58:04 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e8fa6e4d412e38be342d99e60170b4004ccdec717ffc61fabc6c6d684ff274`  
		Last Modified: Fri, 08 May 2026 20:58:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:6b243b87410d1fdd0e3dc336bb71ce7cff3796f5bca948332c3609dfa7033524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d305c323b12be631904d6b8c6c290b05163f4aa588dde52104536f6b9639df3`

```dockerfile
```

-	Layers:
	-	`sha256:7b8a575b3d627a3619eb4704d4af8300376a9829e1508551a41e55cce2383ca5`  
		Last Modified: Fri, 08 May 2026 20:58:01 GMT  
		Size: 5.7 MB (5725400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9acec29a853c622ec0edec4c27826eb1b056efbc2712b4aea25c1ed50b5f698a`  
		Last Modified: Fri, 08 May 2026 20:58:00 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e773787e96efdd15c1d5fdcd2e6368ba538fede91528fb2753cf62c3cc304404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149215098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4018398ffd4354670e991cff2aa7f628fa073b2eb55076d058f2b1323dec110d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:28:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:28:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:29:01 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:29:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:29:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:29:08 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:29:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:29:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:29:14 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:29:14 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 19:29:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 19:29:14 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Fri, 08 May 2026 19:44:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:44:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:44:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:44:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 19:44:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 19:44:14 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 19:44:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:44:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:44:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:44:14 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:44:14 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:44:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55702235c3d77e40e234fae1ce5552ed4961d42af5f4347313e03f80098b08`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d458330aded6707bf4907b522680079886845bfa55367adb3478aa40ea9072`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 5.5 MB (5496604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59cdb631c2f309e7f0fd2dcedfba95232bacd15bc96f17e2716362c3b054840`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 1.2 MB (1222393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41dc83562353d7964e11f6174edc1c3821914eea9229f1423636c9a5d3dc1a3f`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 8.2 MB (8204042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9189b55bcced559c79c773826c7e1c0351b2a910902a94a633ecca9af6e08a`  
		Last Modified: Fri, 08 May 2026 19:44:34 GMT  
		Size: 1.2 MB (1172617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fea6c3ca3b865f0bb5076272d56aa14cc32124f7b219725a9f4e04c76fb4824`  
		Last Modified: Fri, 08 May 2026 19:44:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f992ece7f9d72757d0d71972a6c634eaa68fe97f784175b098aeff2cc92c25`  
		Last Modified: Fri, 08 May 2026 19:44:34 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be564d0b22bd97efbcea7eff5e62de1c433834ae402363927b79a969f3c548f`  
		Last Modified: Fri, 08 May 2026 19:44:37 GMT  
		Size: 106.9 MB (106883443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ff0c1cd44acddde802bcc5f83178b20ca07f23a77cbcb9aa5584d705c583b7`  
		Last Modified: Fri, 08 May 2026 19:44:35 GMT  
		Size: 10.1 KB (10078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149c7215f6a11c48bc882c95fa809296ee7586a09ecc47d5023d34bfc2aa5f90`  
		Last Modified: Fri, 08 May 2026 19:44:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71acff943ae29cba614a684d74e6b9bc466b9924f2a70a8477f4e2bcd7b00d7`  
		Last Modified: Fri, 08 May 2026 19:44:35 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c89be77b7ba139b418a6eddd27d4e466cc7628cd2ef9603883e0c3bc5565a8a`  
		Last Modified: Fri, 08 May 2026 19:44:36 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd36ada1811e67d9a89ba568bc04c0f9b7b4a90cfcf96eddfd9a655666a80fa`  
		Last Modified: Fri, 08 May 2026 19:44:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:c2cc0266e3d7244ddf8433fdabca273a406e295462a521047230bd6e87d51fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27469b2028e51a186ecbc4f7b48def16654f71d99c461ab4e1db458ade881556`

```dockerfile
```

-	Layers:
	-	`sha256:11f507e469eac7b0b0f30c5c1c879edc0eb949cf2b32bc8a1e6a0a29b8fc361f`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 5.7 MB (5724705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ffa86a48fe7ad38f7eafd4daf3e305c6508e52a0517805c4b12db807055bca8`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:bf738fa93668ee69ca247db4d98830fcc9b7e486257096adf793fa7836b5f076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158758663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c5619d18061cf239b35bc620208f4dc82317f976417a5abf8e551c82b31e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:34:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:34:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:19 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:34:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:34:25 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:34:25 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:34:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:34:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:34:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:34:29 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 19:34:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 19:34:29 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Fri, 08 May 2026 19:34:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:34:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:34:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:34:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 19:34:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 19:34:42 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 19:34:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:34:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:34:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:34:42 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:34:42 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:34:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f7fa48ee5e996adf1a741df9a1f238d601a8166f1b0178d674b94714613fe2`  
		Last Modified: Fri, 08 May 2026 19:35:01 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e64b3f10962cdc507f98bc6434118f22ea2cc2d158dd88050692390c8a6438`  
		Last Modified: Fri, 08 May 2026 19:35:01 GMT  
		Size: 6.2 MB (6234088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fa92807c5961f2cd6a5e9ae76dd434bb1ce67ebf3490e2ee505b649403d5c0`  
		Last Modified: Fri, 08 May 2026 19:35:01 GMT  
		Size: 1.2 MB (1209595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0bf2a24c283581da5ffe7f2e30f54e393cf310f4b0840d5e8d974d33955a9c`  
		Last Modified: Fri, 08 May 2026 19:35:02 GMT  
		Size: 8.2 MB (8204011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48292863d45df8a0f19e112542a010cb4ad7d79c95cb352908c14573847c949e`  
		Last Modified: Fri, 08 May 2026 19:35:02 GMT  
		Size: 1.2 MB (1220618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a8233221f246666a8fc23f10d9a56bea0201d0a76e8443c042512336885d77`  
		Last Modified: Fri, 08 May 2026 19:35:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa678aab6edcb8d6d77c633365b93b2556f12b6704d7d8e619b4256eea248f1`  
		Last Modified: Fri, 08 May 2026 19:35:02 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd6009319fbecf7e6668f8e1f50fbce7c8df7b407979918c342ffc909d5ac1`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 111.7 MB (111725625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13da09e550ab983e46110629b862d993134c6af1a9e961b0c75bf2580d20d8ea`  
		Last Modified: Fri, 08 May 2026 19:35:04 GMT  
		Size: 10.1 KB (10071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c802c8913864ccb50cdf1c7ca553ee156e72e897b87bdeb667d164df795b8896`  
		Last Modified: Fri, 08 May 2026 19:35:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f1a1b03fb4fcf49a86748b69ebcbef884d4f379e644a97465de6020ce24215`  
		Last Modified: Fri, 08 May 2026 19:35:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c807b599b3a94b5f5310a8d4b9b7070976d1bb6c01b126ba049df1020103a304`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9636af2d93fa89069d1b12c2c6851a7c2952b1a34f7582de0dc427e71390d580`  
		Last Modified: Fri, 08 May 2026 19:35:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:243a4c30213ec657871633dd0d19dfbd686a84a688a4d2c3d4556642bd8fe361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42faed1738926395170e9db990674b0dbf13536a02b919d4118c7bbd0aac4d6d`

```dockerfile
```

-	Layers:
	-	`sha256:b6cdbcbdc75a36380fefd96483e591b0725c40a56d5a8966f7bedf29b87a850e`  
		Last Modified: Fri, 08 May 2026 19:35:02 GMT  
		Size: 5.7 MB (5715108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aa54600ca6142443a8f7e514a9ec6f99b3ea970d2a78a021ffe8897b922e614`  
		Last Modified: Fri, 08 May 2026 19:35:01 GMT  
		Size: 54.1 KB (54137 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; 386

```console
$ docker pull postgres@sha256:98da647f0ab8cc1afb966e94b31fbd8f56958c87423b944b7980b72ad67d9a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169258896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6252ce2114467130934646048590d996b9efafebc90e8d98b8c4f87971a4642f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:32:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 19:32:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:32:15 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 19:32:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 19:32:19 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 19:32:19 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 19:32:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:32:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 19:32:23 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:32:23 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 19:32:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 19:32:23 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Fri, 08 May 2026 19:42:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 19:42:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 19:42:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 19:42:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 19:42:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 19:42:18 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 19:42:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:42:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 19:42:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 19:42:18 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 19:42:18 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 19:42:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3140d9e514bee29463969b6a78a923fb2a85dcb34a20a0094776c3e04961631`  
		Last Modified: Fri, 08 May 2026 19:42:36 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980961bc487dcd24937e29bd5f992bc9180c29a60e09a0095563d6d738addf12`  
		Last Modified: Fri, 08 May 2026 19:42:36 GMT  
		Size: 6.6 MB (6631532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf7f0b8c7f3bef7c2665d809cdc26e32856d0146ca65b1e8f5261b502f5396b`  
		Last Modified: Fri, 08 May 2026 19:42:36 GMT  
		Size: 1.2 MB (1225866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b802b5e8d949e0a57fd46a75daa2127693d1f11de82af84699a413f8aba1612`  
		Last Modified: Fri, 08 May 2026 19:42:36 GMT  
		Size: 8.2 MB (8204012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827a31b2a10d36ae3533e03228f02357beb1de3a10f97539506d2eabbf13b0fc`  
		Last Modified: Fri, 08 May 2026 19:42:37 GMT  
		Size: 1.3 MB (1308257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0319ca2c644ec6257171b24e7d73bdb2ee25bd4ef6896ee75d6f69d01aaf3ccc`  
		Last Modified: Fri, 08 May 2026 19:42:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac74544f43231092c24d72b3a290ddd042019b00b5cff576f0150e5409d809b`  
		Last Modified: Fri, 08 May 2026 19:42:37 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28caa9253658249d86d16a8932bf2100537b969edc443e57b4dc6ccd9ead2039`  
		Last Modified: Fri, 08 May 2026 19:42:40 GMT  
		Size: 120.6 MB (120571756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21a57ce76f0aab830b10cfb80d3800e14933e093eb5de0ed4ac94fa0566f6f5`  
		Last Modified: Fri, 08 May 2026 19:42:38 GMT  
		Size: 10.1 KB (10070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dda74823715821ef6319b3db0ca0e4de9a39630accf196db2ed28cadd47c376`  
		Last Modified: Fri, 08 May 2026 19:42:39 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e2c77fd0fa46a7e4b0292cacca96523e3da22783078afaa1f949ca763f111`  
		Last Modified: Fri, 08 May 2026 19:42:39 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541a2bfb4b1a3a3afb40ab84dc4f356b347108cf218c1aca8c68c0b7cb1c79d7`  
		Last Modified: Fri, 08 May 2026 19:42:40 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da5dc837b2a5f60952afa927267fb945fc1bce7e31ae4f16b736df52016e6bd`  
		Last Modified: Fri, 08 May 2026 19:42:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ee6a6f20ad11ecb86536ea10d52c462350717874f1957aadb4bb2f6b99dcc40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67868ad23f45119a64582ecc732b6a72b117c663c22806d7ed4d8d2252684aad`

```dockerfile
```

-	Layers:
	-	`sha256:2607a758fa2dd6e200557453891bb39cee3c85d82c71e0a4d6ebb4b77b72b865`  
		Last Modified: Fri, 08 May 2026 19:42:36 GMT  
		Size: 5.7 MB (5724293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:793be3bea3f0c45cb90ac420f29dbd7b9549728036cd92460a564a34c408ee66`  
		Last Modified: Fri, 08 May 2026 19:42:36 GMT  
		Size: 53.8 KB (53814 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:1a13ed861093d81a9a34a71dee87fbc63579c9c6af298c83433fbbe14d4211f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172385308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d336a95785ec2424e4dc37a7ad9bfc170c46871f6c4539074f79c20c1c134d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:04:30 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 22:04:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:04:57 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 22:04:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 22:05:08 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 22:05:08 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 22:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:05:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 22:05:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 22:05:17 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 22:05:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 22:05:17 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Fri, 08 May 2026 22:09:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 22:09:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 22:09:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 22:09:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 22:09:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 22:09:27 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 22:09:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:09:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 22:09:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 22:09:28 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 22:09:28 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 22:09:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2eb5bcf861b5954cbd8aa274be85797f789eaf4f7830d738e4798a1651868f`  
		Last Modified: Fri, 08 May 2026 22:06:33 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c54588ebee8694ff5c5fbf602397f87e358ac7af57d80c8080575f8e637908f`  
		Last Modified: Fri, 08 May 2026 22:06:34 GMT  
		Size: 7.1 MB (7076549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d156dd1c7581b994aceebc6b6f8b3aeae5621031fb3a14bbc7a59ec25d649d`  
		Last Modified: Fri, 08 May 2026 22:06:33 GMT  
		Size: 1.2 MB (1214795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad496728dfe09a0fb255ec139c4280f3dccb2ecef098c1dccdd9169453a997c1`  
		Last Modified: Fri, 08 May 2026 22:06:34 GMT  
		Size: 8.2 MB (8204023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505abe9c519fe082023a9b025f87b79065b404072fad4d9ce899267f09135a69`  
		Last Modified: Fri, 08 May 2026 22:06:34 GMT  
		Size: 1.4 MB (1394915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e1a3bd754a65cf803d92642e60d80a6b17b1c26799da11d9be2ebdb8f9733c`  
		Last Modified: Fri, 08 May 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a246767a8a2895b57737fc54d44684a26eb59099490e87fe9df21f18972b685`  
		Last Modified: Fri, 08 May 2026 22:06:35 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62c82caf89f1b6ad6d1879b5f6ae7df63bceee17a0d0e9d33be3bf36094e417`  
		Last Modified: Fri, 08 May 2026 22:10:13 GMT  
		Size: 120.9 MB (120875872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e961640dd83103c1d052d03194914dcaf7993af501048670fa3141a6d35d9c`  
		Last Modified: Fri, 08 May 2026 22:10:09 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24349b25a82114e4f5d1db199271bff99b51b663326238a0c013cc5558f89a00`  
		Last Modified: Fri, 08 May 2026 22:10:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4a83ce38d20e6d8ee2b48a098324c20070ba808ff5a77be2490355c9fb599a`  
		Last Modified: Fri, 08 May 2026 22:10:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edadf4c0eacbbb494e15bd66394e5439d79aee114e42d6cee926faf237050ee1`  
		Last Modified: Fri, 08 May 2026 22:10:11 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a0f6fdfd827b2f35727c2bb36c0d434d669c236539923bcf09c5d0f4760e59`  
		Last Modified: Fri, 08 May 2026 22:10:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:6b38375a52a2df510daf608827eb1d3c31526133a9bce7b7f15c0a39a1db3815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971762ae71e1809a1f3d2510195a39c2132d319d23498671e307cbcef939fdaa`

```dockerfile
```

-	Layers:
	-	`sha256:caf63cd785822fcafe49916148769edc90e25f7367bf84d0ba5bd16522ab3eaa`  
		Last Modified: Fri, 08 May 2026 22:10:10 GMT  
		Size: 5.7 MB (5715375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d68f6ccb8c9bab4fe250be2047b1d70b5ccb22418a1d045d8b8a6d00b826e6`  
		Last Modified: Fri, 08 May 2026 22:10:09 GMT  
		Size: 53.9 KB (53933 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:0983cce5d4de0fc3220b46e18ae4758639c00084141d9f63f4e0cbf407f1472c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91569333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7629b9429d4c308dfec04d375d5814e84ee27ceee8415c44b412d2f03f8c88e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Thu, 23 Apr 2026 05:02:52 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 23 Apr 2026 05:03:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 05:04:48 GMT
ENV GOSU_VERSION=1.19
# Thu, 23 Apr 2026 05:04:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 Apr 2026 05:05:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 23 Apr 2026 05:05:48 GMT
ENV LANG=en_US.utf8
# Thu, 23 Apr 2026 05:06:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 Apr 2026 05:06:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Apr 2026 05:06:32 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 23 Apr 2026 05:06:32 GMT
ENV PG_MAJOR=16
# Thu, 23 Apr 2026 05:06:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 23 Apr 2026 05:06:32 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Thu, 23 Apr 2026 11:27:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 23 Apr 2026 11:27:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 23 Apr 2026 11:27:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 23 Apr 2026 11:27:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 23 Apr 2026 11:27:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 23 Apr 2026 11:27:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 23 Apr 2026 11:27:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 23 Apr 2026 11:27:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 23 Apr 2026 11:27:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Apr 2026 11:27:28 GMT
STOPSIGNAL SIGINT
# Thu, 23 Apr 2026 11:27:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 23 Apr 2026 11:27:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db89992af1b8d47fd7a9a0f8271eb6df17db144813cdd28aee07960a783a662`  
		Last Modified: Thu, 23 Apr 2026 07:12:21 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c336fb128bf755abcb9cb85e9fac67603aa63e6f620515d2cfcbeebf0546c6f`  
		Last Modified: Thu, 23 Apr 2026 07:12:22 GMT  
		Size: 6.3 MB (6293323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7283b26c842d8881a01e6158d28e702ac9d715e378d52f2de188591630f91154`  
		Last Modified: Thu, 23 Apr 2026 07:12:20 GMT  
		Size: 1.2 MB (1202037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b109565222f047c7a2b619f0dcfbba53241b3e9aefd1a3e8ac3d8cd6d59dc86`  
		Last Modified: Thu, 23 Apr 2026 07:12:23 GMT  
		Size: 8.2 MB (8203659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c83970ff5cc085e629bb1efdc12b0eb2f4fd1b3da6afb03ae1545f6f77dbf4e`  
		Last Modified: Thu, 23 Apr 2026 07:12:24 GMT  
		Size: 1.4 MB (1402351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54288587dc60046cce4eb2f2c87d3951297ec128cc1fabfe154e673e7d1ae5b8`  
		Last Modified: Thu, 23 Apr 2026 07:12:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bc69cbf46986b716209d751964165b000f6d175f963223b5c7bad58dba6d59`  
		Last Modified: Thu, 23 Apr 2026 07:12:24 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8924e3c6ea4dce10b2bad444e98213430c8286c4576f964db22f1736ce7fb2f1`  
		Last Modified: Thu, 23 Apr 2026 11:30:00 GMT  
		Size: 46.2 MB (46166693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1aeebe867ec4385b18fabe3534cc87a17341a6c4a10db725c90b2f219b41084`  
		Last Modified: Thu, 23 Apr 2026 11:29:52 GMT  
		Size: 10.1 KB (10071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d8f60a50fca5bc3356bfe5596112a96b644de0f82b272b485142d07a487e9`  
		Last Modified: Thu, 23 Apr 2026 11:29:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba92e20eb814fdca6e04006a488ad73053cd600b548a5f105cf95acf2eee1110`  
		Last Modified: Thu, 23 Apr 2026 11:29:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1300190a707bd82a70366f7253b5a58a3487e600825007d1a006003b689b1194`  
		Last Modified: Thu, 23 Apr 2026 11:29:54 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f87170d9121be2cb6f8ae2ff89590b69655ef46ca5afed7ff6ac52539b73e7`  
		Last Modified: Thu, 23 Apr 2026 11:29:54 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:770854bebc88ee77f66d36762b61fb2ff293156d7bacb4021bd878e98583deb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5128970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889f92f879ac7045a2c7447b87d4557766a14445fae5d1675e6e9061e2e8623b`

```dockerfile
```

-	Layers:
	-	`sha256:69f3feb11fec0ebb20850243f98781260557582abdac5cab34fae05c8a139296`  
		Last Modified: Thu, 23 Apr 2026 11:29:53 GMT  
		Size: 5.1 MB (5075041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6fcb29dff198745cc39c45c67e848a5aaa14f29e68e4c87fca6867dea0ee27`  
		Last Modified: Thu, 23 Apr 2026 11:29:52 GMT  
		Size: 53.9 KB (53929 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:d2716aba26d46610f5e3c8f83d180a00b34507353162222ac2531999d2eab17f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174638832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f757d0c8d26f00bd89d1a8d6adb5cde5e906f68cf1e3daa0940e068cda37e01b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:07:58 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 08 May 2026 20:08:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:08:28 GMT
ENV GOSU_VERSION=1.19
# Fri, 08 May 2026 20:08:28 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 May 2026 20:08:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 08 May 2026 20:08:37 GMT
ENV LANG=en_US.utf8
# Fri, 08 May 2026 20:08:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:08:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 May 2026 20:08:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 20:08:47 GMT
ENV PG_MAJOR=16
# Fri, 08 May 2026 20:08:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 08 May 2026 20:08:47 GMT
ENV PG_VERSION=16.13-1.pgdg13+1
# Fri, 08 May 2026 20:42:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 08 May 2026 20:42:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 08 May 2026 20:42:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 08 May 2026 20:42:53 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 08 May 2026 20:42:53 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 08 May 2026 20:42:53 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 08 May 2026 20:42:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 20:42:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 08 May 2026 20:42:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 May 2026 20:42:53 GMT
STOPSIGNAL SIGINT
# Fri, 08 May 2026 20:42:53 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 08 May 2026 20:42:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324a6d5bc993de76118c34ad358b49e49ec21c76110bd38bf8a9c2a311627727`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96784e671d70834e50d6c40942ae4db432860007f1a1d3ca3a2fb94702158e93`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 6.4 MB (6408011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52635f5e39fc81b1081c836e8c897de19e77010241bd6e847f3a050cb4458e1b`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 1.2 MB (1230311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32ecff256196f59fabe2e7fd5014efaf226ac93d31f83f1d3bd9e9830813f51`  
		Last Modified: Fri, 08 May 2026 20:26:45 GMT  
		Size: 8.3 MB (8259087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9b036b14f6c076459ab17f58edd2ac18e095da45c4fc41586c00260f74a842`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 1.4 MB (1398299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb09830cc71cb54a7a0536f0027bf458b4bcadae9dc56a6e095e5c0ad7601e62`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddbe193e1088d4792995e6361ab179e35a4b3c8333fec5c7d0c4dfc386907fb`  
		Last Modified: Fri, 08 May 2026 20:26:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29d126a87f50bdbba0b89bd7b137b4911f83d452731ebd23049f33a8866e912`  
		Last Modified: Fri, 08 May 2026 20:43:30 GMT  
		Size: 127.5 MB (127481702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc9c655eeabaa511a15ce252e450e64c343d32626b9112f331042d1ebc335a7`  
		Last Modified: Fri, 08 May 2026 20:43:28 GMT  
		Size: 10.1 KB (10068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c98e56ac4c5c59f07208f444f41f02ffa6885beb7a5c7baa1c42b9f030103a`  
		Last Modified: Fri, 08 May 2026 20:43:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5503a4f5cc57bb3db04c69342c7d9ace1bb4366097607fa359c5408cb2454998`  
		Last Modified: Fri, 08 May 2026 20:43:27 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cd09fdd7d3ad1b5de146b207135bee0fd2190e718219c06248bca04e2f815d`  
		Last Modified: Fri, 08 May 2026 20:43:29 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a07c156e49c802ed7ad0f3866a84eee25079056a93a3acd15fe2f5c70f4905`  
		Last Modified: Fri, 08 May 2026 20:43:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:9ca6871b2530a2118d7512533c1ab57d9729e090b9b1b95220e468b85d61781b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d2bee0f2af69fcc56749b30d5e00ccd6dbff877563c6dea7217f820f1ed50c`

```dockerfile
```

-	Layers:
	-	`sha256:d756bcea567ab1bdfc2d4d7c4223ad2ba54e7df278a7f3796f306331c3263284`  
		Last Modified: Fri, 08 May 2026 20:43:28 GMT  
		Size: 5.7 MB (5725431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f644713f1ae84e6fb5298d2b7bf6559e4bcb8b80602318df08e667fab2e35ae`  
		Last Modified: Fri, 08 May 2026 20:43:27 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json
