## `postgres:14-bullseye`

```console
$ docker pull postgres@sha256:12bc86431663507120079805ef69b1a701069e1f7d9cec249682122f1015e82b
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

### `postgres:14-bullseye` - linux; amd64

```console
$ docker pull postgres@sha256:a9b24ed9f3292e7bfcb7b03af13ef738f5a0dbf572dd20d3703f56ccf5e8f505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141769123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d624bba2309838b2c08032ad6e74782397411071818ac1995c13e02022db5ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:31:12 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Thu, 09 May 2024 18:31:12 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12-1.pgdg110+1
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dcfcde5031a10de13dcc94edc445e5887918fc54e94618ee317ce8d64219a1`  
		Last Modified: Thu, 13 Jun 2024 18:24:13 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0705fc1abd3e56bf8ff54259ba980b3f2717c046e237dbeb4c30471c7ee2a748`  
		Last Modified: Thu, 13 Jun 2024 18:24:13 GMT  
		Size: 4.3 MB (4308184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac08dbde45f881eabd5cdb55892856a082457be037e2323078d9d4520110b09f`  
		Last Modified: Thu, 13 Jun 2024 18:24:13 GMT  
		Size: 1.5 MB (1473526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bae10b1875a6d033a56cabfbf22d97235f57880b9050bb554ba28969019e5b1`  
		Last Modified: Thu, 13 Jun 2024 18:24:13 GMT  
		Size: 8.0 MB (8045838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1193db21c64e5ae749cf7dd650e074a0f5427bd4c2cf0e62bc80662ee6ddffff`  
		Last Modified: Thu, 13 Jun 2024 18:24:14 GMT  
		Size: 1.0 MB (1038347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7e97bcd01361c1203faaedef7ff8dc5c04d725ba3dddd9e0dbf528e4bab83e`  
		Last Modified: Thu, 13 Jun 2024 18:24:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53490f4dae24cad0414e7751631723267b6e7f3ab4836df2c8664ee31b910e28`  
		Last Modified: Thu, 13 Jun 2024 18:24:14 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd74e39c90fc8d19ee4250ff1b494ff9eb3481a1babf9a65db17673126af324`  
		Last Modified: Thu, 13 Jun 2024 18:24:16 GMT  
		Size: 95.4 MB (95448818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bb064e2982983e6e015fa2fe961efec49d9a2ae384e95f46d95906b496382c`  
		Last Modified: Thu, 13 Jun 2024 18:24:15 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff19809177ecaceecf2c33751b8fd945e2e70287c8df80ba6b1248af7e8a094`  
		Last Modified: Thu, 13 Jun 2024 18:24:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0b543e97fd1d425b3e86e53e2ba94daf81307cc0ef0ca9017ac89590ff558c`  
		Last Modified: Thu, 13 Jun 2024 18:24:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489c31daab7f883999e19232472729779f7067ae5ac26e0af15549898aaf153`  
		Last Modified: Thu, 13 Jun 2024 18:24:16 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ba91633893ad067e94b33c8588830dd668043acf202c7ce48318ed3eff18a9`  
		Last Modified: Thu, 13 Jun 2024 18:24:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:e4964f8472ae8bbc40b544feca7dabe604174b56c5cf05110c434e4427fcb181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb81d6d9135b882456bb2bbdcbf5a64b0d4e3af76d497f78649e1f69aae9478`

```dockerfile
```

-	Layers:
	-	`sha256:ac6f29003203381d075706621089622e844e8eb9fbad33a4ef65f1e7aec41961`  
		Last Modified: Thu, 13 Jun 2024 18:24:13 GMT  
		Size: 5.9 MB (5851149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a00c363ced1bcf696a635a4592bd323ae2fbe47d31c5015790e52a089c7648d`  
		Last Modified: Thu, 13 Jun 2024 18:24:13 GMT  
		Size: 53.9 KB (53924 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v5

```console
$ docker pull postgres@sha256:4a8842687ec3166b06f3f1b0ff4e1bbf856f42b6e70f3aec040ec6076a3f5c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134605672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935041cc7e048019fc48fb0b5b4cd1b921bcdbf48ebd41cdc2d494838f2024d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:31:12 GMT
ADD file:78cff0ed53bbaaa1d7680e733d50b8fc9042e257b78718ad822f9ac57a5d1dbb in / 
# Thu, 09 May 2024 18:31:12 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12-1.pgdg110+1
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f8a34d14f57d3fcf2d97b9fc0fb4439a2d00afe9411fdc788629eb4074186288`  
		Last Modified: Thu, 13 Jun 2024 00:52:21 GMT  
		Size: 28.9 MB (28936731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91482f2667a2ee602bcd9d22d841f2d1f93424a77a4d9cdbeec791b23ab9a44b`  
		Last Modified: Thu, 13 Jun 2024 20:44:41 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9443af51938bde9947f82821150bf5b7e65c18e451a8f17f5d56fad380f5424c`  
		Last Modified: Thu, 13 Jun 2024 20:44:41 GMT  
		Size: 4.0 MB (3991632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f459cb1eb2ff5cf8f49c1c12823aa250b7dc2a6dd575e0b753bdd54df660d3`  
		Last Modified: Thu, 13 Jun 2024 20:44:41 GMT  
		Size: 1.5 MB (1450639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c64a0172ff1ae12ed668caad303acdecc56642efa735304656265a7776964b1`  
		Last Modified: Thu, 13 Jun 2024 20:44:41 GMT  
		Size: 8.0 MB (8045741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7d510a7ee2896503cadca5ed4a55fe4b8cf6ef1be243df775bc4c91b5e580b`  
		Last Modified: Thu, 13 Jun 2024 20:44:42 GMT  
		Size: 1.0 MB (1034849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88332254e20d49fd6cd4fb1b02c7b586bf8d5fc7048dc9e4a225e7dbfc390d80`  
		Last Modified: Thu, 13 Jun 2024 20:44:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ed0cce26b2b70175dc92d13db4bac90e88d571e509156ecec8b42dd41d8574`  
		Last Modified: Thu, 13 Jun 2024 20:44:42 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bb43cb30fd4ff387c753d6a014f0583c05a1abf5ac86dc6617726554e4fb42`  
		Last Modified: Thu, 13 Jun 2024 22:18:53 GMT  
		Size: 91.1 MB (91125710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa196539699663da3bfc14632d7ba2c3e98729e7f6c6358def4d3ce8c8c7ea3`  
		Last Modified: Thu, 13 Jun 2024 22:18:50 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75917415aac729e1a49e7afc7c37b8bb679bc156511369dd4a4e64ab5b478f9c`  
		Last Modified: Thu, 13 Jun 2024 22:18:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b6d9ce3f65d18c2fbe293c0a7945a40c486a478e2f98cb09f5991c0d08b51f`  
		Last Modified: Thu, 13 Jun 2024 22:18:50 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91a280b6011631f4c7c9cfdb42a7315455e67f6f28687e68fa358808d4e38d6`  
		Last Modified: Thu, 13 Jun 2024 22:18:51 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7899851f355768d666c403c58d6060782c5e5fcbac08452e9504c6dff64b465b`  
		Last Modified: Thu, 13 Jun 2024 22:18:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:d5552893ea68cc5af0386a3a8cb1f0d2aab8a2bb94255b06e347321629d227e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5915115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd8245a487d8f5e64df11ff72ab8568937e5e146aa6f3fef2ab2939980bdfd2d`

```dockerfile
```

-	Layers:
	-	`sha256:b68202afe2334b614efe82495927f492c8de7e74ee7ac9d0baba28b1a5ac5da6`  
		Last Modified: Thu, 13 Jun 2024 22:18:50 GMT  
		Size: 5.9 MB (5860994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90871edb2905cda7e81e6570fd40346b610f151f2eb9b21cfa35767f00d8e771`  
		Last Modified: Thu, 13 Jun 2024 22:18:50 GMT  
		Size: 54.1 KB (54121 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f1bec0919979d755208bc8888941be5fc07fdd1e9ff5aaa4569b9f56be0ffad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129732389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfddeb667808464b157b308d55a726d9e05fc5afa737960f6bf01a12c66447b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:31:12 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
# Thu, 09 May 2024 18:31:12 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12-1.pgdg110+1
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2931fa25f098cfb85a9e2ab63b32f42e0a38d948de08037ebaf41564215be3f`  
		Last Modified: Fri, 14 Jun 2024 01:31:38 GMT  
		Size: 1.7 KB (1677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af708d144a1736f39af6b983593190d32710b24784ff0d548a5ff97684bfef9c`  
		Last Modified: Fri, 14 Jun 2024 01:31:39 GMT  
		Size: 3.6 MB (3601619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126dbb3b6030510a22eabb64c1c168ac4ff657d79a006f5824746e1c2fd5e340`  
		Last Modified: Fri, 14 Jun 2024 01:31:39 GMT  
		Size: 1.4 MB (1440825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bacc00ecda8352e7b3e2312653e32de97ad93d9ebc13319ae22edea2b44667`  
		Last Modified: Fri, 14 Jun 2024 01:31:39 GMT  
		Size: 8.0 MB (8045802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55803590f5e2c3a873bdebf5238649577ec4b5f0d628ee528df9ac7359fd8ed`  
		Last Modified: Fri, 14 Jun 2024 01:31:40 GMT  
		Size: 908.7 KB (908660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b80780e0a0bbdd60caaeb103723853e5e2db82c08827db79ab4a0cec61215ad`  
		Last Modified: Fri, 14 Jun 2024 01:31:40 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d224aa4d57d0a54614dfc9293cd5826927f9325c08c29f8cc32186695f06631e`  
		Last Modified: Fri, 14 Jun 2024 01:31:40 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352001bce999a13e7def96eb49e9a97bea68bb9d6e69f8878a0123c7c762b0c5`  
		Last Modified: Fri, 14 Jun 2024 02:59:35 GMT  
		Size: 89.1 MB (89120609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e3292ea291b1d5357d7a13416a64e801c7c45b0ace720f532b89fb089ce2c1`  
		Last Modified: Fri, 14 Jun 2024 02:59:32 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e294253cb8d70b2f04fe22bf1b6fab810c2afa2b6ae5370d58cbd7b4e9834928`  
		Last Modified: Fri, 14 Jun 2024 02:59:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e1da0841bc3ac6c4f254a4328dc025b8efd04345b1cb6a4198ef97d58a4ba3`  
		Last Modified: Fri, 14 Jun 2024 02:59:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c68825a6d6eaa5d848e8fdba5d584acd021f686dd03eb0bed2d2289ccbf814`  
		Last Modified: Fri, 14 Jun 2024 02:59:33 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5efaa51b3bfec77818fce24289edda5bee554a79da6a4f376cd1536fb0a254`  
		Last Modified: Fri, 14 Jun 2024 02:59:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:936eb26bc163aba8f65126a7be6dc5a121304e4e5bf9f7e135324de50c603042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047e77f9f7983efc42933d47d428192a467d8b55b1d757369775f3064cd7e94e`

```dockerfile
```

-	Layers:
	-	`sha256:0a4a38dac09767bf8f292d70480e0ce0269408e9bb3f89b99060e0e69010d99d`  
		Last Modified: Fri, 14 Jun 2024 02:59:33 GMT  
		Size: 5.9 MB (5860766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf20dabd4f52662ee0c79e9fe5858edfe44da75c1afe79a7fe5e79b68c81647`  
		Last Modified: Fri, 14 Jun 2024 02:59:32 GMT  
		Size: 54.1 KB (54112 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:2ded1c1b8d3b4c5176c69f5d5b108f3f8bf8c89c96eb137db3de1b2eb3fe39c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138188334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67993e3a5e284682d564bc05923b03eb85bc2b2bb38f8869de3b62996b63b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:31:12 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Thu, 09 May 2024 18:31:12 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12-1.pgdg110+1
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb28ca68ecfc3c03e505d7540fe02a380ef93dfab58facb8e40674c120c35de4`  
		Last Modified: Fri, 14 Jun 2024 00:42:15 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbd6a6f4ffc2265f4e7190df83c0ebedc51b62f181cc5519e69ecec44873012`  
		Last Modified: Fri, 14 Jun 2024 00:42:15 GMT  
		Size: 4.3 MB (4312765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1c1745601ba7fc2a64b9a3ad7f1a22c9eaa21bb0b557adafa57fb5199eccf0`  
		Last Modified: Fri, 14 Jun 2024 00:42:15 GMT  
		Size: 1.4 MB (1405900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1295861d7380761e55795e2be158e67ddce9cab82d0a361b18ec1b4987da6aa`  
		Last Modified: Fri, 14 Jun 2024 00:42:15 GMT  
		Size: 8.0 MB (8045779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c5f02f0c267ddda7903b8d1c3fd583d4c253988b1bf1372e28704efff61982`  
		Last Modified: Fri, 14 Jun 2024 00:42:16 GMT  
		Size: 1.0 MB (1026604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514b106d79ccc7563e64bcef8d04a100acdafb5f318590284727ecbf6637d1c8`  
		Last Modified: Fri, 14 Jun 2024 00:42:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1ec2b6225396907d9fa7a99e8243c694ee1e58117218df87093b57e0130d43`  
		Last Modified: Fri, 14 Jun 2024 00:42:17 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbfc437178fdce3c4297c46aad55de3124a3145e3f185fe57a7e908b5b09611`  
		Last Modified: Fri, 14 Jun 2024 00:58:32 GMT  
		Size: 93.3 MB (93289940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6e88245e7384af7d6ba28ad62771452f479dfcafc7cbed1249c9b986598a5b`  
		Last Modified: Fri, 14 Jun 2024 00:58:30 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d56f5f6f2393968dc7dbdef577b2aa625efab0da85e1ff66eb6ae9f9d08e048`  
		Last Modified: Fri, 14 Jun 2024 00:58:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9d6208c671da3271aaddddb37be35ac9f8bf45a9b8dbe7a03d0f570c7b4b81`  
		Last Modified: Fri, 14 Jun 2024 00:58:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ebf915079e21192608cb5516b396aa81710c327f1e42f0d7a75d1f8e9d5b43`  
		Last Modified: Fri, 14 Jun 2024 00:58:31 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e44e9c7cb91a0c2da3748fe605691a4b366ac15c92bfa1811e3d4b9fa91a2d3`  
		Last Modified: Fri, 14 Jun 2024 00:58:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:656c903cc891dc03454b8c708a8d8ca6670f45a8c9c73cd2f737b1966c5d462f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5911647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23d754a379ab1723d07415866b9636f4dd191b72a7473c993d2a575538a2fa4`

```dockerfile
```

-	Layers:
	-	`sha256:3c751db90db06632244287cc3d22260493f4e582601793118ec5625bf55fadb9`  
		Last Modified: Fri, 14 Jun 2024 00:58:30 GMT  
		Size: 5.9 MB (5857439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dc6b35d8f7155311399d3dbf487996ce580b14593b5d733e8fd3473fc764725`  
		Last Modified: Fri, 14 Jun 2024 00:58:29 GMT  
		Size: 54.2 KB (54208 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; 386

```console
$ docker pull postgres@sha256:c1958378be382ad6b3c748491adb5fd1c7716c73ccc5bede1ed352ac19b87d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144361744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19bcc7cfe3b3b3480d542e6661d37378fa8acf349863708a9d0f3737270c544`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:31:12 GMT
ADD file:ef80ad838dee1f170442a02f8d0808e624e7c317df766c49aec042c1f3ac4732 in / 
# Thu, 09 May 2024 18:31:12 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12-1.pgdg110+1
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:71e749b27156c50e0706f9267afd1ca9fb38d6272a353964948602fb62336fd8`  
		Last Modified: Thu, 13 Jun 2024 00:44:08 GMT  
		Size: 32.4 MB (32424179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906674da477f8e6611b235ca2c0949b7cfe39b8f50a633719f6642eda3a3512f`  
		Last Modified: Thu, 13 Jun 2024 02:12:14 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26d725a26b4fcf921871c6cdaf49773e2d00fd47d7b5d2535a441dae3bfe7ac`  
		Last Modified: Thu, 13 Jun 2024 02:12:14 GMT  
		Size: 4.7 MB (4719623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40257714d16af02f61c4802990cd77d0fc2bfaf9735ddaf76a04392380b83430`  
		Last Modified: Thu, 13 Jun 2024 02:12:14 GMT  
		Size: 1.4 MB (1449297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16898659d5d388fdb538d21ca5e489abbb5621bd7b9043d70b65b388e726c3fa`  
		Last Modified: Thu, 13 Jun 2024 02:12:15 GMT  
		Size: 8.0 MB (8045731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510d9453e71661a08db881080716996bd62492ccacd028269476cb18b0a4aa1d`  
		Last Modified: Thu, 13 Jun 2024 02:12:15 GMT  
		Size: 1.0 MB (1028888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2effa40444a8a115fc63e24f248990aa7ed0136f2ffa92fdc6b50ad32eba04d2`  
		Last Modified: Thu, 13 Jun 2024 02:12:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9902fb69ed7f544415e5720b8138b494536c29663883681aed28e93299df381c`  
		Last Modified: Thu, 13 Jun 2024 02:12:16 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c6d71849a8744ea1d155df80b0295d05d8d27b93e65fefd415096ca2866fd2`  
		Last Modified: Thu, 13 Jun 2024 02:12:19 GMT  
		Size: 96.7 MB (96673646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47164295734322aa81d9b657c54af84cc1765a63faada8f693532e23f81526f8`  
		Last Modified: Thu, 13 Jun 2024 02:12:16 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acff9c3cf3e1fe1ecdd7ba47dc6b615eb22f8b18d4f9de8c6f23e637b0451f3`  
		Last Modified: Thu, 13 Jun 2024 02:12:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3913d3b58fb5a55c08a572ac867cfcaaa754b750629f5783ff5af2ca7154ca`  
		Last Modified: Thu, 13 Jun 2024 02:12:17 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e5eca465300367a87de9a98e99684dfce6791a3f340c87078bbc612b9dec49`  
		Last Modified: Thu, 13 Jun 2024 02:12:18 GMT  
		Size: 5.4 KB (5427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2014299a34c6aeeae63f07a60e5c6fec8ecb8f0e8733c4e1f8aa06a57f2c8ff0`  
		Last Modified: Thu, 13 Jun 2024 02:12:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:bb577221344ae146b5af039c378b70069721571d14ef0a7f418d983aef722ec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5912197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc995f5d670df5026f71803789df27ffc0928ed2fe45fa8a7336c7e1d6152fb`

```dockerfile
```

-	Layers:
	-	`sha256:d01cea4df3959a174e4027f23ff0ae0b9fa01a373d8a40fb23dbb2508432d6c3`  
		Last Modified: Thu, 13 Jun 2024 02:12:14 GMT  
		Size: 5.9 MB (5858314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c755d1cd0f9d161a8e8966258d1ae246ac797f22ec833a82440528edcac71ad`  
		Last Modified: Thu, 13 Jun 2024 02:12:14 GMT  
		Size: 53.9 KB (53883 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; mips64le

```console
$ docker pull postgres@sha256:02676083bb7fe9fcd861bd514ac428183fd57e199e533508ef7e31cfbb7407f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (136038623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63cd82ddccccdbd56b523ae9dd32f30e1d124719ac4ac9b6ff6825a4a6dd5983`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:31:12 GMT
ADD file:ec3acf4bc32b149c2b67d1b2c5f3a6d1f16fbae266ac16c115e1fca276b970e7 in / 
# Thu, 09 May 2024 18:31:12 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12-1.pgdg110+1
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:38917083d8284ce1ec7533351600bab5d64f8295f3edc5dc651be130fb9a4bd4`  
		Last Modified: Tue, 14 May 2024 01:23:44 GMT  
		Size: 29.7 MB (29651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aba106760195f9fa030021197630ba635b05c4647c2ea02f902d3175e6072e9`  
		Last Modified: Wed, 15 May 2024 12:03:06 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a013914fe54cb7a85c574d42774dd74d4e118513f35c2a493ed1c8d466443201`  
		Last Modified: Wed, 15 May 2024 12:03:07 GMT  
		Size: 4.3 MB (4308318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bb9ff3153bacdce838e74d516501e67381c21b7d89ddb2808ce5516eded2a7`  
		Last Modified: Wed, 15 May 2024 12:03:06 GMT  
		Size: 1.4 MB (1360875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b75d6cf1960b36bff0ecfba1e74c765f4d775db53c52c3c49f929260d07e1b`  
		Last Modified: Wed, 15 May 2024 12:03:07 GMT  
		Size: 8.0 MB (8046107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8a1178596bea097e6b4b01f8cd18d4f0caa71002ee5fc9a641a27be2fa9bc1`  
		Last Modified: Wed, 15 May 2024 12:03:08 GMT  
		Size: 1.1 MB (1090277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1465b7c1ea3830dd65fdad4015bf4efd0535db8bbb304049c89025696f7877ed`  
		Last Modified: Wed, 15 May 2024 12:03:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9635669a94122c34c7a42e34d3d9e1b1898723a1b11705647f973bf1d2240f0`  
		Last Modified: Wed, 15 May 2024 12:03:08 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab006f009ce12c3ed1ed980990271b894f9677ba9f2c2494f15c90adcea7605b`  
		Last Modified: Wed, 15 May 2024 12:03:17 GMT  
		Size: 91.6 MB (91560806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a05cede6d9d2f3a4769c8bd2d86f5ab30ed0130d2682bdf79b78d4c26d8d5d`  
		Last Modified: Wed, 15 May 2024 12:03:09 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74a9a47d5e50c1852682dab09abf0bde17b32354af0c2f74c782348afdf9dff`  
		Last Modified: Wed, 15 May 2024 12:03:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e90e6d37538121072e24f0a2693c073653981c2b497ce5beb281f39b5a93c1b`  
		Last Modified: Wed, 15 May 2024 12:03:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5784b814f7aa2cdc0e3eb52fc4888aa0ab3b162e1021da0b6e3fe9a8acce4b93`  
		Last Modified: Wed, 15 May 2024 12:03:10 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823a84863e319070bdefa33cc9165f52ac5ad702974468cc36d4f9b38e4ad528`  
		Last Modified: Wed, 15 May 2024 12:03:10 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:51259cac33283fd586dd50c78d707ec1c925496879ec180efaffcd55feef5d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 KB (53895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ffe14e1d9666a70b41ca0ca71cc0296d59f20af2091d4eca57d67625d1fd77b`

```dockerfile
```

-	Layers:
	-	`sha256:aff7e319ffe777854c8416b43209c45a2e5d0a2643d5a780b10ab2f3e473e12e`  
		Last Modified: Wed, 15 May 2024 12:03:06 GMT  
		Size: 53.9 KB (53895 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; ppc64le

```console
$ docker pull postgres@sha256:240dfafdb981b291b0031759886b00fcefbcf00d77b97261ad7a2f0d6972e86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152673429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139383c80788bf0edc732b0ec19c4aaaf332e5588b91538839d20c9b161b67a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:31:12 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Thu, 09 May 2024 18:31:12 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12-1.pgdg110+1
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1235223a318cb62554e65c2d1f1a498b9792066e504a7b470bd5fbb4544df604`  
		Last Modified: Tue, 14 May 2024 15:40:49 GMT  
		Size: 1.7 KB (1681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e97dae3d796b39ab1573db218f4e5250543a4f6fd855a2f6d326ed88d7770d`  
		Last Modified: Tue, 14 May 2024 15:40:50 GMT  
		Size: 5.1 MB (5137874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e0c9e92539e0c2ba742726c009111c147f86960a9bf599bf04943ce1693870`  
		Last Modified: Tue, 14 May 2024 15:40:49 GMT  
		Size: 1.4 MB (1394903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06efbab62c9510c70a3fea123ee45c56fdbee1e768283666836cfe5710ef1f4e`  
		Last Modified: Tue, 14 May 2024 15:40:50 GMT  
		Size: 8.0 MB (8045878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974e84a835bb377946282ae200ef4e73b477298eb1d7a36016fa33ecdf176483`  
		Last Modified: Tue, 14 May 2024 15:40:51 GMT  
		Size: 1.2 MB (1197549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6669c23fcd244c2d8fe9a1adc5afd4f63cf65be06017f9b53c1b7ba040cab900`  
		Last Modified: Tue, 14 May 2024 15:40:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1647d546bb5750047f27efd7e3a9e79499c656a4f85656497605d0766bca97c1`  
		Last Modified: Tue, 14 May 2024 15:40:51 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5448e4596b1cdd183e42a4effd8816c289330c1577e8af8f55639433f2def4e`  
		Last Modified: Tue, 14 May 2024 15:46:54 GMT  
		Size: 101.6 MB (101565697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80454c2832699cc378f9869516c0cd2b36e54b8bb9a38055cb13789b10a962b3`  
		Last Modified: Tue, 14 May 2024 15:46:50 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36d0c05bb3f0598607a8e5113be191e00912e176e3e38b32d5c42c92a24a7b5`  
		Last Modified: Tue, 14 May 2024 15:46:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fd1d0a04161c2fc3666ddac7f3d00586d73469ea4725df3a526629f59716f6`  
		Last Modified: Tue, 14 May 2024 15:46:51 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30945bb891f706b97a7cb3857a8ee87ed11f06dfa4247070dd39cdc99f56d75d`  
		Last Modified: Tue, 14 May 2024 15:46:52 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e8fbf71a44eb062458cb61ea2889eaf1ab2e2c6abf143fa12d247c5c53303`  
		Last Modified: Tue, 14 May 2024 15:46:52 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:b6b63ed3da6ba6b5fc4bbe2e645eb7b1230e1ccddfd943b801859da45a570634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5912211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0209d6e5419265ee1d983394ea7dbf59c2030867b4c032174b60f2205e79fe`

```dockerfile
```

-	Layers:
	-	`sha256:6a784432c23de7332cd817321efbca3037a0f795ae91971a8c5900818d3568b1`  
		Last Modified: Tue, 14 May 2024 15:46:51 GMT  
		Size: 5.9 MB (5858282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b201add896829d54867af2a4f16483752642609686de78d9254b6e3a9138fa0a`  
		Last Modified: Tue, 14 May 2024 15:46:50 GMT  
		Size: 53.9 KB (53929 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bullseye` - linux; s390x

```console
$ docker pull postgres@sha256:44b80e574cb5929aa96818427e33c3143984c087ccd2500b547c5badbf9d16aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146169262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb22316ce66ec6ef1b20c288629acf0552c01da052cb20013dcfd1645f6dd48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 09 May 2024 18:31:12 GMT
ADD file:dbc45f2c1dc4ae2fcf0e05b8c9401406afd0f7aa3623659e470bb7d0fb97f9ec in / 
# Thu, 09 May 2024 18:31:12 GMT
CMD ["bash"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV GOSU_VERSION=1.17
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12-1.pgdg110+1
# Thu, 09 May 2024 18:31:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bullseye-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b9966e11fe1c4138e9aa4f0356568463c21e36009b72062413bb596e0e57738f`  
		Last Modified: Thu, 13 Jun 2024 00:48:17 GMT  
		Size: 29.7 MB (29673762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460c230adaace3949645878940d610c4ce38c0e447f048b02217e91eb050fec3`  
		Last Modified: Thu, 13 Jun 2024 12:23:54 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bac93d97a40e00dd3390048e4d534c3ab50ffd81ef933870410b6e8dc4ec471`  
		Last Modified: Thu, 13 Jun 2024 12:23:55 GMT  
		Size: 4.2 MB (4200281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0793852fc1f76326929ea80fc34bdd2d26d7ef7d25089b639170768d4e00b42b`  
		Last Modified: Thu, 13 Jun 2024 12:23:57 GMT  
		Size: 1.4 MB (1439447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408bdc779fb25812e76e6855bdc1e12f5b966080f5c04c1d824ceabb23c6cc80`  
		Last Modified: Thu, 13 Jun 2024 12:23:55 GMT  
		Size: 8.1 MB (8099613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419d494d4895e7ea22af6a94b4ed70469bdde216801d7d02da6df9cf27db64a7`  
		Last Modified: Thu, 13 Jun 2024 12:23:55 GMT  
		Size: 1.0 MB (1015255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca5e5eca589d99e7509c8665b60a932cbfd1c44dc4561551a29284bce702b63`  
		Last Modified: Thu, 13 Jun 2024 12:23:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65306f81e991db54de503312aa99f227234fc3f95f0fb208d6b7e9e6175c49f`  
		Last Modified: Thu, 13 Jun 2024 12:23:56 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601d98f8a77fc29c7e786f5fb1956dfdac4c96ab056b77279d7d6b63173f3160`  
		Last Modified: Thu, 13 Jun 2024 12:32:55 GMT  
		Size: 101.7 MB (101720526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d6fb48087325227556d08f89cdae090607b7e3cce09d2902aa17146f75de83`  
		Last Modified: Thu, 13 Jun 2024 12:32:53 GMT  
		Size: 9.5 KB (9529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793988c1b752c7a3bd240ac0b840f156cec45aae42dbf995026bb3a16297bec7`  
		Last Modified: Thu, 13 Jun 2024 12:32:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2ff2c05fd339edbb9efa47b833dd0ed8ee75093a0ac442b61d433cb9c07fb8`  
		Last Modified: Thu, 13 Jun 2024 12:32:53 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da93d30645ada17c2fd1ab8ee28e225be5c5a14fe27a2852f334cc65e8931ad`  
		Last Modified: Thu, 13 Jun 2024 12:32:53 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4875183afa55ea11f4c7a60c5b1f66b58b311b548add945665c8e7ede67234c`  
		Last Modified: Thu, 13 Jun 2024 12:32:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bullseye` - unknown; unknown

```console
$ docker pull postgres@sha256:98c5bb8463ba8190ed915fc903caf2dab8c1f2800cf3d094a8f1b706838d2139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5904056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f6b66bacca8b579aec4f3e2696e917a441b30a416cc32540b6263784a66c55`

```dockerfile
```

-	Layers:
	-	`sha256:671b1f2989ab1cd8b688685e9e7f7fc638a976006616d8abec465f338690bcd7`  
		Last Modified: Thu, 13 Jun 2024 12:32:53 GMT  
		Size: 5.9 MB (5850126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a6c4051c77a96fe54cb8d43c925f841810d6536e58c0fb373394c3fe568d53`  
		Last Modified: Thu, 13 Jun 2024 12:32:53 GMT  
		Size: 53.9 KB (53930 bytes)  
		MIME: application/vnd.in-toto+json
