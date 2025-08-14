## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:1da055802fa53739179143682482601ee91ba1238ae88406c89e822943d390cf
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
$ docker pull postgres@sha256:01f27351c6c14e821a104a5c53196d1c0c1cc1de1f397d9c3c344ac84225664a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155282164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfcaa4640b85e2f2d2e75fff8ba6fca3f3578d3f9d58e4c3e900e1978ec51c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_VERSION=16.10-1.pgdg12+1
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:56:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:56:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:56:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:56:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9cbfca11d34c3b5242931c4824afd8b63cc25e3ff46c1fbc6752fd967b8b442`  
		Last Modified: Thu, 14 Aug 2025 18:20:06 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a759c99e5d9ccb4d74bb0359764af8d79b98567d708ea1e488c18a62deb53e7f`  
		Last Modified: Thu, 14 Aug 2025 18:20:07 GMT  
		Size: 4.5 MB (4533688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40999643f831e244ff5b0ad85392da6e51ef82a9f99160d85a3723f3e0a8e4f`  
		Last Modified: Thu, 14 Aug 2025 18:20:06 GMT  
		Size: 1.4 MB (1446747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9c8f27f94cf7b27b56d07705d67f471ccfba7d8963137ae408b21d6062cb2a`  
		Last Modified: Thu, 14 Aug 2025 18:20:07 GMT  
		Size: 8.1 MB (8066282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6019da469dd7120741df5740628dd476087cbbd6f165b1bfb6bed05c851079ba`  
		Last Modified: Thu, 14 Aug 2025 18:20:07 GMT  
		Size: 1.2 MB (1196138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7960bd43e7e7093fc87228eaf9f132681666766f6fada680c0a498256ce300c7`  
		Last Modified: Thu, 14 Aug 2025 18:20:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035bce430520d17512580bb3ab002ac0961df2b2c153430a20d7513c75c8f01`  
		Last Modified: Thu, 14 Aug 2025 18:20:06 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9daad206a8573add64351ba5d021552707051f6a47d970afa13acd6ae5e64fa`  
		Last Modified: Thu, 14 Aug 2025 18:20:24 GMT  
		Size: 111.8 MB (111788301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e9830491e9fc6873ef9e8ee996ce631b95a03609ad124414b7b7f8c33e8238`  
		Last Modified: Thu, 14 Aug 2025 18:20:07 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659157e68c9d8c54c0aed8f14e62f20d617057d7590b1b5dab49a8c1cba7e615`  
		Last Modified: Thu, 14 Aug 2025 18:20:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374299179ba15ab0811816949fa04dac7d48e497cf113225834842806f6ac54b`  
		Last Modified: Thu, 14 Aug 2025 18:20:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712cf9c206493a010f7ce35d07b05593ac55dbd50814c394c3e5923cd7f6bcd0`  
		Last Modified: Thu, 14 Aug 2025 18:20:07 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f04bf0c6c52853a50fffcca73469009dec05b187ab43a180000e5faea7d4fc`  
		Last Modified: Thu, 14 Aug 2025 18:20:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ed04ab73e2033d0c8764dfe50751d33130796c79d929fe6e4e7e63c82dca4ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6042864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c443e43a6a23274397c99e2f8e93097a56b963a31472d2862a2e25b410f203`

```dockerfile
```

-	Layers:
	-	`sha256:28c8a00ece15a6af7edd2225279fe4469d67e1951c5387ea511fb5c01b84b0e2`  
		Last Modified: Thu, 14 Aug 2025 20:15:34 GMT  
		Size: 6.0 MB (5989524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8533f147fb0e3df56cc0d627069c52988ca9792113f266778f3ee7441f99bddf`  
		Last Modified: Thu, 14 Aug 2025 20:15:35 GMT  
		Size: 53.3 KB (53340 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:7f3c730af63371d9868c03db9bb7243fb00900f061c328e225c6b0319c4a20eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148358703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a83e45134d7ee4515fce983c8d1386b60b419d93b4167c6730656db11034660`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_VERSION=16.10-1.pgdg12+1
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:56:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:56:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:56:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:56:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f1308410f7fc012f99053b4cb015f00729905d190346f35e41fdcb392305b5`  
		Last Modified: Tue, 12 Aug 2025 22:35:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe932228ef46a7bb295ff8b94c427fcc664fc20af9603cef5c502294a5219f38`  
		Last Modified: Tue, 12 Aug 2025 22:35:34 GMT  
		Size: 4.2 MB (4151045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d297e9f77474c96968f44d1c2e236e2a0f615159a02033122506c3621aab051`  
		Last Modified: Tue, 12 Aug 2025 22:35:34 GMT  
		Size: 1.4 MB (1424064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0d55562dc7f2fc0a5b6a7ceb4ce7f084a9b0ea371e0006a329a25420a96fe7`  
		Last Modified: Tue, 12 Aug 2025 22:35:35 GMT  
		Size: 8.1 MB (8066423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69b4cd684dc799d3589c4e3ce773988aaf66f993567544c216f4f8cbed55d3`  
		Last Modified: Tue, 12 Aug 2025 22:35:35 GMT  
		Size: 1.2 MB (1194903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45a743949ab456235ea44e0946e8ba2c16cff3f5909e3e45ec665b69e7f37eb`  
		Last Modified: Tue, 12 Aug 2025 22:35:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41be77f8e538f2aff43f10696092d5a909dfc5ea37a1e6c69f6e2d7b3427ff3d`  
		Last Modified: Tue, 12 Aug 2025 22:35:35 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9d744c2845ee6a5eb2c4d9e4ec36dc0e1f7da9062c66f364c60e2c112b6499`  
		Last Modified: Thu, 14 Aug 2025 20:30:09 GMT  
		Size: 107.7 MB (107738792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c808f884ec2f0ffca0592dd0ad25252334a5dc1a4a670c462fb12895984f5f4`  
		Last Modified: Thu, 14 Aug 2025 20:00:18 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2d24dacb7ddc7c07b2fc209c50b09f0bfd03508e09937a1d5c5eb5213403eb`  
		Last Modified: Thu, 14 Aug 2025 19:56:09 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a168a0b6eae462348adb0c8ec556d30fb7ccbe5c1ae0ee8b957ae3b3c5f220`  
		Last Modified: Thu, 14 Aug 2025 20:00:23 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d354cc46f7f79be035ebcdc1911f53b0521ccf8001b0da6e091186aa3b058c0`  
		Last Modified: Thu, 14 Aug 2025 20:00:26 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099ffc7988e3a13963b4539f5c0b5c411df8d1f0ed401b4e4261d693977386fc`  
		Last Modified: Thu, 14 Aug 2025 19:56:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:170f726e6ac166ab6d3ecc9c18299eb228c4b93c363523c26ffcf2a6ecb73933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6061168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a38702b3bbbba834e3fffac5fffd1a840ac1a233406eef863287af317420c72`

```dockerfile
```

-	Layers:
	-	`sha256:b79d6ef895455de6cb87d096e9947714ba07de167df63e2f116a6ff161f6cc25`  
		Last Modified: Thu, 14 Aug 2025 20:15:41 GMT  
		Size: 6.0 MB (6007625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7436633f0b26b38dc5ac5e141896b1765c05b6df77e71763f83322163290beac`  
		Last Modified: Thu, 14 Aug 2025 20:15:42 GMT  
		Size: 53.5 KB (53543 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:47f5c4f02686032c1ecde6006a48ac56a7017d27adfed8e8c94717cca073f4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143361701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa3a89a5b11476b018ecb20566d00e28514430f3ff2a1149c5f840ded310efc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_VERSION=16.10-1.pgdg12+1
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:56:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:56:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:56:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:56:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6820cfb123948a92acbf96b230a0cdea26476a1d3d429aebc35cc9fc764b4a6d`  
		Last Modified: Tue, 12 Aug 2025 22:38:54 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3b99820b8a61186a81204f61ee925a3f4266ace75a824b4ebff77980b261a8`  
		Last Modified: Tue, 12 Aug 2025 22:38:55 GMT  
		Size: 3.7 MB (3742574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba3f5dbe870838e10b49748bc06c909eaeb5ce71d28f86afbb30fb50686f3d`  
		Last Modified: Tue, 12 Aug 2025 22:38:55 GMT  
		Size: 1.4 MB (1413752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991df6523048151c47c162c5ac7ecfc88bf25eeb426a1400cf0194426f20313`  
		Last Modified: Tue, 12 Aug 2025 22:38:56 GMT  
		Size: 8.1 MB (8066369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201deac0b306fa58e8dd8ac5df3e46479efee68548ea761125fc205f19c46d4a`  
		Last Modified: Tue, 12 Aug 2025 22:38:55 GMT  
		Size: 1.1 MB (1067038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8763abcb4c6fe6a574c1314ae0ac66ef89c57408280beea34653c3d252f5ae54`  
		Last Modified: Tue, 12 Aug 2025 22:38:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c55d99fc111b0443e24a20c7eaa4578a66b6eb57754d56f6704f35122015a32`  
		Last Modified: Tue, 12 Aug 2025 22:38:56 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32c684c2042f7e57abcebd43934b87117afb469d56a3b6410f25bfdb11f6cfa`  
		Last Modified: Thu, 14 Aug 2025 20:07:18 GMT  
		Size: 105.1 MB (105112279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb63340b4a48ac7f9b24afc46be0e36561942b103b4a6ad239a514ca4b5324e`  
		Last Modified: Thu, 14 Aug 2025 20:07:10 GMT  
		Size: 9.9 KB (9926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6649ee13a4459c05f588c776e9be6cfcc335f6b85a67a4dd7af5311db015e5dd`  
		Last Modified: Thu, 14 Aug 2025 20:07:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96489e60a37f668f56bcef43dac896a213b89ea60eec980a9bfac8eb6acd01eb`  
		Last Modified: Thu, 14 Aug 2025 20:07:10 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2298d6288031c3c4431333ff480e677a17df1e9f2b508ae019735ec09343857`  
		Last Modified: Thu, 14 Aug 2025 20:07:12 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38235b0a2ff5dd4be413ed3dda6f5c7c94be6566c3457a8177642f19ef152334`  
		Last Modified: Thu, 14 Aug 2025 20:07:12 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:84067f4917008565d3e9e09c3cd6f47e83549bfa09bc6ad5b11794bdf4e4fe02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beddc35925bc64e3469a61a78328799dc93893bd7512274335deef5dc16692bc`

```dockerfile
```

-	Layers:
	-	`sha256:11d56eef4fccb35b4b30f7dffd3e96fe14b4fbb8f5f3a53a6f909396e3b5144c`  
		Last Modified: Thu, 14 Aug 2025 23:11:57 GMT  
		Size: 6.0 MB (6006888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a143ce0232675fa27069377ef99d21c05caf8e35f3d9efc170101fdc8f1f9018`  
		Last Modified: Thu, 14 Aug 2025 23:11:58 GMT  
		Size: 53.5 KB (53543 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:c288ae77b89c13c1e78d89a947f70c7270ce0081a78a26f5e1699fd6f56e43d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153199112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd841d2d58e3f78c24a27a1e6b0ba7d8684075376ff60f8ab6e4be0e454ec181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_VERSION=16.10-1.pgdg12+1
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:56:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:56:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:56:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:56:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f22bf4a69c67725a5d28659467a9f4119ed414adf8a1d433e11ad80206e7a29`  
		Last Modified: Thu, 14 Aug 2025 18:51:34 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361ee65475462ea3e8ee78a207e0ee11b503288d0fc59ca7e79ac316ec6acc04`  
		Last Modified: Thu, 14 Aug 2025 18:51:36 GMT  
		Size: 4.5 MB (4499189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d686f5a8767e8f7119f4019c78e95b41922a788f6adf346700ad86916e3f0d47`  
		Last Modified: Thu, 14 Aug 2025 18:51:36 GMT  
		Size: 1.4 MB (1378836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c4da94471816abaff082b723798940778c0d6e9ba39ca35822ae23757628b1`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 8.1 MB (8066342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dd948fe7b916f24497e0aa4ac3ea5f654f2ec18fecaf144b35e44757fcc0f5`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 1.1 MB (1108732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9e7f843ae66f3ff0fb7f0e9b43b16750e2dff4f3d8bb23e783ba6c4e9faa04`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb81ba96e939b60e2849bd3e78c77085a5b656b0da6722c19eec786712cb1a7`  
		Last Modified: Thu, 14 Aug 2025 18:51:37 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3edc6f490b72e77dc23938c973219b636ea0db7759bda7f1159fe75426ebc58`  
		Last Modified: Thu, 14 Aug 2025 19:07:14 GMT  
		Size: 110.0 MB (110043254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d33a5bd8355c8aa81704881388b4cd6da445a01c51844e2c946d8d76d4c4bf`  
		Last Modified: Thu, 14 Aug 2025 19:06:56 GMT  
		Size: 9.9 KB (9921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0802ccd8ec08c3fe90226c90373edc559499a5c77246df46c93a9384258d346a`  
		Last Modified: Thu, 14 Aug 2025 19:06:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c04263383dcb185bb5e6c7f8b85fb8fcd80756110d2a33839d529cec523c579`  
		Last Modified: Thu, 14 Aug 2025 19:06:56 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49d49c280bd7d4398e2a75332399311a6d6b51693da48fc65eba54ecec9aafb`  
		Last Modified: Thu, 14 Aug 2025 19:06:56 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a2b06c9d3f71b196b4878d883ba06265020a5c2fed2ce3bd0c5dca2e06f944`  
		Last Modified: Thu, 14 Aug 2025 19:06:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5c68429dbf1489cea7b6bf8cecbac9a65fcae95f0dd6341ffb3dc1d79ff37d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6049423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8302114831cb1ae44bb96b6efbe7a86ac01330568388a6a9a3f218dca87e77cf`

```dockerfile
```

-	Layers:
	-	`sha256:6c9ebf1d4a16466b1a60adef3c0657ff4300677517bc99f977c374fdd64274e9`  
		Last Modified: Thu, 14 Aug 2025 20:15:51 GMT  
		Size: 6.0 MB (5995839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13c056ef9684719515761036dcb2332baa9190665d3fdebd6a7709b7b9ad8f7`  
		Last Modified: Thu, 14 Aug 2025 20:15:53 GMT  
		Size: 53.6 KB (53584 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:6302e5605162d79d9c98bbd0561fe6f217d0ffeea42e3cb024765e152d17046a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.1 MB (164140170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6e16cde84524bd2bc535432a7ef9aa99bcf52320467a3a832f548c3e2921b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_VERSION=16.10-1.pgdg12+1
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:56:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:56:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:56:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:56:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d36a64ec57b666102043b2d97ecf749a26cb648a0657acc591b229cdde12f9`  
		Last Modified: Thu, 14 Aug 2025 18:32:03 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012e41f71126a4570ec3082c24d5be65c4506a6e5baa27187cf26af898ba1dbd`  
		Last Modified: Thu, 14 Aug 2025 18:47:05 GMT  
		Size: 5.0 MB (4965031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c5a8ca3d3590da06653560b2d7b144cd5a5cb2961464ecd565773874c4fddb`  
		Last Modified: Thu, 14 Aug 2025 18:47:17 GMT  
		Size: 1.4 MB (1422270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f2106ac1fc798d23bd5688fc7f8cca1d97c7a9e399959624072d6d22fea9cb`  
		Last Modified: Thu, 14 Aug 2025 20:31:03 GMT  
		Size: 8.1 MB (8066282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3326bb01f1e62b329d55fe8bf530aa8ff75ad3953d4a1a674e73dc96bf15e723`  
		Last Modified: Thu, 14 Aug 2025 18:47:22 GMT  
		Size: 1.1 MB (1137171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3236b7bd2c2f21f371a221d850422e25b5f88aac5644b356f3162d03e1130092`  
		Last Modified: Thu, 14 Aug 2025 18:33:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5299798ec2cbb3576150d75359eb833c4100fa1f9fc663370184dc49f9fb6666`  
		Last Modified: Thu, 14 Aug 2025 18:47:32 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b60e3a3797de45ec8821ada9a2c24869187382826df7085cf040e84e709dfe`  
		Last Modified: Thu, 14 Aug 2025 20:31:14 GMT  
		Size: 119.3 MB (119316052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125aeb5633ac8627485b878775b535641a823ad0303774c15cdfb84a8a7c3ebc`  
		Last Modified: Thu, 14 Aug 2025 18:47:36 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e503ec61b5b2dd9b5c2f0b579abe530e9bf08f2324d410980f1e7f42e476a15`  
		Last Modified: Thu, 14 Aug 2025 18:52:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb54156005c712030e73710e2c22bd745161232ccd731a16d54af61870d7651`  
		Last Modified: Thu, 14 Aug 2025 18:47:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0b71b43b16c1cbf8b27304193f4f40003d13f619385c0ee4e5cc328b31a97f`  
		Last Modified: Thu, 14 Aug 2025 18:47:47 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85afc5ae4cbcd0bdb31f2371f6ed2970a533e0f565c1ed8cf585c762a9060ce`  
		Last Modified: Thu, 14 Aug 2025 18:55:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:9fed4b0570acb9eadd9835d0bc8be6184bfd344f32f29faa6b12e91be5adfe7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6059052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c0b065fafd840a3ecff57e20b1cf5155c19866f43210c109754691b24f9066`

```dockerfile
```

-	Layers:
	-	`sha256:ec9827ef7beaabe9e23faf4da84172452965e4430fbd127decf7df1d0f331092`  
		Last Modified: Thu, 14 Aug 2025 20:15:59 GMT  
		Size: 6.0 MB (6005756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10293dc3c467dad156bba41a6d44c31c55f2450844c2ba6445d5f9d4baeeb042`  
		Last Modified: Thu, 14 Aug 2025 20:16:00 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:352c190d3f3c8cc729f18ac292856145c18b502378905a8f2d571913cd3e4e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154149748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:523cbcbc1d1fede6d1fdd7035d9837256cf4e8dc57cf476eadb84d998d3fe293`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_VERSION=16.10-1.pgdg12+1
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:56:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:56:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:56:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:56:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83bd2d8e15bdca1c657f4e1229c9515648aa638816bf4ae6a4be5a7afaee3a81`  
		Last Modified: Tue, 12 Aug 2025 20:45:57 GMT  
		Size: 28.5 MB (28516923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29312da7268b11c0e420282a3de73777dd60323a6115c94e4770a3967d1008dd`  
		Last Modified: Thu, 14 Aug 2025 19:34:18 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadf75f6a42f2ec57e669503e79a92f31752f394516ac3907e5fb7ad2261db38`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 4.5 MB (4475161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edb5cc62fc658d056d649cb284f0a020e6a6c0b57162be2680462937f71ab57`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 1.3 MB (1333909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474838f47aaa89f71355146b0a39b988275244759ef97d0cf6e616a991c9027f`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 8.1 MB (8066502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148e17ad67a5ccc4d969ff6abab8130942de3726b9e6fad6051c12601f1f8343`  
		Last Modified: Thu, 14 Aug 2025 19:34:19 GMT  
		Size: 1.2 MB (1182641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31de7c74bad6aba9b4e3ba53d1a4cfc29234f0d874650d8b3ecb0e3678aa8c07`  
		Last Modified: Thu, 14 Aug 2025 19:34:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5cba190353263630bff7d7d1f8db3bf41c59f3df3ef093a60839ff9e4950b3`  
		Last Modified: Thu, 14 Aug 2025 19:34:21 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9d740435679797f8c250e98d7cd804525d6b36df928af0240ab90597858864`  
		Last Modified: Thu, 14 Aug 2025 21:57:06 GMT  
		Size: 110.6 MB (110553847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84957ac7566833768bedf37985ca054c01f0f664022729881df695eb844b980`  
		Last Modified: Thu, 14 Aug 2025 21:56:54 GMT  
		Size: 9.9 KB (9923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb04fe82fd18cf2f0ea9357cede5c448793b52f0f3774fdd93bacf43b73e455`  
		Last Modified: Thu, 14 Aug 2025 21:56:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3baa8e397a5bf9cd47fdddb00415f658dfb26decfe79d9424d96395452f4b177`  
		Last Modified: Thu, 14 Aug 2025 21:56:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74fa42028fdc57b792e1d5b1f8191cf70a2ec8ebd5ff9d46035d97c5e5da1c8`  
		Last Modified: Thu, 14 Aug 2025 21:56:53 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd44a605ee96c165b6f5e99cab6582ffa97f1d2faf1f6280aa24933e1e13c100`  
		Last Modified: Thu, 14 Aug 2025 21:56:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3dabe843965bfd151b13c4635e73b71cce4aff733bc38823ee421a6f1fd9a901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5b75c283d8ee10e3f47b6b54681cc3a8a7217e7f65ca86a84accc8e9b1155c`

```dockerfile
```

-	Layers:
	-	`sha256:4f568af5e3252724947caeea3990430e4003ec67af9ccd8dad6bb3bdb3716653`  
		Last Modified: Thu, 14 Aug 2025 23:12:12 GMT  
		Size: 53.2 KB (53206 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:d0ef765e092928ae99ea3d40d85690c9181ed27c73cb384606e49d31efeea161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (167999238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716d64cb92823f01a7cc975096ce378dccadb700c61ceacfca9c330c6c5deb02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_MAJOR=16
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PG_VERSION=16.10-1.pgdg12+1
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:56:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:56:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:56:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:56:05 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:56:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:56:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e71427bc966f27e4c045f76677200cc1cb8d57b75ba0d7ab977498c00e8d6a4`  
		Last Modified: Wed, 13 Aug 2025 11:23:54 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c88c8558d33d220ba0bd06a9aaa623bae8d2dc5226d907b7bea0495002b0d32`  
		Last Modified: Wed, 13 Aug 2025 15:35:10 GMT  
		Size: 5.4 MB (5368151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4541684e1bb8d6caaca0ac9f5d0cf566b2ef5226a534bd35fb5967ecbf66d244`  
		Last Modified: Wed, 13 Aug 2025 11:23:59 GMT  
		Size: 1.4 MB (1368729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f3c9c3e96a7afe0384ff2776211efbadf170ac27ffbd881765dd2568bbe5de`  
		Last Modified: Wed, 13 Aug 2025 15:35:11 GMT  
		Size: 8.1 MB (8066366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5ac7820ef53cc6fce6e86c3e89e9180a62df051f52f4f05f567ba757da2dd9`  
		Last Modified: Wed, 13 Aug 2025 11:24:05 GMT  
		Size: 1.3 MB (1283505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b039814790880fa88c0fe02fdcfc7406c540d2eeccdf1c8012cf811171ba3348`  
		Last Modified: Wed, 13 Aug 2025 12:12:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f05bb5a6b03e6da586b1e62ffbc88e07fc494b048054316cdb970e7f6adacb5`  
		Last Modified: Wed, 13 Aug 2025 11:24:14 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5eb4d4f1544be8f014c0bb138831168b9229e4cc2e99b1753ccea3657ac789`  
		Last Modified: Thu, 14 Aug 2025 19:24:45 GMT  
		Size: 119.8 MB (119818308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50f169d367f6a464f23fa97898a217f077dbc048a897303072adee141416822`  
		Last Modified: Thu, 14 Aug 2025 19:24:32 GMT  
		Size: 9.9 KB (9924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975505bf903e6b1c161250fd55fa08ce4f664d9078fe6ca68459ac4400c0050a`  
		Last Modified: Thu, 14 Aug 2025 19:24:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d34f5599342a34b1497523e37719e58b8e477207a9705880e9dd0a9bfa1c10`  
		Last Modified: Thu, 14 Aug 2025 19:24:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceda2d99f5b2a234f37886cd19f687c9f00aca8cb87768a3432ebf70e5db4087`  
		Last Modified: Thu, 14 Aug 2025 19:24:32 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bab6f55bbb30e0c92365fe48bd76822b9f7d70ddaea76a603f10876c6a857e`  
		Last Modified: Thu, 14 Aug 2025 19:24:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d611599128346e7424da760255712209ea92d560f2c6896398f2e00e2bd6be07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6050299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff7b3b23438434304dc292fd7ec522fdd390b1e88120d060b3a65109ffb3f59`

```dockerfile
```

-	Layers:
	-	`sha256:07b58b589af5330e8acd6eaa7148786fd37fd26568d9ec9203df4fcdbc634adc`  
		Last Modified: Thu, 14 Aug 2025 20:16:06 GMT  
		Size: 6.0 MB (5996905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8eebfa1d461bc7fc6829d730f39ab328e2f4776fd5bafec8e788e06493fb404`  
		Last Modified: Thu, 14 Aug 2025 20:16:07 GMT  
		Size: 53.4 KB (53394 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:90d8048e1790c85ab3355d7c9951d1053204c174ddbbb2320f16d53581f3ca85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164521817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d236cc5cf6a81f7d950c8d2108964ef855076f54ce4bd4e614f7714d1ed141`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Jun 2025 18:27:47 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV GOSU_VERSION=1.17
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV LANG=en_US.utf8
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_MAJOR=16
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PG_VERSION=16.9-1.pgdg120+1
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Jun 2025 18:27:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Jun 2025 18:27:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 06 Jun 2025 18:27:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Jun 2025 18:27:47 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jun 2025 18:27:47 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 06 Jun 2025 18:27:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6c30648f10140423dedad94d980ec43d531a9cad0983059ff739bb9b52a33f`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ac9590e0ed955da24f366c054364cf8ba0c10685c2a11926f9130d96dd2ef`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 4.4 MB (4391026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610383596c1fcdd9ad52eec420a313e89a0b3b8e9b9eec4a9c97875fa3199e0d`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 1.4 MB (1412789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968418c0a002c3f87fa669b14de23f59d9a339200e3b6e12866ab5eaefe04843`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 8.1 MB (8120490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c87bf03e6298d0eda03dad7a991ef95e36418ce316b1cab732a6c5aaf20b9c`  
		Last Modified: Wed, 13 Aug 2025 11:43:35 GMT  
		Size: 1.1 MB (1096806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e80fccf7e254e617a490a5e480bf0a7d998d006d09d137c184187e9db82e9c`  
		Last Modified: Wed, 13 Aug 2025 11:43:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0382bed70396ec99ad734fded83f746496510f544ac4570bbc14cf5ca09f924`  
		Last Modified: Wed, 13 Aug 2025 11:43:34 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8347a498ff173015142d9ec166573b81bbf8f75ff95e3a9a578bdfe8ccf22479`  
		Last Modified: Wed, 13 Aug 2025 13:11:04 GMT  
		Size: 122.6 MB (122592115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d649cbd89bfc488adb63d1a58016794498256fcf0cf7a792fee3a1952d0004cd`  
		Last Modified: Wed, 13 Aug 2025 12:23:24 GMT  
		Size: 9.9 KB (9922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903ff11394ac4218f3b5baa52cd3fe41e8ed70a1db4c35d1f2418c769754515c`  
		Last Modified: Wed, 13 Aug 2025 12:23:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9b4388f48398a77c96ec7532fd9919328c871e154a2888224f9087ac8ef207`  
		Last Modified: Wed, 13 Aug 2025 12:23:30 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492fcac67b64fa097b8e1142a6ad6ea06eafff9daa23c8390fa3e6072e88017`  
		Last Modified: Wed, 13 Aug 2025 12:23:33 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a67ca550f84db8233c89e229fc61e1f73547e678911d463071c45de12798e2`  
		Last Modified: Wed, 13 Aug 2025 12:23:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4e442b6fe2cc9ed0cb8541edb84162107ddcdae943b44cf9825e70a692b94160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6055572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a52d91128ce028acd07f70ca775bc78fceb6dc5908d3e2ec6104771e912ce4`

```dockerfile
```

-	Layers:
	-	`sha256:c61309cea89afb5da3a1b26d1934eb5db99e4e55cfe64b5c2efbbac7ac31c0e5`  
		Last Modified: Wed, 13 Aug 2025 14:09:47 GMT  
		Size: 6.0 MB (6002234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec244ecb2ec606dd9917c549993c6a507aa9e40bd9679811923c21d6c53b44a8`  
		Last Modified: Wed, 13 Aug 2025 14:09:47 GMT  
		Size: 53.3 KB (53338 bytes)  
		MIME: application/vnd.in-toto+json
