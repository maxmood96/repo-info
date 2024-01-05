## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:cb45f8bb9040b82351ec4c90ae91cb5b6cf0c6dea99f50c44d80e116f72a3b6b
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

### `postgres:15-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:0d3f08b11b1bf67c6ed0314116bf52395381f6305c91211ea60deddeaaa09881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150934010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d89a2abe0dcb3d5e3bd0b72098aebd4af83e2fc34b480f2a2beaca0cedca9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc21908f55ddc70c693907f5c0e7a95fe4388fcbccb47d04ca8ba0c8eecf750a`  
		Last Modified: Fri, 05 Jan 2024 01:54:33 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0633c239cd6c37809edaeb718532ccc237c9fdb103f02a6655b620704de2c019`  
		Last Modified: Fri, 05 Jan 2024 01:54:33 GMT  
		Size: 4.5 MB (4533194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29236a1c421b00c1b55977e065ff61eee05129145be7a7059dd1681ac5011d7`  
		Last Modified: Fri, 05 Jan 2024 01:54:33 GMT  
		Size: 1.4 MB (1445970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a429ce5b1b08980d883263319e1412570bce5a234fae6d0aab0b0278516ef25`  
		Last Modified: Fri, 05 Jan 2024 01:54:33 GMT  
		Size: 8.1 MB (8066074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f2d698b72abd3637253f2ea5495f5f0daabcfaf1e535bd952f12a26a7fd284`  
		Last Modified: Fri, 05 Jan 2024 01:54:34 GMT  
		Size: 1.2 MB (1195879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82ef769236bad36328f093072cf0f2c45f63d2d35ec20a5c1720429b98527e0`  
		Last Modified: Fri, 05 Jan 2024 01:54:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aec4efdc9c6efada635029998015a8068937d84b189b1aef9314ddb1ff356f`  
		Last Modified: Fri, 05 Jan 2024 01:54:34 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997449cb95195b91c35e02d34dced658a2695855ea774abb662c4e2c8018afb4`  
		Last Modified: Fri, 05 Jan 2024 01:54:37 GMT  
		Size: 106.5 MB (106546816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5e5974d4fcf8914e2b3d63de9a7838c37411ab19f005a9b3cb9e9bb54e4bd6`  
		Last Modified: Fri, 05 Jan 2024 01:54:34 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f6c16f2928f538e78ebf962decbe450a9f3cb63be978842099fc34f9ff27a1`  
		Last Modified: Fri, 05 Jan 2024 01:54:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6fe7e36cddd0295264bef69216925e8b6d5daeb5597e8ddb6f5fae69f569e1`  
		Last Modified: Fri, 05 Jan 2024 01:54:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a23c6557ef4f90575b74b59ce2dd06367d6aabd292e541d952689931f8a920`  
		Last Modified: Fri, 05 Jan 2024 01:54:35 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ed19a7b0b3ddbb7aabcaa1392e10f9c6eb08c8caffe240f2ae742a6c55a5af`  
		Last Modified: Fri, 05 Jan 2024 01:54:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:cf85e501e67b7e9e725eb856b9c6f5bf2b6d48068e67c4a04d42a6ee50594e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4950233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f854eb2c82fd4270bb23d3a800c166f1097f822ec5a91b150ca137a851b5d7`

```dockerfile
```

-	Layers:
	-	`sha256:a7118a852de3bf64a3a4601106a2fbe3f70a3e2ba10f5d16b954e80f09e44886`  
		Last Modified: Fri, 05 Jan 2024 01:54:33 GMT  
		Size: 4.9 MB (4895608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88015391c4c94fcdaee116a3ea3ae5f6b84c0f365b237667520677257fc213d`  
		Last Modified: Fri, 05 Jan 2024 01:54:33 GMT  
		Size: 54.6 KB (54625 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:39575427620786df1ecb6e5b6dfc4181a92ee417d526bf7028236c896896a0fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143599786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082b4ecef8330abe8c0c9b080dfaddcead2b86ad405a054a1820ae9c7fc98775`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:22 GMT
ADD file:9503ab966c9dd707eeccc7c2f633bccc94c199f8714ec4ff2c8b54dde3dbabf9 in / 
# Tue, 19 Dec 2023 01:55:22 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1ae9a2844c8c70942d2220553689b62e841cc706d77284fbfedbd770080fd699`  
		Last Modified: Tue, 19 Dec 2023 01:58:33 GMT  
		Size: 26.9 MB (26885440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0b56c3a713f986d961e55417607ff3640e6d06edc859194b8eaca21a757240`  
		Last Modified: Fri, 05 Jan 2024 02:29:31 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b604a63864efd0e0e046820c520d9cb6ef746d0b29eea1fc47265f3c1c3693`  
		Last Modified: Fri, 05 Jan 2024 02:29:31 GMT  
		Size: 4.2 MB (4150606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2685f9d69db4e9bf67679f005b17857ee518287e17b73d26df755ac368ae595`  
		Last Modified: Fri, 05 Jan 2024 02:29:31 GMT  
		Size: 1.4 MB (1423611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e1f87b9e4192533e9d4bd021e96b40d31381e1ca1fc804b28aac5c4a3234c4`  
		Last Modified: Fri, 05 Jan 2024 02:29:31 GMT  
		Size: 8.1 MB (8066241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71989e868529eb66a0b5c1fd075b6d3dd140af7704076e3f2d8aa33325955669`  
		Last Modified: Fri, 05 Jan 2024 02:29:32 GMT  
		Size: 1.2 MB (1194729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa438b7ddb9e411850ffb8463adfbebfd042ca1e74e11edc61edb1c0d6c6bde2`  
		Last Modified: Fri, 05 Jan 2024 02:29:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccd680157e53ea4a248cbc12021c35fdaad5614c4aba0cc9f749f5e65ee8039`  
		Last Modified: Fri, 05 Jan 2024 02:29:32 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ef58f345375cc4a1b50a629eae1828d86e99bddfe43afa4d7f9822c3a47524`  
		Last Modified: Fri, 05 Jan 2024 03:08:17 GMT  
		Size: 101.9 MB (101859042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b494a00690758744a1c1aca45c6812625c232ac207a69bff6a0e4200adc092`  
		Last Modified: Fri, 05 Jan 2024 03:08:14 GMT  
		Size: 9.8 KB (9788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4de82087cd9fa17f741c7a4bcf4c0a1e23d9d9859233e399647cf9b1c97ce5`  
		Last Modified: Fri, 05 Jan 2024 03:08:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab6e92dc6f4517aa06ea9e829722718edc269a1b5ea79eb02916e688af487d9`  
		Last Modified: Fri, 05 Jan 2024 03:08:14 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3f4804004ee1daa2fcfd3d90690e21fbd6e564f54559743e0132ca5fbcec17`  
		Last Modified: Fri, 05 Jan 2024 03:08:15 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c28c47ef73a4a2e73236baa9438f68afa00d4326ddb019cb6e2b6fd4e6bc63`  
		Last Modified: Fri, 05 Jan 2024 03:08:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:183292412ffb5e89fdcd34ac522bafd9a04f737e7218e82f1092be4106eab261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4960739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f244d7e0d9cc4152da62780b9943a6ae83b694ecb05124cc3bc1d4d8dbb3dd`

```dockerfile
```

-	Layers:
	-	`sha256:740ca32aba16d4cbaf072c981e48d4f2cd9f392ca74e9f6242c754b625d5caf7`  
		Last Modified: Fri, 05 Jan 2024 03:08:14 GMT  
		Size: 4.9 MB (4906068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7dfbbe363bb107aafc5ab2a34721b02fbec92ff9afd45a44087579b420a6c6a`  
		Last Modified: Fri, 05 Jan 2024 03:08:14 GMT  
		Size: 54.7 KB (54671 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:307f5794c3c7c1b5a89dfa2ca516573879110eb13b6706b36a63124a64435261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138449778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef0c57a580a0b1bba22e04d8975336369f70849a42ed8dd00277ccfd2ad9195`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 19 Dec 2023 02:07:50 GMT
ADD file:aef112919e7924ad6da32181b1df5099cd692680c104118da3a24cd4dfe55a1d in / 
# Tue, 19 Dec 2023 02:07:50 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:65ab19615c01a3b542f77fadb3bd27872b6a20cba3e9269fb951de36d8fa6805`  
		Last Modified: Tue, 19 Dec 2023 02:11:52 GMT  
		Size: 24.7 MB (24718157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491d66ed0c94e899a5fd8e5a17a823c75c97acb78b022a4f1fdac35cb1688063`  
		Last Modified: Wed, 20 Dec 2023 01:13:17 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c95611529611fe5b899f6c395de27c813b3b277590e4ea2cc7d63a462d7438`  
		Last Modified: Fri, 05 Jan 2024 02:59:15 GMT  
		Size: 3.7 MB (3742396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e9088c91dcb4fe0aa94226449b61c17a8995555392550ab61630a3da1708a8`  
		Last Modified: Fri, 05 Jan 2024 02:59:15 GMT  
		Size: 1.4 MB (1413437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b98a6ab5ffa7420ec94629fee761a9737146b07726c4f44704f3971414f5ab5`  
		Last Modified: Fri, 05 Jan 2024 02:59:15 GMT  
		Size: 8.1 MB (8066148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72277f2a03ab5b0d9560cddc76ddadea5dc44e587ea2b7f220d314a850256796`  
		Last Modified: Fri, 05 Jan 2024 02:59:15 GMT  
		Size: 1.1 MB (1066804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccbd2f7976cd13e78255640b3901fd5c6d24ffea1c470b970c6466733ec4673`  
		Last Modified: Fri, 05 Jan 2024 02:59:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c238c2a3ec4de2ac07e249105a834425b711278a054a7e2d6ee768b15c26e2e`  
		Last Modified: Fri, 05 Jan 2024 02:59:16 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98957ad0615972f3d3903b854b89d4823e3ef2ef7ee93422cd31733902df449f`  
		Last Modified: Fri, 05 Jan 2024 03:48:49 GMT  
		Size: 99.4 MB (99422716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5408ec6f5299e64dd1b8f093e0d0bae83d3f5056b8f77251419e398f6aa569`  
		Last Modified: Fri, 05 Jan 2024 03:48:46 GMT  
		Size: 9.8 KB (9791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe0f465f5adc4d56e63cfcf66957b0bae6643cc5952931b8d0a90be5c152853`  
		Last Modified: Fri, 05 Jan 2024 03:48:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6c05da74cab6f908e42c7c9c797863e67dc6846fa66c687b755a74857a7ce9`  
		Last Modified: Fri, 05 Jan 2024 03:48:46 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd08e8ce084e5c1bb3b8b3f62d066fe569a6e30c0c3c002365c9c84e5e6abf`  
		Last Modified: Fri, 05 Jan 2024 03:48:47 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aa5862b014231c1ca99367204bc4ee416ca3347d47f2472db225b7e43e3f17`  
		Last Modified: Fri, 05 Jan 2024 03:48:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2dde42544b1bbe672311de36349cea22b474d83151da2ca0448f21c311b6ae1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4960651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09234fbba8dc3affe426572e848503dfcb32992236403a8b28e085a8f0eb7fa4`

```dockerfile
```

-	Layers:
	-	`sha256:ae452b43a9688a0792bab6d70f20321174e0a1e6ef87ade2513729be0ed3c938`  
		Last Modified: Fri, 05 Jan 2024 03:48:46 GMT  
		Size: 4.9 MB (4905986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f679875dfba3e4e8df5762a10a4227c9a9564e413039a8022f196c43745207`  
		Last Modified: Fri, 05 Jan 2024 03:48:45 GMT  
		Size: 54.7 KB (54665 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:4956ba2bf9e9d2edf0987a0a31b93bcf012486bb522605e0c0c761b0bcabd3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149124992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdea6953864dec90f5ba6e9bb67211c247b889ad7bfa93ddfc838886d486856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b20a3ade36a25ede5711ca425e17b9c06dd6a996c7084ef14a3e7f52ef03cc`  
		Last Modified: Wed, 20 Dec 2023 10:29:30 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7ec827b618e24dc6701d8176d33e62b8be86a0367564d313ab0e7139eaf42d`  
		Last Modified: Fri, 05 Jan 2024 02:22:41 GMT  
		Size: 4.5 MB (4498675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b28172b826cb8e32985556014bb3c9463110998e2014aeb809b4f245f7f4310`  
		Last Modified: Fri, 05 Jan 2024 02:22:42 GMT  
		Size: 1.4 MB (1377978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dac61d000df1aff9618f0cd58d6be9859f5d4854f9b6efbec11602ad2c9e823`  
		Last Modified: Fri, 05 Jan 2024 02:22:42 GMT  
		Size: 8.1 MB (8066185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1dda37839efa557b408c5b439962a45ae8287354518538e3f51041fc607158a`  
		Last Modified: Fri, 05 Jan 2024 02:22:41 GMT  
		Size: 1.1 MB (1108517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa4474a8b36a5392fe704fa1c9f361ca183253be7b2cde10433bd7fbbd4f20c`  
		Last Modified: Fri, 05 Jan 2024 02:22:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdc6a365216c8ad9bd31fc9c215fbb889c6f3481964969ffdaac5a8d1d74566`  
		Last Modified: Fri, 05 Jan 2024 02:22:43 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1daa2b9ce4ad18e7a0d4f70e95649549045e5596f34d032fdf1215770f3c2b9`  
		Last Modified: Fri, 05 Jan 2024 02:26:27 GMT  
		Size: 104.9 MB (104896250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce19e61ff38133757933499a771a54e9507aa1c2cccb2ca1eeb8147d6b8a8fa`  
		Last Modified: Fri, 05 Jan 2024 02:26:23 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7031fce9d760db84d4d54981c30e1c4735be135050c7362d71abd12bb38c2c36`  
		Last Modified: Fri, 05 Jan 2024 02:26:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de5817fbeee91d9c37b96e84cf0f058c4685ef930bbb6cae79d468adb725ae7`  
		Last Modified: Fri, 05 Jan 2024 02:26:24 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdebffdf7e8751201d92a8e345145f76d9b011969a3db0786722bae19eae9fbc`  
		Last Modified: Fri, 05 Jan 2024 02:26:24 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8184cb8e1185f7ad7ed239472478c2be16a380a0a983070e22de0317dbd1d2`  
		Last Modified: Fri, 05 Jan 2024 02:26:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8b15baa66b3b565652d65603c861049422989c811d23af45b3005af6b28bbe01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4955736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1280c8a32b333e6e10b9b0812929b5474c231c282a2e4468fbbf19ff8751e369`

```dockerfile
```

-	Layers:
	-	`sha256:d1fa1ee102b9cc76351be1ceb53d3544f8fda225ed811cfe6831098aa9bacc82`  
		Last Modified: Fri, 05 Jan 2024 02:26:23 GMT  
		Size: 4.9 MB (4901268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97a3538f67018ac47a4c68b88b52311e98eeb9d08df0b7a55a013b2fd1ee0e30`  
		Last Modified: Fri, 05 Jan 2024 02:26:23 GMT  
		Size: 54.5 KB (54468 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:a982b32801f17845cc1e7ac7cc937478a96f763d70826683aa315bf290def2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158329652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad10a1698746fe9c0b8f9ee8c3044fe5993471f23c79704154bd77fc410a00d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:07 GMT
ADD file:6f4083d57ea9644b5a827e67b0725087a15aa428272ec223ab968bf8b4623e42 in / 
# Tue, 19 Dec 2023 01:39:07 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8d4aad22fb6a12b8cc7a78d338dfb9bc2bd6d621517b374e446f2915833ea883`  
		Last Modified: Tue, 19 Dec 2023 01:43:45 GMT  
		Size: 30.1 MB (30143863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae0b006e2ee613868802a813f5ed505067adce55d4d41db6a5681e508e1f054`  
		Last Modified: Fri, 05 Jan 2024 02:06:56 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbdf11c2ef2180425cd73f88b0e3e09d2a7a37848deba2c13ea389efc806737`  
		Last Modified: Fri, 05 Jan 2024 02:06:57 GMT  
		Size: 5.0 MB (4964211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041f8e1c96c8365dbac7b5b43ce59a6514d5782e8798dc6fd11884d5f431604c`  
		Last Modified: Fri, 05 Jan 2024 02:06:57 GMT  
		Size: 1.4 MB (1421614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a4de622b0609b23c112dd082715afab0c7efee29fcae18bd6ee0c1885eda07`  
		Last Modified: Fri, 05 Jan 2024 02:06:57 GMT  
		Size: 8.1 MB (8066117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc1464398ef17d9602861e6f7bd89c510f68e8a6a5a63cfbf18604d4d9f695c`  
		Last Modified: Fri, 05 Jan 2024 02:06:58 GMT  
		Size: 1.1 MB (1136980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b77fccc1227a15aaa73fa94b34d7c11e1ea2f6b944bfc5d52aecdeb910ffd3`  
		Last Modified: Fri, 05 Jan 2024 01:54:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69b2e520cf34fcdc0abe6ba8ecd0c683702f638392db615f75d4cddda47c95b`  
		Last Modified: Fri, 05 Jan 2024 02:06:58 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af97a41f2861ee7de0eb125f2cd1b96b53999f35302b62d1044059f62f92d74`  
		Last Modified: Fri, 05 Jan 2024 02:07:01 GMT  
		Size: 112.6 MB (112576744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b6afa807863125f335ba0aeeebb10f141f0908b8bb60a767c06d43bdc9f70f`  
		Last Modified: Fri, 05 Jan 2024 02:06:59 GMT  
		Size: 9.8 KB (9782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b77dfc8d5cd33a44182c8a847b36f1863e1352ab8d6e8b58d8b837078dce4d`  
		Last Modified: Fri, 05 Jan 2024 02:06:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2fde950e0c736aeda520f1862e17c8281c8c08c5791cc7ac465c88c90af79e`  
		Last Modified: Fri, 05 Jan 2024 02:06:59 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b6df84900dfbd44583edb7f1f0298c3c69484b433723ae2cfe57ded35a66d5`  
		Last Modified: Fri, 05 Jan 2024 02:07:00 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c89a6c6c7de3b1d1282c1dfff20622fbee4e2f536c48817321286be5456789`  
		Last Modified: Fri, 05 Jan 2024 02:07:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e64e0fcbac597dcb8817e21505b8f306075108a1f5eca974e15f04cd487fea75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4958377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234b2bd15a7f44f472694620e5e6eb2f964af77efeaa7935865c02475069eceb`

```dockerfile
```

-	Layers:
	-	`sha256:38cadd6331f790e6893fbbc4055faf8ff0809af922218c5dd00a0270c218325d`  
		Last Modified: Fri, 05 Jan 2024 02:06:57 GMT  
		Size: 4.9 MB (4903803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3cc4c4c2683b297cc9d009094cc341641663c6651203abdf3e37553f247da2`  
		Last Modified: Fri, 05 Jan 2024 02:06:56 GMT  
		Size: 54.6 KB (54574 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:ff4dfe1734c5dcc9ebe6791c1b4302d5e924730fc9329e464cd8c9d7fcfc8fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146790990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd03da5d330a09686add413c0af1f7ccdc7d5132be4236e4ce201320451663d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Dec 2023 18:58:54 GMT
ADD file:dcd5696ac281b24df52a518e2402c7f7a4caedfcba0d82e195b7c06cd3a38fdd in / 
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["bash"]
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV GOSU_VERSION=1.16
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV LANG=en_US.utf8
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_MAJOR=15
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PG_VERSION=15.5-1.pgdg120+1
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 11 Dec 2023 18:58:54 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 11 Dec 2023 18:58:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Mon, 11 Dec 2023 18:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 11 Dec 2023 18:58:54 GMT
STOPSIGNAL SIGINT
# Mon, 11 Dec 2023 18:58:54 GMT
EXPOSE map[5432/tcp:{}]
# Mon, 11 Dec 2023 18:58:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:12b1322ffb17b8e81ca1c6d9d7118e2fcee0b9d971aa3c90601e6345804a60d1`  
		Last Modified: Tue, 19 Dec 2023 02:24:36 GMT  
		Size: 29.1 MB (29121427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a0f3384903dcb4ce2d7959d41f8b1050b2b7c38783b4212515340a9e991446`  
		Last Modified: Thu, 21 Dec 2023 03:45:06 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42aab21cd31b359e3c4263f6be72986fc3079c8ae284559fffe5d9a9e966fb4`  
		Last Modified: Thu, 21 Dec 2023 03:45:07 GMT  
		Size: 4.4 MB (4355809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5baf4adddfe5644e1feebb3a650f1178a0f0943a5f19f1d7a6d208e86526bd0`  
		Last Modified: Thu, 21 Dec 2023 03:45:07 GMT  
		Size: 1.3 MB (1332590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2591385a2304f470d38ef2f8adc801fdbe9d44102301b6485a49445dab7ea0`  
		Last Modified: Thu, 21 Dec 2023 03:45:08 GMT  
		Size: 8.1 MB (8065712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a05b2acafb43db63b58b2525fb292bdde309efcc058296d9598f29ee3a0a3e2`  
		Last Modified: Thu, 21 Dec 2023 03:45:07 GMT  
		Size: 1.2 MB (1181588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e4e80bfec56ebc7335d3090d93f63d1260411c9d50e16103f8e1533db4f7f1`  
		Last Modified: Thu, 21 Dec 2023 03:45:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21d68de69db0e38114e07c03140a182b444b26e7069c53677294a10ec4b2d70`  
		Last Modified: Thu, 21 Dec 2023 03:45:08 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54733642e9cf365f5b72d710f2f1777100bf40de2e7fed544611edfc8488b00d`  
		Last Modified: Thu, 21 Dec 2023 06:04:02 GMT  
		Size: 102.7 MB (102713812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f874edd722bfc4eba13f1b5979554a818bf94a0f5970f08fca74cde7e19e283`  
		Last Modified: Thu, 21 Dec 2023 06:03:52 GMT  
		Size: 9.8 KB (9787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6738e2e316169cd9ad95301af6cd8f86fe4a1ac4bb13dc29339ff885c3476057`  
		Last Modified: Thu, 21 Dec 2023 06:03:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0165c80d13aef0d83ec2990eb8317ecd44891ea3215758b9152004d96c278155`  
		Last Modified: Thu, 21 Dec 2023 06:03:52 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc87744ec7ed8c72ff14dc5e4205d7c0e0be415547830bf66707a06b4702dc1`  
		Last Modified: Thu, 21 Dec 2023 06:03:53 GMT  
		Size: 5.3 KB (5345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e751666e6c02ac316d54fc1a22ad995b123a8dd504d3b1a4a8683f53d6c76cd`  
		Last Modified: Thu, 21 Dec 2023 06:03:53 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fe841bb7b918bda2c580480bfb93f1892e2fb882230f0af4dc9f00ec1d82aa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 KB (53764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc33186d77d484c6dffea73b559d102c93f54125be0054bc7c5442ac82f7eb1`

```dockerfile
```

-	Layers:
	-	`sha256:82c165976c337e3d1aade12001d146b916673e40d0ffada75c57bc6acf7980f9`  
		Last Modified: Thu, 21 Dec 2023 06:03:51 GMT  
		Size: 53.8 KB (53764 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:d21348955a76e06e9a8da8ac4abf54f13120dada151b0526edb24f679da10332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163234112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74d01534a2493a306dfd68fd853ddf9b533353828f06a61615ca02b42e022a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:50 GMT
ADD file:ca1db68689e0b0388337ba450ad2c8e79c159c6b78f5aa6d3ff2b89b8d7edc93 in / 
# Tue, 19 Dec 2023 01:21:51 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fc9b8f5eec3aa37ab3aace05165427479352f290d53904cea87dca6349633a09`  
		Last Modified: Tue, 19 Dec 2023 01:26:19 GMT  
		Size: 33.1 MB (33120558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9123c1be0352633684d0467d97a5ccd6ffb116db15f9856c78ed6e5aecb40b`  
		Last Modified: Wed, 20 Dec 2023 08:46:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74355209db3c6c8f846a692bf55920fe145986b193f36b3eb9c0afbeded46153`  
		Last Modified: Fri, 05 Jan 2024 02:15:16 GMT  
		Size: 5.4 MB (5368012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2b004b6e0530881e771c8657c5aed4f8e616450e0dda5c9b7623502ba5529c`  
		Last Modified: Fri, 05 Jan 2024 02:15:16 GMT  
		Size: 1.4 MB (1368392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3dca4df8512c93cb1a4bf2276de3c1d24a774b1edd73efddaeb720570c51932`  
		Last Modified: Fri, 05 Jan 2024 02:15:17 GMT  
		Size: 8.1 MB (8066277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ea5e00d1775cbacbc1fb201b81fc139a14aefc6d86be1c2939b3b3d7dfb3d0`  
		Last Modified: Fri, 05 Jan 2024 02:15:16 GMT  
		Size: 1.3 MB (1283427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9b98d0c38fb38f7d9168ce7f4210d77064a711b0073eab5c8041e758b93203`  
		Last Modified: Fri, 05 Jan 2024 02:15:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075a4aeb79571e1969cd7b0f0eb841ff79b663f23672dcef30468873fcbf84b4`  
		Last Modified: Fri, 05 Jan 2024 02:15:17 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30588b468301969f31e4afec82ad41334e379683510fe8bddf45eb5f243cba5a`  
		Last Modified: Fri, 05 Jan 2024 02:22:05 GMT  
		Size: 114.0 MB (114007329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c042a9a4eead17a704611e8e33871b08e23ac6904571997ffa1ba399e284966`  
		Last Modified: Fri, 05 Jan 2024 02:22:00 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e741c23828c14e0d5b42bacdc52937c9122ec9529f970cac20682590c39aacc4`  
		Last Modified: Fri, 05 Jan 2024 02:22:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16ec65be0d3408b7e15b1ff3e2d9a150756b2f0600c204f0d380136e107d316`  
		Last Modified: Fri, 05 Jan 2024 02:22:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2fcc6fda0ab3938472de10b480afe55caa416f23fc203ee01969dddd2f8df7`  
		Last Modified: Fri, 05 Jan 2024 02:22:02 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c6172a13bc3777cf5a7aa2f44347284e6e1e0282b397a4185a73303974c673`  
		Last Modified: Fri, 05 Jan 2024 02:22:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:226b9e7cbecbdb3d50e58b0249dc2f45193fd1e363d037b805f954276a501c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4957355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8144676cd7a03538af14f790ef0d9be32001877d357c32cc128fa9dccad617`

```dockerfile
```

-	Layers:
	-	`sha256:d8637e5af189c89c29f0887f01848088b4d24b7a9f74744fc808d73e35e75cb5`  
		Last Modified: Fri, 05 Jan 2024 02:22:01 GMT  
		Size: 4.9 MB (4902837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48fc44fc98bcadfb80adb59b29596cf22c609a23bc82104d58dc4dc8419aff84`  
		Last Modified: Fri, 05 Jan 2024 02:22:00 GMT  
		Size: 54.5 KB (54518 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:269e0edf0a9af082840a99239c5f28248e1b4a712f131831044e4dd656728260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156628024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe861880488844af22bdbc3cf662479ff677bb3d00c1abb7c03ead291aa5731`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:37 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Tue, 19 Dec 2023 01:42:39 GMT
CMD ["bash"]
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV GOSU_VERSION=1.16
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV LANG=en_US.utf8
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_MAJOR=15
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PG_VERSION=15.5-1.pgdg120+1
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el | s390x) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common pgdg-keyring; 			apt-get source --compile postgresql-common pgdg-keyring; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 04 Jan 2024 21:52:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 04 Jan 2024 21:52:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 04 Jan 2024 21:52:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2024 21:52:40 GMT
STOPSIGNAL SIGINT
# Thu, 04 Jan 2024 21:52:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 04 Jan 2024 21:52:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6967509bd16206b93c3024f4b68e0387925ab9e31847a1cbfcc4c1ff13958cce`  
		Last Modified: Tue, 19 Dec 2023 15:40:14 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58405b3b76a514401e0e244f9eb7cc104acf637ecd82511e98f2c7ec5f415299`  
		Last Modified: Fri, 05 Jan 2024 02:06:25 GMT  
		Size: 4.4 MB (4390656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45b176cc19efd4624cebae35d1fb8e8699ee4305ed0d6ebc9da1b8adb76cd5`  
		Last Modified: Fri, 05 Jan 2024 02:06:25 GMT  
		Size: 1.4 MB (1411873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c6ca7b4d00b0bf59321304795d62be5b4c732c4262355ea65f8ccbabbe8a6e`  
		Last Modified: Fri, 05 Jan 2024 02:06:25 GMT  
		Size: 8.1 MB (8120198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dac74e38c266b3a29870277cc05e303f1f33a2e26f63bf9b2f9a50f7e19d5f`  
		Last Modified: Fri, 05 Jan 2024 02:06:25 GMT  
		Size: 1.1 MB (1096493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e21b926bab4f8b7702f5ca52135032f0e8fff52f5c35b5962c1f40618c8ebe`  
		Last Modified: Fri, 05 Jan 2024 02:06:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac914f2e5170499f4bfcadf76a01273b803c4cecbc37a3ebf67af070930433b`  
		Last Modified: Fri, 05 Jan 2024 02:06:26 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0654c42b75ff63ab3d46a68d338c643f88993d49acebce2473025f61844d8a19`  
		Last Modified: Fri, 05 Jan 2024 02:09:56 GMT  
		Size: 114.1 MB (114096816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88b691236819f03c06111a237393999ab22249c5a8a0aa344e2bf05685ce65d`  
		Last Modified: Fri, 05 Jan 2024 02:09:53 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3d48f5c89db4ca726b6f662f35aac4e98111c3e438774a98f3a56fcd1b10f7`  
		Last Modified: Fri, 05 Jan 2024 02:09:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c83b607e1e82ea18ae849de6a1886128e83927d1938206821afe760a67fd32`  
		Last Modified: Fri, 05 Jan 2024 02:09:53 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5764d26b100cfb245ed1b06fae9424c7c2b522b04a09664384dd8c9341af3d8d`  
		Last Modified: Fri, 05 Jan 2024 02:09:54 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c94938580bfe6865617ac43fe79bef71ad5ae36e861f8a4669ae1965f5eaed`  
		Last Modified: Fri, 05 Jan 2024 02:09:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:cdc50271abf3b15a7e01aa3f168e82bc16253a05af83c522bdf4ebe66d1614f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4949248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86613a3ffc6d79286efb904ccc5e90f21d3fa03c5508ff326f1be8153389ba79`

```dockerfile
```

-	Layers:
	-	`sha256:ed926e5000be021308527bd93d6522c6e6c760b4666349557bd4891b75b893cd`  
		Last Modified: Fri, 05 Jan 2024 02:09:53 GMT  
		Size: 4.9 MB (4894790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:661dd56881036e572cd0f7525955c2da8c30e7e3a0fb983e4664a5c5266f9dbe`  
		Last Modified: Fri, 05 Jan 2024 02:09:53 GMT  
		Size: 54.5 KB (54458 bytes)  
		MIME: application/vnd.in-toto+json
