## `postgres:18beta1-bullseye`

```console
$ docker pull postgres@sha256:16cf86004c2f5b8c7bf4c1bf3024f930faa6c76f1e96e5540e6fa62ddf603004
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

### `postgres:18beta1-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:bf9b7a364b6867b7889c93e510d221838fc63b29cb2236cecb603d2494a52cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149416706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b040fcbab1557613c8faf8a6ceb88d4763e3c0cb0d5d4023630bd03a55bb5d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031d22971b3ed5d407b088ee54e2d6cbd790c0351e6e21d7ef8598bf05f7417c`  
		Last Modified: Wed, 11 Jun 2025 04:03:19 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1437f2bd1e1577bce713d458352377f7c7852c826dd85c04d8b3bfaf18f0e4`  
		Last Modified: Wed, 11 Jun 2025 04:03:19 GMT  
		Size: 4.3 MB (4308132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71ae3310ef2f6da0bbf0c063e42cd030a10952075d52f93f9c66fc8b9a9159a`  
		Last Modified: Wed, 11 Jun 2025 04:03:19 GMT  
		Size: 1.5 MB (1473584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac120b9b24f24517043dba5fa404ddddb1b100c8e270ce07f2bb2d735fb16b7`  
		Last Modified: Wed, 11 Jun 2025 04:03:20 GMT  
		Size: 8.0 MB (8045878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527a6aa82c8b1502f7a8fcf84b72c36916e16a1926207c5040dddec5b37e3732`  
		Last Modified: Wed, 11 Jun 2025 04:03:19 GMT  
		Size: 1.0 MB (1038349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be01aa70f5a0173f03f06aa520b430d8a1b28be19d3ebd86a6c1bd117cae80a3`  
		Last Modified: Wed, 11 Jun 2025 04:03:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f73e86d0e00f73c4da64141923887a158e4e8a8886abb685663afd0539ebad5`  
		Last Modified: Wed, 11 Jun 2025 04:03:20 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56745df40b1078fb9e9c415e3d78b1d324f9d7f32c3c25e5af0537a6414c637d`  
		Last Modified: Wed, 11 Jun 2025 04:03:27 GMT  
		Size: 104.3 MB (104264231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca9b1a91b81e0db250c333926e88183eac81ee74bff8dfce35d6a9a1fe066d`  
		Last Modified: Wed, 11 Jun 2025 04:03:20 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c031470d6f16d3642d6790e12803568c517b0e4859c10631af096f5623243d4`  
		Last Modified: Wed, 11 Jun 2025 04:03:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825cc30b3e9ab2cef50b021c501f49bbbfc6ad0a8577aea139645c1541e25d1a`  
		Last Modified: Wed, 11 Jun 2025 04:03:21 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb374b2e4a55b445f0d7fab531ceb806f3d33f71b8aa219a622dc4a595636fd2`  
		Last Modified: Wed, 11 Jun 2025 04:03:22 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09c2d33c9e0c6eb67b2a70f6b474017a7649a316d5cb93365c7a9d4bbec32b`  
		Last Modified: Wed, 11 Jun 2025 04:03:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d6a754041d5332d797ea494204667ee462f574486b2bb1fe0b0ba552dd21be33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc48e2e41f16a37ea574ea932943f4dc70a5cdbabb390a8fa162bf295bcc3c2d`

```dockerfile
```

-	Layers:
	-	`sha256:b0e5c034e3d87536de3dfd38ef3fb8e97d4816a41ce659daa16ea7eb32a0b7b4`  
		Last Modified: Wed, 11 Jun 2025 02:10:57 GMT  
		Size: 6.5 MB (6474629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:102772c9cb2a534e420d707eb930517f968cd417cb5364ad1a4b8a091e30c8cf`  
		Last Modified: Wed, 11 Jun 2025 02:10:57 GMT  
		Size: 54.2 KB (54167 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b2ab1ac050728b13a50ac41258b29dc512cbf42407f5a7922988efb7c1d6c127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80904479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9726d407f15cf5445f77116713dff8d183d054154a6abac875be828f5a1ee37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:254beacf3f323cf99977d539dcb720dc371b362af3a11b68a1c46f29aa86d29f`  
		Last Modified: Tue, 10 Jun 2025 22:48:19 GMT  
		Size: 25.5 MB (25544195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abe736d79e05f6cffecc0489bd1925ce7cc5f9671168cbf7867aa77313d971d`  
		Last Modified: Wed, 11 Jun 2025 02:25:07 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d9397c415d07185281508dbfde76f00630943770be20437cc820991f8ec21a`  
		Last Modified: Wed, 11 Jun 2025 02:25:08 GMT  
		Size: 3.6 MB (3601820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1a1bf96ba3a9651841503cf2b69eee23230d91c9126b1234cc229031dfea69`  
		Last Modified: Wed, 11 Jun 2025 02:25:08 GMT  
		Size: 1.4 MB (1440899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2025e835f5ed5e2604a37406d717ed5a637e9d92206db7c4a8cf1d65438ab5b6`  
		Last Modified: Wed, 11 Jun 2025 02:25:09 GMT  
		Size: 8.0 MB (8045875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff99a2f3dce50e4137487f6eff81dc15728ca8800ca80b7dae2b06fec7760202`  
		Last Modified: Wed, 11 Jun 2025 02:25:10 GMT  
		Size: 908.7 KB (908668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2116d5e376bdceb6d9777f3d1726c44c6a3794040d3f15b49f2a4bde1a67793d`  
		Last Modified: Wed, 11 Jun 2025 02:25:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362f39dd9579f18412778f736f45f79de6eb0f211f150b4d55a14a370325c7ec`  
		Last Modified: Wed, 11 Jun 2025 02:35:08 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faade6b63f72f8130dea8af14dd1cacc3120495851a8ed5f4634248e1c34d072`  
		Last Modified: Wed, 11 Jun 2025 02:24:39 GMT  
		Size: 41.3 MB (41332548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453eac95777a537586f05ab2d209f29f801b5ab99958b4ea94c67b68f89a9e2c`  
		Last Modified: Wed, 11 Jun 2025 02:35:11 GMT  
		Size: 19.1 KB (19112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a71b7809729d16687eccc738aa7d9bea17259e513868c335688b07105c1654`  
		Last Modified: Wed, 11 Jun 2025 02:35:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d39dccfd02b9658bfa13ee9c2e52bad3cf78c8df0b0b62b4dca0a13b83a799`  
		Last Modified: Wed, 11 Jun 2025 02:35:17 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910184ae81f3348d0a6a801b0866c73f598657565d6ef5f5e8b4a19e6fca9dba`  
		Last Modified: Wed, 11 Jun 2025 02:35:19 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e52b48897375e7f31882bfad49c916f25df4f37b8f8eb72b71ace9b0992a86`  
		Last Modified: Wed, 11 Jun 2025 02:35:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:ff207881c7d1f2b9984c2c4fc781f21e735be36992c5b273237da878cc30196f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5683904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58e0c14c42bb29d6ef25c5ae6a1efc4abf2d77cacf8f67d879d916da410d56a`

```dockerfile
```

-	Layers:
	-	`sha256:849b079a1ac9ea792b844a270d0260edb3e920f2c6a3b294777fc366eb6162a2`  
		Last Modified: Wed, 11 Jun 2025 05:11:13 GMT  
		Size: 5.6 MB (5629559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d2fafa74914554cc31fd5fd2969f6d83d9a7d5a44dd6b94a89d4a097eff776b`  
		Last Modified: Wed, 11 Jun 2025 05:11:14 GMT  
		Size: 54.3 KB (54345 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:90b4584a7e46361040dd39d89712c5945d8d6e2699cc3d1ebdca149491724e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146420054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475b5cfcf71632b0555c3a99d2c809cf153079c54fb134cb4e49e0693290c95c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d1aa8b14d6c2340d79f9dcc5c7d981e9e2449c2ca1ddd3b841ba02a9ec9f67`  
		Last Modified: Wed, 11 Jun 2025 02:17:16 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ab99dfee393772b9d00749ba3a527c73c1a985bb2fed2a057c33d6f424c5c3`  
		Last Modified: Wed, 11 Jun 2025 02:17:18 GMT  
		Size: 4.3 MB (4312799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d3d84fd8c9d70058c8e0b4b31de85d5043cda15864068cea6f88d0a4f7be0e`  
		Last Modified: Wed, 11 Jun 2025 02:17:16 GMT  
		Size: 1.4 MB (1405929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10877f2d7984dcfc3fb405a8f9308383ef014de0f5c75bcdc758568a3d5ac16d`  
		Last Modified: Wed, 11 Jun 2025 02:17:18 GMT  
		Size: 8.0 MB (8045717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935055b822914944b70a0083990ace46c79f323e5b48a04fa6930405a9c3dc8f`  
		Last Modified: Wed, 11 Jun 2025 02:17:18 GMT  
		Size: 1.0 MB (1026587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c81c0a4b897271c0a3da28c0825c4f12588599be36b9dcaaa7f853fdbf25578`  
		Last Modified: Wed, 11 Jun 2025 02:17:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f71f395644070dac7f893864d14036e82819689dd49412df9b843b9befd09fe`  
		Last Modified: Wed, 11 Jun 2025 02:17:18 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb70be45ee0110b6274b91478629b3e16f4462390cc5fa356d7e1ba916cc378a`  
		Last Modified: Wed, 11 Jun 2025 02:17:23 GMT  
		Size: 102.9 MB (102854363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99c632da84c3633d11b52deb0942d34da991a3684bb86ee7aad1397c8de9cc5`  
		Last Modified: Wed, 11 Jun 2025 02:17:19 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d9bce9c40ba9ef20236dca3f43c0b5134d12090367290bd6bce36262c90dae`  
		Last Modified: Wed, 11 Jun 2025 02:17:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c295350ba57ae13937d99f8920b6407d6b38bcba9d6d6190ce5b2f96a826218`  
		Last Modified: Wed, 11 Jun 2025 02:17:19 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6681ffd334e64649216a4ef793aa23a97c6112e55ea61832035470debbd99a08`  
		Last Modified: Wed, 11 Jun 2025 02:17:19 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba9292e10ec3edf919fc1be27729f5facd0d9610818ee9a13518f7e0f0ced07`  
		Last Modified: Wed, 11 Jun 2025 02:17:20 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:9873bdbbe5eb5fad82bdcfad6cbec51c937eee95b87029cd391e65a9d71324bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6535306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77a8b44098cc8c11eb1b0f09d0fe3c91304530d8402d90e03244c18884966da`

```dockerfile
```

-	Layers:
	-	`sha256:e991368591840f3a96edc5bcf8f057411143291ae05ab800fffdd7a7729d4fdf`  
		Last Modified: Wed, 11 Jun 2025 05:11:20 GMT  
		Size: 6.5 MB (6480906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53651ebb902f4b818669574251bba71a349a0f6df643dd5e0617c1a3679bff8`  
		Last Modified: Wed, 11 Jun 2025 05:11:21 GMT  
		Size: 54.4 KB (54400 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:866d73733642fba5915254b96b3822728137831d472f90ecba549e187385e0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91043373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ae3f4b9907f201d9ec6625224ecae8bfc2c7f609a615c1a787c975b65b4976`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jun 2025 21:23:06 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV GOSU_VERSION=1.17
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_MAJOR=18
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PG_VERSION=18~beta1-1.pgdg110+1
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
VOLUME [/var/lib/postgresql]
# Mon, 09 Jun 2025 21:23:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 09 Jun 2025 21:23:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 21:23:06 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jun 2025 21:23:06 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 09 Jun 2025 21:23:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1294ecac50b0f4fe7018ad5e666e6e3c43bd85fbdc4ff68322834fcc70904e3c`  
		Last Modified: Tue, 10 Jun 2025 23:26:42 GMT  
		Size: 31.2 MB (31189682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48326e3202a7d581aedb37f968b2ae7a959bb408cd92bb4cd41af78676a3c002`  
		Last Modified: Tue, 10 Jun 2025 23:43:15 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ebfffed07741abcee3a3ef3b0786d69c0c6395799eaefa8043d668bfd9dc61`  
		Last Modified: Tue, 10 Jun 2025 23:43:15 GMT  
		Size: 4.7 MB (4719699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b140080ab7e224b8ef38da91a1841c9a36042a969d4fa0257376edae6f6dad5d`  
		Last Modified: Tue, 10 Jun 2025 23:43:16 GMT  
		Size: 1.4 MB (1449377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175c7fd4499d2a2d0e5bb28696b9f5f644d15e942b17f4a39786a44cffd0d978`  
		Last Modified: Tue, 10 Jun 2025 23:43:16 GMT  
		Size: 8.0 MB (8045775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb2442110d955a64de9873a54094711991a44d13073263f2a0e7360f39c5a3c`  
		Last Modified: Tue, 10 Jun 2025 23:43:17 GMT  
		Size: 1.0 MB (1028924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba77ff36f49a8f5738664e712cbb35aea712865a22b440f78d9a1f89f9071d9`  
		Last Modified: Tue, 10 Jun 2025 23:43:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5328bff925e59eb36c38d4cdfb712bb8a85fdfc1d4a2cc4cca4eac5d4e9fffc`  
		Last Modified: Tue, 10 Jun 2025 23:43:17 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2a37507cfa9d02f1e13510f1aa96f01f21e306175e6ad12f40e9c661c2a105`  
		Last Modified: Tue, 10 Jun 2025 23:43:21 GMT  
		Size: 44.6 MB (44579448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06930825935e1e6097a2e86b0b7800bb565ba486e94690587322f9a6748aaf2`  
		Last Modified: Tue, 10 Jun 2025 23:43:17 GMT  
		Size: 19.1 KB (19112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341c71e2252166f2a7113069736f3a3569a48f769c0c87681a303454220b9920`  
		Last Modified: Tue, 10 Jun 2025 23:43:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e80030e4223170644e6019e06f00f8ad0e61fcc16685470f5ec0b27fa9be7d6`  
		Last Modified: Tue, 10 Jun 2025 23:43:17 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c681036d62cb74b510327ecb59b6c629627ef9950a9d937a332b21098af60d44`  
		Last Modified: Tue, 10 Jun 2025 23:43:18 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf5298a5219719eab9861957b7aefd70e2d640f92b04b1409c4ce8e369c2d51`  
		Last Modified: Tue, 10 Jun 2025 23:43:18 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:1dccf75cd30a9a83a157c00d5eb9c04187f07f002a5afcc538aba7cd56807280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5678299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea1d77383cbb4ec2f2d02b10b7c6cf71c08ae55917819b999aaffd5020e60e3`

```dockerfile
```

-	Layers:
	-	`sha256:046d4d6d51f8e06ba493a8251de12d2e20eb7d964464fcb7925c20e06aeeb49e`  
		Last Modified: Wed, 11 Jun 2025 02:11:13 GMT  
		Size: 5.6 MB (5624177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61e71fc93b87170ba11cf617238afd75497357e771e7f9efa37739512554fe39`  
		Last Modified: Wed, 11 Jun 2025 02:11:14 GMT  
		Size: 54.1 KB (54122 bytes)  
		MIME: application/vnd.in-toto+json
