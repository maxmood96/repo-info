## `postgres:18beta3-bookworm`

```console
$ docker pull postgres@sha256:38eaad8670b69f2204635465c0ac0d97b4dde093b5ce08abc58bf5aef38dbaad
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

### `postgres:18beta3-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:6e61080e40e83d124d7cb819b5f260d2e21ef2860912fd4da179d5b985e50455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157269863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ebc589ba1fb617316724872ffbbf1b1ae05fd1e80e9c493001fe5f97f84fa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg120+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3166755df2cd1988f231f0033260fc94747f5435503225060769ea4ec3b06f07`  
		Last Modified: Thu, 14 Aug 2025 18:20:03 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099cfbd8d99d56f28606bd72cf14402516e2911401223c5aab2a05f10be7fa78`  
		Last Modified: Thu, 14 Aug 2025 18:20:04 GMT  
		Size: 4.5 MB (4533729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855dc6c2ec4918b8a6bd6c06d2a170684897ad63eaeae547f9962c4691964c0e`  
		Last Modified: Thu, 14 Aug 2025 18:20:03 GMT  
		Size: 1.4 MB (1446770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da62dae82c54e9df004db8446b12df9f944116bab210c0d06e2c6e87eae49a3f`  
		Last Modified: Thu, 14 Aug 2025 18:20:05 GMT  
		Size: 8.1 MB (8066291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff54ad786f2aaad1e27f613ddae9653a59ac222ee72c35cbc861a204f8dd89da`  
		Last Modified: Thu, 14 Aug 2025 18:20:04 GMT  
		Size: 1.2 MB (1196132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2481d2b91b4c86930d7ece337d3718030786eeb4400347e8e0fcdd2624038eb0`  
		Last Modified: Thu, 14 Aug 2025 18:20:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2c277a4e178a7778bc332656ec7d7e52353fd0ad01b9ecda9306bdb2919835`  
		Last Modified: Thu, 14 Aug 2025 18:20:04 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86d2724f8bdaa8bf323a985ada419123c34ea86f96bedc205d7cb43e1ef1a45`  
		Last Modified: Thu, 14 Aug 2025 18:20:27 GMT  
		Size: 113.8 MB (113766749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e6028c983afb2de36ca01c896c14ff1965f724b13a8554457dcd1188bb387c`  
		Last Modified: Thu, 14 Aug 2025 18:20:04 GMT  
		Size: 19.1 KB (19087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea84c88b8a046dc9b4cee140c90aa3cd18b076444178f061a1716f456b05b146`  
		Last Modified: Thu, 14 Aug 2025 18:20:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca10af4375323434f32ff5ae1477659e512fa94db2a72979081acf8cdfc27646`  
		Last Modified: Thu, 14 Aug 2025 18:20:04 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba28bcac152ef9b0c7cdf286b0a95da091394a7a2e9fb1d2b8b53c90f38dcfb`  
		Last Modified: Thu, 14 Aug 2025 18:20:04 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2bdff2205a922a5d6bd2140bb8c4571fef17b7ef60ff9335f3a75aeee5c0fe`  
		Last Modified: Thu, 14 Aug 2025 18:20:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:757d4650bbbd1b269f68543079be9ad6860f2c5d7f7dabe4c99dd9527b6a9610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6290060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9848fca82900e3309a6863ee058290daa358e49239bc95deb388917fa41b27b2`

```dockerfile
```

-	Layers:
	-	`sha256:d690dc24e24acb87a3ac1d2e409e9425dd6b656bf62dde0e531999b14c975e4a`  
		Last Modified: Thu, 14 Aug 2025 20:20:03 GMT  
		Size: 6.2 MB (6235893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e608c47d6596d80313813d929c0179e23a2a64f16b286e3c0e1b31536cfd7cde`  
		Last Modified: Thu, 14 Aug 2025 20:20:03 GMT  
		Size: 54.2 KB (54167 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:aac8f06ff7ceb584d1a1dbef18560244a57e00db41ef5fafe56ac123dde16935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87401698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d98cb390741e1b327dafa989ca2df39ff3c586144e9fdaa2f9f1e0988309ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg120+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
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
	-	`sha256:1d59d28d1accae8015b6fd90eaa5904f143d7e8b8f4eb148575105e89ab12506`  
		Last Modified: Thu, 14 Aug 2025 18:34:37 GMT  
		Size: 46.8 MB (46772605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e355ec6ec55d0de012eebf2eb08da13c6edbd333ecdef3b873a5cb968e297aa8`  
		Last Modified: Thu, 14 Aug 2025 18:34:32 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1980747f2ecff49ca9dffc6ba1d6dcd24386150151aef3b3c9bc6d37d87f066d`  
		Last Modified: Thu, 14 Aug 2025 18:34:32 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9a753a25adb88ca1987acb618c0cb1a53a1504ff127490d758e2d0acddc0fe`  
		Last Modified: Thu, 14 Aug 2025 18:34:32 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6e78273a1540f7d2f90d762d66590fba744aa9d0fb6f45f4b8e305f86b4b5`  
		Last Modified: Thu, 14 Aug 2025 18:34:32 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64f5b605c7de0ebb42f4426dc51a8db2f3b373ffb1fc348dede2fab1e2d228a`  
		Last Modified: Thu, 14 Aug 2025 18:34:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:499a2d6afa049d4b63c2f2ec3582db96839d64b4280df3a0e185737ccf109f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fb5e750283ff6d2f8113adfe55ccf177b52cbd3b8bd3251927142f223c94a6`

```dockerfile
```

-	Layers:
	-	`sha256:d8011264575755812cbf6965104134d46a10cba4253fb2b7720a1cf7183f4cfd`  
		Last Modified: Thu, 14 Aug 2025 20:20:10 GMT  
		Size: 5.4 MB (5396390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a4506d5d57b022e13f7d0cf040d5034684e901baa64c4df381613aac2da219`  
		Last Modified: Thu, 14 Aug 2025 20:20:11 GMT  
		Size: 54.4 KB (54356 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b40d8691a6dba2d97311a1cc3a63dbdeaeb5909a5b1ac7b80c57b030e5bfdcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83505702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a628d2020d421b1998f921adb5d48b7a887688571bbe23d7f4d3b8da218bfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg120+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
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
	-	`sha256:33aa3e167f6c5a81bdd41cf6a41720a4f52eb4c832f3ad2b0fd9568ff70e6537`  
		Last Modified: Thu, 14 Aug 2025 18:45:57 GMT  
		Size: 45.2 MB (45247099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d487f86b278126624b573b1454d35e2f7aec0f8d398ceeeddf268ddd4409d64`  
		Last Modified: Thu, 14 Aug 2025 18:45:49 GMT  
		Size: 19.1 KB (19094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27696439e68d6426ca86a30a14e7cca8a0081ee8e0a9feeae5dcfd7db36f73f0`  
		Last Modified: Thu, 14 Aug 2025 18:45:49 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c67cb620a92ac0d98a1bf51016e22b46f264432c65e5ce583ca33a5bc350644`  
		Last Modified: Thu, 14 Aug 2025 18:45:49 GMT  
		Size: 180.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d52708dc9d8eef31c99802dec398d1ca16754012022a71adcf38f702a759d09`  
		Last Modified: Thu, 14 Aug 2025 18:45:49 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8461c5c8a2904c0bd8006ab0a1ace17072315268808d34234ae36d477d4d924`  
		Last Modified: Thu, 14 Aug 2025 18:45:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a06896b9515830797c11c00a95b460d89d7beb85df519f35fcfc2cc5bb295b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6e56174ce08d3bdb202ec528b9db5e74c25d3beb47e88c828dc1fb29924825`

```dockerfile
```

-	Layers:
	-	`sha256:66b27fe8f77724c5fc26362fb7b4c642efabdca353255176a8e81ce756298c19`  
		Last Modified: Thu, 14 Aug 2025 20:20:16 GMT  
		Size: 5.4 MB (5395649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec521864fb078dbc27d6f9dad8449d6e9a19dbbc2f1e0e5405ed0b70bee8e52`  
		Last Modified: Thu, 14 Aug 2025 20:20:17 GMT  
		Size: 54.4 KB (54356 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:ca22fd5b75e67e6575836f6aff352d4988fec8e341b5af970f7028702498add4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155180349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb38d74e2ef3e3bd55f6f151243620105983a4f4e60735410f0ff7c07ffdcc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg120+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
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
	-	`sha256:7ad166788e8347ac32527c5f8c0e52e339ee4d675261bfd269774945a8405fd1`  
		Last Modified: Thu, 14 Aug 2025 18:51:50 GMT  
		Size: 112.0 MB (112015310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4a3df8c2ef324831daf36c65cf23b4460cab0a84dbc98683f0017732af33ea`  
		Last Modified: Thu, 14 Aug 2025 18:51:33 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bae019fac60058c4e143f1c8c5da81e25b591842287f9547bcaa0e5b3613bc1`  
		Last Modified: Thu, 14 Aug 2025 18:51:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470ed5bb41b4f860681dfa8c7598c1c6480437d169a37d81808088393a0419e0`  
		Last Modified: Thu, 14 Aug 2025 18:51:33 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8790b79debd206d9e93ad59f4b766e0f514691db2f4dc4d56d3807b557a04851`  
		Last Modified: Thu, 14 Aug 2025 18:51:33 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e02f02c6d7668b54f8d74cb2eaee76e403acb199262487938c592a79ecbbc74`  
		Last Modified: Thu, 14 Aug 2025 18:51:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1b6ca7805bc7eef2bd68c16a3c2fee9d12c16406d8d9bbc74b653b41b6a36f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6296597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d0441cc14b90fa16bb555460f24ccd3bdc3a6ebf3a62163bf5dca9fa1544d0`

```dockerfile
```

-	Layers:
	-	`sha256:ed87026c4ab8597152d51641e4a598f377014563f2f046a15711282873ac4826`  
		Last Modified: Thu, 14 Aug 2025 20:20:23 GMT  
		Size: 6.2 MB (6242198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bea9c082f0a783da544cb5242f3762dd7422481e13624f9e732e5068ef8dc44`  
		Last Modified: Thu, 14 Aug 2025 20:20:24 GMT  
		Size: 54.4 KB (54399 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:d38b315b4c89ace2f96ed1b25b3783e0fea9602d149913d608adde5206f3b0ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94167217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9edcc752b5d2f137715ddf75f4f2678cceae635a78bec373b9e07a486936d250`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg120+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df99dde7a2cefc6906c9806ab74f35528f04a08db6eac2a01df6b3ee48d719c0`  
		Last Modified: Thu, 14 Aug 2025 18:20:07 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddffd14ed3c2ce6b8a976414b546b4c142f586f8e422bfecefd49a887525e57d`  
		Last Modified: Thu, 14 Aug 2025 18:29:41 GMT  
		Size: 5.0 MB (4965092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a07eb7cfcf6535e2597cb33ea08179a697f8f4c896d552db38d4c8df416a37a`  
		Last Modified: Thu, 14 Aug 2025 18:29:41 GMT  
		Size: 1.4 MB (1422297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710103009dd991d96a58d1eb3c6bcfc7c6174871b1ec4469d71ea4d92028711d`  
		Last Modified: Thu, 14 Aug 2025 18:29:42 GMT  
		Size: 8.1 MB (8066291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd91c5114af0ffe3f920c182023b2882429e7ad84c156f9966ddede211ee0bea`  
		Last Modified: Thu, 14 Aug 2025 18:29:41 GMT  
		Size: 1.1 MB (1137167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7b4580a3a6efb2dcc107b5df7c244f2f0484dd94e09d4939466c4da51ab6f7`  
		Last Modified: Thu, 14 Aug 2025 18:29:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f00aea51ef455dbabb9172357bd2bca0a4d7133b7f035e3f402230379759623`  
		Last Modified: Thu, 14 Aug 2025 18:29:41 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf9accc8c1bf3520a639682cc3beda0401ea8ee3b061e37936e907ec9fb250f`  
		Last Modified: Thu, 14 Aug 2025 18:29:47 GMT  
		Size: 49.3 MB (49333822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62555da520761f839947e63f4d3a26ee6cd94b3c9122676b847ce0c5ed19b199`  
		Last Modified: Thu, 14 Aug 2025 18:29:41 GMT  
		Size: 19.1 KB (19092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff741da92bf41e86ce2e2ed719319c8b19d1d6aec8f85b4836cb13d16020b8a`  
		Last Modified: Thu, 14 Aug 2025 18:29:41 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d82971a0aaf7c60623df9e88b6e12e888a42e67d2487a8049f70383d87362af`  
		Last Modified: Thu, 14 Aug 2025 18:29:42 GMT  
		Size: 182.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dc7235e5628c593a08baa49893887a0ead0c756b42ae2993a3c62b03e26961`  
		Last Modified: Thu, 14 Aug 2025 18:29:42 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc2aa08be3f16191df82d2da9d07ff52c790591d04102af4af63b6a18158ded`  
		Last Modified: Thu, 14 Aug 2025 18:29:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:20da82e060697cde6ff4881ad3fb619c7ce17e1f284c2e364fbbb9f41f171fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1616bdefc94b1d1fe5f77d54fe7e82c889e00182a1b2d4a5171d45475a6f10f0`

```dockerfile
```

-	Layers:
	-	`sha256:2179a130b5a28e5263b3584f4f727b7f2237160c6084c6fb7f98eebde1c9e2c8`  
		Last Modified: Thu, 14 Aug 2025 20:20:29 GMT  
		Size: 5.4 MB (5390970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f10dcabbf627d4a44b0b2bc513d21303edd28e9d152553fed920b98117a08a9`  
		Last Modified: Thu, 14 Aug 2025 20:20:30 GMT  
		Size: 54.1 KB (54122 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:5fed33c5861f0c544e04f15347fd608fe6c61f7e9f3e5538b7755ea5ec4617c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156117207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbbf775ea756cdd362f6f64722ed6edb93b3cb5bef46447760eb5cba7e3b29c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg120+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
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
	-	`sha256:1aba3494aff85ea66f9aedf97ca9cb377287d4be82c5b550edd8e018d60aaf26`  
		Last Modified: Thu, 14 Aug 2025 19:34:27 GMT  
		Size: 112.5 MB (112512128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e74a9cc968654741911706a534266009a1e6df6b1639212842ab17ab274c85`  
		Last Modified: Thu, 14 Aug 2025 19:34:21 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effe0f5a3edfaa1695b02445820e897d86f152ee08461910b4eb791e4fc7db0d`  
		Last Modified: Thu, 14 Aug 2025 19:34:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5b455e7aa56b1fe0f76042db0757cd0a3e4e4352311b9a2bc708cc36895bdf`  
		Last Modified: Thu, 14 Aug 2025 19:34:16 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7c13c7a2747cd1d07c9e2ec6ee512a9bff9ffb490e8ccca25e720de9743c8`  
		Last Modified: Thu, 14 Aug 2025 19:34:16 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2815096d94743eccd73700182f1ca2cdf22f98e3be3a5601ea5d4f48191fd818`  
		Last Modified: Thu, 14 Aug 2025 19:34:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ea979f638ad98bd53b6cbea1d4f210f25d103df2205dcec31a76bacc91e822cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 KB (54023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfeea0e6f7ad0996b3fe219e7e80123750e457067d109774ebd676b7a6e94e96`

```dockerfile
```

-	Layers:
	-	`sha256:36e5a561ba6ec5401f8b6b32d9bd156ef082804792e3fa742267a96617644625`  
		Last Modified: Thu, 14 Aug 2025 20:20:35 GMT  
		Size: 54.0 KB (54023 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:eb36bdf65b388d9bde07a9083e137379831b47728fba5a6ea1111b8149511d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170130208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a329bed43c4bf107df2dee2ba7700c73288268f90d265fd327c8e898e4f2d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg120+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
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
	-	`sha256:a7f606a4b1ca1148ecdbb97b378bf5a324e3bd7c030e3421655db576bf785238`  
		Last Modified: Thu, 14 Aug 2025 19:00:53 GMT  
		Size: 121.9 MB (121940092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c9ddba09efa57aa9a6941492768954c2ee76a8bbdbb2aba299e0858ec49b`  
		Last Modified: Thu, 14 Aug 2025 19:00:46 GMT  
		Size: 19.1 KB (19092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ed6350c83dd5bd2f49e9e7198eed631ff5fdf4cc351f67da8b4b1eae08dcec`  
		Last Modified: Thu, 14 Aug 2025 19:00:46 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62f2eb5d0321c904ee1dc39e8dbf10c2c7400f2ccec0d3f1d0e17cd2d5eaec9`  
		Last Modified: Thu, 14 Aug 2025 19:00:47 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ed50c8971433f680e7fa92b1704cd61a92712d20ddc79c3af047896faee0ec`  
		Last Modified: Thu, 14 Aug 2025 19:00:47 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64c728dcfd60edf293f13aee27d0cbfc6225609713cfce500c0e4307a91160a`  
		Last Modified: Thu, 14 Aug 2025 19:00:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4234df7fd2c1cf96da44b77e45eb43b788545a990f6cc22117d344dd7b65d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6297501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1dbd62e6fc91747766d866bf58627646404c145b0a3fb88d2d185be1d03d5e`

```dockerfile
```

-	Layers:
	-	`sha256:abd8bd2eb235d2538c2003308538781e6b58826763c1f91cf697a7921cd22b8a`  
		Last Modified: Thu, 14 Aug 2025 20:20:39 GMT  
		Size: 6.2 MB (6243286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7ef820ab5fc5f6cc1b89f6f4362adf87f6e13e3be5b613413a41c071bd5704`  
		Last Modified: Thu, 14 Aug 2025 20:20:40 GMT  
		Size: 54.2 KB (54215 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:18beta3-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:52c3ecd64677e5a93f1bd5e96d8dd5abb4ef49cd9bfb41e71a1e090ec257aad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166579400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63157394c2a1f4a4b2d74d5391c4ff4b1942338840d1725b44916c0e52b140f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_MAJOR=18
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PG_VERSION=18~beta3-1.pgdg120+1
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -svT . /var/lib/postgresql/data # https://github.com/docker-library/postgres/pull/1259#issuecomment-2215477494 # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
VOLUME [/var/lib/postgresql]
# Thu, 14 Aug 2025 17:31:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 17:31:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 17:31:22 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 17:31:22 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 17:31:22 GMT
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
	-	`sha256:a306907f0fa7c06e6851aa0dbbbd793fc22ad5c26672046c3b1acbdf11335382`  
		Last Modified: Thu, 14 Aug 2025 19:18:47 GMT  
		Size: 124.6 MB (124640518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8e02b620f371bc10164a8d85aa6e6f2afdb03be1a265a10f7842bd837fae0`  
		Last Modified: Thu, 14 Aug 2025 19:18:33 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ec1534369cde81c74893afd6da9fd32d4188c37707e0f0968df8690dd008bf`  
		Last Modified: Thu, 14 Aug 2025 19:18:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c995370bb720004f5dceb38fcfcc3feb88f881b383eb8f6c5dfd11cfb10818ba`  
		Last Modified: Thu, 14 Aug 2025 19:18:34 GMT  
		Size: 181.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41796c9aedcb0c7d823c0988d1e8f55fa3b0d285daef10efa6c8457c41ed98e2`  
		Last Modified: Thu, 14 Aug 2025 19:18:34 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298de512fe057e932a63a984898bd38317cb8e16e213070b7853316c0223c166`  
		Last Modified: Thu, 14 Aug 2025 19:18:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:18beta3-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:fa9fed62be3f2c54d6177fe769a22f4244b14ef2162cf52e267b8438e3529f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a026667f4c9b52acbe121cde0359418cb148f34f655a28de74872e5d2fb97a04`

```dockerfile
```

-	Layers:
	-	`sha256:84815016356da8ed3a90582024a2e03cb2b4c2718c49bd4d8fe26c820d274717`  
		Last Modified: Thu, 14 Aug 2025 20:20:46 GMT  
		Size: 6.3 MB (6250547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756fea3a16939917ed2634216b272c4dbb21427ab8c5649fc77b1177042c05fa`  
		Last Modified: Thu, 14 Aug 2025 20:20:47 GMT  
		Size: 54.2 KB (54166 bytes)  
		MIME: application/vnd.in-toto+json
