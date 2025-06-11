## `postgres:18beta1-bullseye`

```console
$ docker pull postgres@sha256:974bb6bcb870304df4948b50cb87c97107bf85e0c757c490421ce2a4e8125a88
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
		Last Modified: Tue, 10 Jun 2025 23:34:52 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1437f2bd1e1577bce713d458352377f7c7852c826dd85c04d8b3bfaf18f0e4`  
		Last Modified: Tue, 10 Jun 2025 23:34:53 GMT  
		Size: 4.3 MB (4308132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71ae3310ef2f6da0bbf0c063e42cd030a10952075d52f93f9c66fc8b9a9159a`  
		Last Modified: Tue, 10 Jun 2025 23:34:53 GMT  
		Size: 1.5 MB (1473584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac120b9b24f24517043dba5fa404ddddb1b100c8e270ce07f2bb2d735fb16b7`  
		Last Modified: Tue, 10 Jun 2025 23:34:53 GMT  
		Size: 8.0 MB (8045878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527a6aa82c8b1502f7a8fcf84b72c36916e16a1926207c5040dddec5b37e3732`  
		Last Modified: Tue, 10 Jun 2025 23:34:53 GMT  
		Size: 1.0 MB (1038349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be01aa70f5a0173f03f06aa520b430d8a1b28be19d3ebd86a6c1bd117cae80a3`  
		Last Modified: Tue, 10 Jun 2025 23:34:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f73e86d0e00f73c4da64141923887a158e4e8a8886abb685663afd0539ebad5`  
		Last Modified: Tue, 10 Jun 2025 23:34:53 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56745df40b1078fb9e9c415e3d78b1d324f9d7f32c3c25e5af0537a6414c637d`  
		Last Modified: Tue, 10 Jun 2025 23:34:56 GMT  
		Size: 104.3 MB (104264231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca9b1a91b81e0db250c333926e88183eac81ee74bff8dfce35d6a9a1fe066d`  
		Last Modified: Tue, 10 Jun 2025 23:34:54 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c031470d6f16d3642d6790e12803568c517b0e4859c10631af096f5623243d4`  
		Last Modified: Tue, 10 Jun 2025 23:34:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825cc30b3e9ab2cef50b021c501f49bbbfc6ad0a8577aea139645c1541e25d1a`  
		Last Modified: Tue, 10 Jun 2025 23:34:55 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb374b2e4a55b445f0d7fab531ceb806f3d33f71b8aa219a622dc4a595636fd2`  
		Last Modified: Tue, 10 Jun 2025 23:34:55 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09c2d33c9e0c6eb67b2a70f6b474017a7649a316d5cb93365c7a9d4bbec32b`  
		Last Modified: Tue, 10 Jun 2025 23:34:55 GMT  
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
$ docker pull postgres@sha256:399ce08145da93b5d31fa4d0f48f1b1b74d04ac072e00178edde24582c9e17c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86659709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e096a63e39e604cad4a909c075a27ac66534d489656413acc003c355dc7c2f6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
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
	-	`sha256:2091b63a268a34467e23520ae27c312421298f420abd278e760061e42a678899`  
		Last Modified: Tue, 03 Jun 2025 13:50:37 GMT  
		Size: 25.5 MB (25543902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2819feb174cd62d9afe4efa58f14c05d6404e45e9fd646186b5caf9e4ffb95`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b854a91797948fa74505443fa76802d4719c60aea4cc87fd15783f71c9acfd55`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 3.6 MB (3601790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6970d22b731c3a99427af1912f1730e34e40009bc7af854735159a9603ffa3f`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 1.4 MB (1440887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a3cd249b6bf25ca9bbea16ab2a0959459eff6af0e43e16d8c956d2888065c1`  
		Last Modified: Tue, 03 Jun 2025 13:44:36 GMT  
		Size: 8.0 MB (8045791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d46adcc9f43b0fd86209d8380e586d2c3465d713fe7c68169a9b3899cfd39f0`  
		Last Modified: Tue, 03 Jun 2025 13:44:38 GMT  
		Size: 908.7 KB (908651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa3404576c56b7e91cee8f6cec2f6cd80e371cbe93a5a27e90528f7ed08518`  
		Last Modified: Tue, 03 Jun 2025 13:44:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd2b53fdac06669f7ad19fd8504e96e7e1429ba317a634f81a63c8d05cc0b2c`  
		Last Modified: Tue, 03 Jun 2025 13:44:40 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497b906dc3ecba55959264695c98ca662c2b50a7f95285b1b85435a46d9ea25e`  
		Last Modified: Mon, 09 Jun 2025 23:30:22 GMT  
		Size: 47.1 MB (47088218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c97b61a611610accac08eeca6ca3d47b993d7644ee4ec2654c935725065b6e7`  
		Last Modified: Mon, 09 Jun 2025 23:30:19 GMT  
		Size: 19.1 KB (19108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee68a632c006ac10690bec59e011042759930d3e3514a7b7be9fda1bc94a6df5`  
		Last Modified: Mon, 09 Jun 2025 23:30:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52560061a59d583a7c286ff35885b918eb5e45c4da729f5668364a1d93eb519c`  
		Last Modified: Mon, 09 Jun 2025 23:30:20 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f7a7d60ddd6b688d391616d2ada84fd28ca946853db7f6abcfa7e1a3ff647d`  
		Last Modified: Mon, 09 Jun 2025 23:30:20 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b073d077539498da0ce1076dfc75dec762f69dba735d4c0b96f362b910eed0b`  
		Last Modified: Mon, 09 Jun 2025 23:30:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:76aabfe62bee526650fa66f59ac736b7b5f840b6e16acbf5d5ce00db1f317994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5685178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e98486af5e8ca37c233e72c2b621b949b4c64ad3053194609660a9a39332d`

```dockerfile
```

-	Layers:
	-	`sha256:d05e29e4ce9f4dbcca4e5db75834869a46541b18ce93e49c57b792b7e0da1ab6`  
		Last Modified: Tue, 10 Jun 2025 02:09:49 GMT  
		Size: 5.6 MB (5630831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0bbcfb6c96dab79afed7775f82ba17ea1cde697e37f07bc5ccb7eecd8f4471`  
		Last Modified: Tue, 10 Jun 2025 02:09:50 GMT  
		Size: 54.3 KB (54347 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta1-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3710d1f47c3b58c514249ef49bcb5df16e8f569013a3d21ef44e32e45691f6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.4 MB (146422419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c82400e45d033f7557a20b8dabfa4bb1fd414694075ef013499bf721503415`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade30debac6fbfee61ba0a16cd7cd4a5a2362d0bc00349c425dcae0dbdc27315`  
		Last Modified: Mon, 09 Jun 2025 17:22:47 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b2a1907d3ca81f8fe755299114cc82d225ad26738e3ab6eb8ef3ef4fcb6ade`  
		Last Modified: Mon, 09 Jun 2025 17:22:52 GMT  
		Size: 4.3 MB (4312864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca74376c9de08cab66a966e2fb5d4eee65048765c129b48c8917a07ea47f49a`  
		Last Modified: Mon, 09 Jun 2025 17:23:12 GMT  
		Size: 1.4 MB (1405880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71517e9a8976f9812c6a92b3f26c890109ce95ad52e22925c6351c134dd5e00`  
		Last Modified: Mon, 09 Jun 2025 18:18:05 GMT  
		Size: 8.0 MB (8045811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea5c166f2e4f6a970930938e7e729cc4127254877c529ff44b5f338b8c868e8`  
		Last Modified: Mon, 09 Jun 2025 17:23:19 GMT  
		Size: 1.0 MB (1026592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb977ec5c7a895b3243c2ee24b985aafd1736c73c773d725f88b6f279149a05`  
		Last Modified: Mon, 09 Jun 2025 17:23:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c61493954d856ffbbade5169251a9c95f0084c9754b65f942342160aa7ba4`  
		Last Modified: Mon, 09 Jun 2025 17:23:29 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab084f025f3a82c7ac676b0679895114028211d9f3170d8b1db28893a5b9b44a`  
		Last Modified: Tue, 10 Jun 2025 09:14:01 GMT  
		Size: 102.9 MB (102854541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a524a3c8fc2036009cd627308f492f01f0d6b43fc4ee9991725a590fe823a0`  
		Last Modified: Mon, 09 Jun 2025 23:11:54 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5879bd48c1aceb68eaf1ef3fc6d2cdb89de08f58ff6ebbb208850e36f3bbe1`  
		Last Modified: Mon, 09 Jun 2025 23:11:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e6a17c4b798669c61c844076eb5462b0345c3497abaf048486609011dd37b3`  
		Last Modified: Mon, 09 Jun 2025 23:11:59 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de21bca97a05c6d0267f9cb3b214dd004377a4fa42f670cf9a5434350a5ac55b`  
		Last Modified: Mon, 09 Jun 2025 23:12:02 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9144583cf9c134aa64808edb8f3abc206b731497149284156594471b467d38`  
		Last Modified: Mon, 09 Jun 2025 23:12:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta1-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:696779c7a796545933e840a3eafeae9cf8327a00ee374187a04cdac19823bf6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6538087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880006d775d8b62e2e4d15c8faceda66f6ea8f10c5c93043454399ca9c2ca819`

```dockerfile
```

-	Layers:
	-	`sha256:b22af22cac6c24603c5b129e86f183e284faf61d0194f69e7c5396822a369528`  
		Last Modified: Tue, 10 Jun 2025 02:09:54 GMT  
		Size: 6.5 MB (6483687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16bdbff3e0d0b4664d446a50b41e21e9fd49bf5753b8a788954683c44a7e6025`  
		Last Modified: Tue, 10 Jun 2025 02:09:55 GMT  
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
