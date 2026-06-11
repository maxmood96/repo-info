## `postgres:14-bookworm`

```console
$ docker pull postgres@sha256:0f6632181f179c2d165df5120234175a550bec1b83cbb7ad581937abf68978be
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

### `postgres:14-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:bcb5887ba9b5a78399d03e977f770fcc11227e55ed6fc6405ff61973ccddfc1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151925073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4aade667754d101d78d6438ddd6b110f3204c138d5b8a782a7d3fc93f9b8eb2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:34:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:34:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:34:43 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:34:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:34:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:34:47 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:34:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:34:51 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:34:51 GMT
ENV PG_MAJOR=14
# Thu, 11 Jun 2026 00:34:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 11 Jun 2026 00:34:51 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Thu, 11 Jun 2026 00:35:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:35:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:35:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:35:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:35:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:35:49 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:35:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:35:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:35:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:35:49 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:35:49 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:35:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07800c4658aad087eb2e7316756b145ad30f7ff6600583fccad7046558396999`  
		Last Modified: Thu, 11 Jun 2026 00:35:25 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b29a572ab139b664a7980e535532fad56ed814bd342f03408651969bd2ae4e`  
		Last Modified: Thu, 11 Jun 2026 00:35:25 GMT  
		Size: 4.5 MB (4534200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c32480c36e2d589345d1fd63d05d4234be0c9e9111dfbc4799523e4b796ed7d`  
		Last Modified: Thu, 11 Jun 2026 00:35:25 GMT  
		Size: 1.2 MB (1249480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0222f6080de5cf49e086af1c21beb75f1ff9bd8df079f8ebfd865ec87b13a9`  
		Last Modified: Thu, 11 Jun 2026 00:35:25 GMT  
		Size: 8.1 MB (8066435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26068876c10681a5f909c349367c914792abf33473b83961a074b98b5bf6f463`  
		Last Modified: Thu, 11 Jun 2026 00:35:27 GMT  
		Size: 1.2 MB (1196381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204ea99b8184ea2a477d083bff7ba63b579b5d47697823f185f77790e771c044`  
		Last Modified: Thu, 11 Jun 2026 00:35:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b7e4c43bc2c9f6c39de761b40022c6a09d44fcfd2b6d692ad2d80d61223142`  
		Last Modified: Thu, 11 Jun 2026 00:35:27 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c2b4cdc8be90495ee6d60cfaa5688545e488fe501aeb5ebdfad04ddbd8b52`  
		Last Modified: Thu, 11 Jun 2026 00:36:10 GMT  
		Size: 108.6 MB (108620423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9549c12130e641e404a5e3243626ee965d233ba050638ffe2441bdeb8b33a12`  
		Last Modified: Thu, 11 Jun 2026 00:36:07 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c3b75056250abddcd6934337ff41c0f6fffde1cd9e641ec6a4f4befd4e6ad`  
		Last Modified: Thu, 11 Jun 2026 00:36:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87928eec87833ebb31bcedcabf66ab4df5adf453d53649378a0d11da2f9b6fde`  
		Last Modified: Thu, 11 Jun 2026 00:36:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08423e428bc16d446672199cfcb7f46287a07035b08a94013e34e78db42608d`  
		Last Modified: Thu, 11 Jun 2026 00:36:09 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d66db7b944782d07e317b71b59940b3c6fae576e3dc97f7670cf1f4a54a7926`  
		Last Modified: Thu, 11 Jun 2026 00:36:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:5c3f0c16d76a692c2ad406d1e54061a527d1402c5dacd98e84f0f0308c67b666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5847608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92d375dbf049194426c9350b6ed47f080824d00b2f1a53de9e53919eb763129`

```dockerfile
```

-	Layers:
	-	`sha256:b485348447105807fd88dcc2454b32ec4f05f8f2aea0a56e759adfd7f585586f`  
		Last Modified: Thu, 11 Jun 2026 00:36:07 GMT  
		Size: 5.8 MB (5794313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a61b13bb2d8ac621ae03f3c9fd490b2faa18d32627992adddcebffc31724ee9`  
		Last Modified: Thu, 11 Jun 2026 00:36:07 GMT  
		Size: 53.3 KB (53295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:780b0f677766751a0de3b23d403a9b42749b0ce1eda05551ee06755a433fb5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144893014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc05a85690626dbfed1fb33c23a50c8282b2575525774afbf1a1c080ac6f9d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:05:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 01:05:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:05:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 01:05:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 01:05:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 01:05:52 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 01:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:05:58 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 01:05:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 01:05:58 GMT
ENV PG_MAJOR=14
# Thu, 11 Jun 2026 01:05:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 11 Jun 2026 01:05:58 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Thu, 11 Jun 2026 01:20:15 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:20:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:20:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:20:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:20:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:20:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:20:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:20:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:20:16 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:20:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:20:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99eb1512995af32b91c63bcd418e886af77e3c7ca088226161af558763425461`  
		Last Modified: Wed, 10 Jun 2026 23:38:28 GMT  
		Size: 25.8 MB (25773188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0008a5c097a3fbef4f88080ebc2974c1472a9513d70549ee63fd0287972f5275`  
		Last Modified: Thu, 11 Jun 2026 01:20:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96000bbddca51f0196cd71a2492e2f791231180d9f781102f83442e1f11b03c4`  
		Last Modified: Thu, 11 Jun 2026 01:20:34 GMT  
		Size: 4.2 MB (4151359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6de365f9087c4ed81d3a9e9e4e723aa2404d0a3b726d04e24b805e62be9a3f`  
		Last Modified: Thu, 11 Jun 2026 01:20:34 GMT  
		Size: 1.2 MB (1220119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b8b40d6a29304c5a7296cc0eba125cc9561052da5871524fe9d69d3479e506`  
		Last Modified: Thu, 11 Jun 2026 01:20:34 GMT  
		Size: 8.1 MB (8066581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6236b7fa813e12752633ca421efa3083371f190b0413ee09e89a21509799d50b`  
		Last Modified: Thu, 11 Jun 2026 01:20:35 GMT  
		Size: 1.2 MB (1195079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9115e05f8788d1e1bdaf61ae1f5bc2f929f6b01f87a8e3e92a648a340ba56580`  
		Last Modified: Thu, 11 Jun 2026 01:20:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d270e6d7ccb257c483b412f317c294a1ee766c2c2afd1f0d040fae00f63d06ce`  
		Last Modified: Thu, 11 Jun 2026 01:20:35 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e110f51519bdfbf0e96ee01842940451cb22ae9f91d026807bb4fcfaa2a354c`  
		Last Modified: Thu, 11 Jun 2026 01:20:39 GMT  
		Size: 104.5 MB (104466154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc51a521666efa4843e667d9cbbb9f62655f3e38f4f7dceb536d8f1a5857d73`  
		Last Modified: Thu, 11 Jun 2026 01:20:37 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4e81643e709aec2de127ceb78f318b7d81a772f95c90ffb662e7a680b2ead2`  
		Last Modified: Thu, 11 Jun 2026 01:20:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a04db7b6ab8fed40c4010c5785efd2c41e618d3a4e0d0cb43715a46bc20600`  
		Last Modified: Thu, 11 Jun 2026 01:20:37 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af27681ecfd2f53247b720312f529b4de79de29197ba9545c67b2749750eb7d3`  
		Last Modified: Thu, 11 Jun 2026 01:20:38 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6583359ccc9ecc5047fa125da3162ad6ddea4bb09f42bf7c2ae2ffa9fcb59e6b`  
		Last Modified: Thu, 11 Jun 2026 01:20:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:75a0f8b04aa2dda5ebb36bfbda6fe0ea209c5a15511cd1171aba41535659aec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5863641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805bbfe1f06a91984ec578cb0671a2274308a796de17b8b934ddb229478f1799`

```dockerfile
```

-	Layers:
	-	`sha256:2970481dc2651ad69f0673362616b4faf4aee9ede682d57047d13f75b9b2fa07`  
		Last Modified: Thu, 11 Jun 2026 01:20:34 GMT  
		Size: 5.8 MB (5810138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0119f03d15e45229191e34e533c70a4128a015cae31de5d8781dc68bec04dce3`  
		Last Modified: Thu, 11 Jun 2026 01:20:34 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:66d30bf5ea944f1e533b5934a9b48be0038fb3b1435f32446b2135a780dba968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139943968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8ed90c3dba73e7ffa68ab348ea5ddb9b8b05daffa4fc79fe5f4baf6a24b7b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:16:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 01:16:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:16:58 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 01:16:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 01:17:04 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 01:17:04 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 01:17:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:17:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 01:17:09 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 01:17:09 GMT
ENV PG_MAJOR=14
# Thu, 11 Jun 2026 01:17:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 11 Jun 2026 01:17:09 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Thu, 11 Jun 2026 01:31:06 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:31:06 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:31:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:31:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:31:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:31:06 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:31:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:31:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:31:06 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:31:06 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:31:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1da2fb0d744d84197159e0caec869b8bf72b88e175253449637f47bdce182f`  
		Last Modified: Thu, 11 Jun 2026 01:31:24 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3c48720f2ea1aefff3c25361f2e032b6cccbc9f1a4078ecf21fec830466a9c`  
		Last Modified: Thu, 11 Jun 2026 01:31:25 GMT  
		Size: 3.7 MB (3742715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5761cbcc0358b4804ff46123c06173ccf587f6db42fd7b15be87f906e87b653b`  
		Last Modified: Thu, 11 Jun 2026 01:31:25 GMT  
		Size: 1.2 MB (1216039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eac7e1105bff78260ff3b62b1a21c7ecd34d083d6c9606d2992c2bb5e348137`  
		Last Modified: Thu, 11 Jun 2026 01:31:25 GMT  
		Size: 8.1 MB (8066428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2214796a8e3ebd204bed5f7403e0b3bb5c2cc4d64dc7249529972566a0fd0db6`  
		Last Modified: Thu, 11 Jun 2026 01:31:26 GMT  
		Size: 1.1 MB (1067285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4af5f12de30685b86a536cd5d678102f36e3a326291d2b0ea3db5c5a903fa8`  
		Last Modified: Thu, 11 Jun 2026 01:31:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d57a58a60ba5f23d0462cf1311cbd9156483d78e7e7fc37d0394da4eb7fa8fe`  
		Last Modified: Thu, 11 Jun 2026 01:31:26 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e97ea9fde7a49326ebe31cb4985ca391b340ad65772aa496f893c6713806ea`  
		Last Modified: Thu, 11 Jun 2026 01:31:29 GMT  
		Size: 101.9 MB (101886490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0db6b2eab213a2cc44aa5aada021c55b30aafec9ef0868e0dc97a37e583aa41`  
		Last Modified: Thu, 11 Jun 2026 01:31:27 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0855d519808c08fb93f79490b67de1c7baead494bd5d954cecffc00ff1b99ce2`  
		Last Modified: Thu, 11 Jun 2026 01:31:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb6f313d302f2a841aae4779cd5d78c69d4236d5920c0fe3c5a3635774bbebf`  
		Last Modified: Thu, 11 Jun 2026 01:31:28 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48eb7da7ae3cc70dc6d024706ae57c4773bcd114b3942ed45d9a447fc9ca569`  
		Last Modified: Thu, 11 Jun 2026 01:31:29 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf847e4c61ad83f4287c6ebed1a56923ceea9d7fa89e5efeffebf5cfebea9f5`  
		Last Modified: Thu, 11 Jun 2026 01:31:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8b15dfa770ee310550565dfeba989ddb0a2f75515f1aa5e76d8afc336fffc38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5862896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ec14f1425c6b5c6ceba86ca6d886f075eabf280c4768f4c822d0b9b7c60906`

```dockerfile
```

-	Layers:
	-	`sha256:7f738965d16926fa52ffbec2a9071959e031de5e253bec4724ae4f6305c08de4`  
		Last Modified: Thu, 11 Jun 2026 01:31:25 GMT  
		Size: 5.8 MB (5809393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3c06584511259bae0072175cd206d69a26031c045b83344f4f364fa010ef160`  
		Last Modified: Thu, 11 Jun 2026 01:31:24 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:eda8c0c0bdd2d1ae364edfdcffd1551b9fc25156ac2409342f3e339bd7489c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149948311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95dd1e75cc933ecacd0120f7774ddfedc5339d100b64a8b0efaba3d06500fda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:37:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:37:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:37:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:37:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:37:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:37:32 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:37:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:37:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:37:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:37:36 GMT
ENV PG_MAJOR=14
# Thu, 11 Jun 2026 00:37:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 11 Jun 2026 00:37:36 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Thu, 11 Jun 2026 00:37:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:37:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:37:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:37:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:37:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:37:49 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:37:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:37:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:37:49 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:37:49 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:37:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573f0b03f096da98909bb8111a452ce678cd0de6b538a8a5a0a72567116e497a`  
		Last Modified: Thu, 11 Jun 2026 00:38:08 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5427e927a28979d174fece60d6aacde7d742c11acc672f366bf31bac506935de`  
		Last Modified: Thu, 11 Jun 2026 00:38:09 GMT  
		Size: 4.5 MB (4519503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c4d9ef63407117b01a661973e64beacfcf211d9c7de5359fb7729ed683735a`  
		Last Modified: Thu, 11 Jun 2026 00:38:10 GMT  
		Size: 1.2 MB (1203297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51818002f5833be7fc2a8a5f1423a998c8e1cddcf2c6af5f479376d98bb59a9`  
		Last Modified: Thu, 11 Jun 2026 00:38:09 GMT  
		Size: 8.1 MB (8066479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f541d35e73a0aee5d1d8a4afb2ca759f317c8b40dd8c856de9cb4fd4bff2464b`  
		Last Modified: Thu, 11 Jun 2026 00:38:10 GMT  
		Size: 1.1 MB (1109039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4536a43987e53205d4a563b6b0ae72320b91d0acfb191843bc87964c06840754`  
		Last Modified: Thu, 11 Jun 2026 00:38:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd52239740d67e077ae87efd7543b10c2a3716daef669f3abdf4337db29009`  
		Last Modified: Thu, 11 Jun 2026 00:38:11 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60696d96c26d58b8d1e1c373096541bdcac2890e2e70019701143f1b669d17cd`  
		Last Modified: Thu, 11 Jun 2026 00:38:15 GMT  
		Size: 106.9 MB (106907156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a9d793284f3dd0edfc22046e712585cce4fa5460d66b449d7ae5cc7c7fb447`  
		Last Modified: Thu, 11 Jun 2026 00:38:11 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4fc70369449025840878c2bda60877fc4bd1d3f9fc8ff4f0d08a1757bca682`  
		Last Modified: Thu, 11 Jun 2026 00:38:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f918723976020918aec96b55e297c25b40d7a4ffb3f9e9543f7567c7b5cadd03`  
		Last Modified: Thu, 11 Jun 2026 00:38:12 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b94ed668fa0d726f661eb8ffba60e4a69aa94eebb7c66713490c391279bc57d`  
		Last Modified: Thu, 11 Jun 2026 00:38:13 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1a77eb6452416a3000beaca70c2b611b6a9c336be71285f43f04fa1acd756d`  
		Last Modified: Thu, 11 Jun 2026 00:38:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:39e4018f302e24d397c27df9be66e451671cdd4d28126fa74bdf5665ead67f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5854165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c8505c5eac8a19ae86fec81ab38fb0bdb65eae52149397065d9da07e20ab96`

```dockerfile
```

-	Layers:
	-	`sha256:fce723077427f1cb6885ede7846978969dd90695d8960cf712f782afe808af3b`  
		Last Modified: Thu, 11 Jun 2026 00:38:09 GMT  
		Size: 5.8 MB (5800624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4322c2610426182c037989ecbe11100865176901f6e7d556c6544d4554b9124a`  
		Last Modified: Thu, 11 Jun 2026 00:38:08 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:d6e8a03d94503414e64924ff99908973479a90ba192dc444332abf880aaea3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160611619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eadc08e180625838375b61fbe25ab7cd7381de2e4dcaf68c1110e11665f9b88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:30:35 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:30:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:30:48 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:30:48 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:30:52 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:30:52 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:30:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:30:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:30:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:30:56 GMT
ENV PG_MAJOR=14
# Thu, 11 Jun 2026 00:30:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 11 Jun 2026 00:30:56 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Thu, 11 Jun 2026 00:52:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:52:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:52:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:52:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:52:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:52:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:52:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:52:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:52:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:52:16 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:52:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:52:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739733f9abf73e63e6e52ee0db87a9cff695ee3e3efa0244333a6ab292f5637b`  
		Last Modified: Thu, 11 Jun 2026 00:41:03 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24617f36ba0318d54bfc6c8531074f8a15e10fd9bcbbee415110180335901ea5`  
		Last Modified: Thu, 11 Jun 2026 00:41:03 GMT  
		Size: 5.0 MB (4966101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d2bcf0275ebd3714f16e1a6d3b6426948b26670f485df2eb28d71f4d5cd637`  
		Last Modified: Thu, 11 Jun 2026 00:41:03 GMT  
		Size: 1.2 MB (1218659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7333bf2a498769030dbf6a3bc4568d1c33a75e1d035baaab845eb03d3fb18aa`  
		Last Modified: Thu, 11 Jun 2026 00:41:03 GMT  
		Size: 8.1 MB (8066444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5f891392c7780a2081f15389602264ed5e08f2b1c3d4cfc981fa5123cc4592`  
		Last Modified: Thu, 11 Jun 2026 00:41:04 GMT  
		Size: 1.1 MB (1137473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c953a5c317593c5209f7a1d648b748ee33d1fab088ac94baff31fad7acea88f`  
		Last Modified: Thu, 11 Jun 2026 00:41:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299363f49fcaa8a01ef155c5b372a1f3e3f42e6fde8200977b259913686fa7b9`  
		Last Modified: Thu, 11 Jun 2026 00:41:05 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebc151516a4eb6dcd8269cbcad9cb66a32159cd060fa3af78e983743241a88a`  
		Last Modified: Thu, 11 Jun 2026 00:52:39 GMT  
		Size: 116.0 MB (115976651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb401bb27c59834a196d966c464263747d43ae57d2f0455b7c9b54ee75506104`  
		Last Modified: Thu, 11 Jun 2026 00:52:36 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38af2ec54f6d3cc44b521290e3da4fd4e529800a2ed6f6aac9359cbfc3a5d1a2`  
		Last Modified: Thu, 11 Jun 2026 00:52:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1a69c076199fd7c01425ba0bc9e636c7dc6fbce4f0841bb7688eb58b7a492a`  
		Last Modified: Thu, 11 Jun 2026 00:52:36 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b6d758f7d0318df22155196b6f526244e9ee0b5d57347209deb4f0dfd3b1f6`  
		Last Modified: Thu, 11 Jun 2026 00:52:37 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f1df0f8111e6594cc1c665a4995af260b484dcef4fec01d8e3c1621c17b628`  
		Last Modified: Thu, 11 Jun 2026 00:52:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0af4520dd126e847e207b229ef56896193f273a2d1474d2e0d37bbc3948d2b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5861533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e9dd7bc97bbd32ac883ae9cfdb1d2dcfe6505666c75f61dd47fd6ba34919a8`

```dockerfile
```

-	Layers:
	-	`sha256:b7f4b45bcf53c007007e52951870b3767f6f30e089c1f9dd146a835a6a5b334d`  
		Last Modified: Thu, 11 Jun 2026 00:52:36 GMT  
		Size: 5.8 MB (5808281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3737aa2aa7850f5ead0d838809d1d3d805c398b17248a8d8e3172c41b4cb8266`  
		Last Modified: Thu, 11 Jun 2026 00:52:36 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:35727db15eb27b0e8df982fd7b1cab51233b868847c922bebd069e2578e8e8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150727766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5629fd209d067f9365f95dec5e40ab399aba8b381b9e72d72ca3af6b7a27f17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 03:47:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 20 May 2026 03:48:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:48:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 03:48:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 03:49:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 20 May 2026 03:49:06 GMT
ENV LANG=en_US.utf8
# Wed, 20 May 2026 03:49:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:49:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 03:49:29 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 20 May 2026 03:49:29 GMT
ENV PG_MAJOR=14
# Wed, 20 May 2026 03:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 20 May 2026 03:49:29 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Wed, 20 May 2026 09:36:08 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 09:36:10 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 09:36:11 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 09:36:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 09:36:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 09:36:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 09:36:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 09:36:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 09:36:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 09:36:17 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 09:36:17 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 09:36:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:83efaacc11aede9fdd3dcef1c025f5df70c81553b815dfb44caceaf1fa9eba75`  
		Last Modified: Tue, 19 May 2026 22:35:42 GMT  
		Size: 28.5 MB (28522504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab0ac5538ed0c0ccb817c384f2da276651cb900c4ee7f52230d296d7319ecf`  
		Last Modified: Wed, 20 May 2026 05:02:21 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3f24330c464e9c9a34b9c04f2af74377fb284ba681aecf1eaca7b0c8d5b376`  
		Last Modified: Wed, 20 May 2026 05:02:22 GMT  
		Size: 4.5 MB (4475198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98381d3276d839839fdcebfcf33bf865cf90eaf43ccf575978aa617c4059ff4`  
		Last Modified: Wed, 20 May 2026 05:02:21 GMT  
		Size: 1.2 MB (1159226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbabcffa59b806ff40b6d0aca34bf8d4642e4fe8a0529111a0a19fcc23d24a8f`  
		Last Modified: Wed, 20 May 2026 05:02:22 GMT  
		Size: 8.1 MB (8066669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec23172ba38a0ef878da18a9628307ee3ba06cb2002c4d210fac8bf8332c862`  
		Last Modified: Wed, 20 May 2026 05:02:23 GMT  
		Size: 1.2 MB (1182959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8236c98d68c2505862cb68f376e64638cb6a31d152042da0346a097dd0953ac8`  
		Last Modified: Wed, 20 May 2026 05:02:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d6d4c1168ae55abd4742068cc060fc7424f84ae4123ad2c8ba118f837a61bd0`  
		Last Modified: Wed, 20 May 2026 05:02:23 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab2f22ef7dcf43df49048a46cb7c5b119ce11faf24c0746477dceeffd2b13ed`  
		Last Modified: Wed, 20 May 2026 09:38:23 GMT  
		Size: 107.3 MB (107300667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad53990ff318ec04de44515894936c36368bc7caed89938d871b13acea01e1a`  
		Last Modified: Wed, 20 May 2026 09:38:12 GMT  
		Size: 9.5 KB (9538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f13ee35593822298d35525831405170e7fe0050f273437e8a403d3786134bcc`  
		Last Modified: Wed, 20 May 2026 09:38:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028c8c953f949e9c37fb96e1c942a9dfa665397a5aeb1196ec332fc085365c97`  
		Last Modified: Wed, 20 May 2026 09:38:12 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ef07d3f96234e32affb40c8966843e425dc03fb9a9094b69cb736d5c115e45`  
		Last Modified: Wed, 20 May 2026 09:38:14 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b6a343184103eff5c11567926b7ca45843dc9aad4c5ea5e1429e243dc2f006`  
		Last Modified: Wed, 20 May 2026 09:38:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:17e4a4579c9b6243ba7d3ebde0c2c6fff9a9aa128704780b0b560ea4aaf8dbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d72782093a25c7ac97f0749bb761cbcf9f67ac22602f3a77211c852be3c8ae2`

```dockerfile
```

-	Layers:
	-	`sha256:21cc6232798844816709ac50f21dfc20b83041fd7636313f871509224aec8afb`  
		Last Modified: Wed, 20 May 2026 09:38:12 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:09a7e8fc1102529445200fef3753dca106fcf439125a09c9fe0291bcff89dc75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164608727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddb9ade12bf685afecff4b209c5cd5ed3cca58216823465393ca336c6a2e366`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 04:24:53 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 04:25:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:25:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 04:25:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 04:25:23 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 04:25:23 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 04:25:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:25:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 04:25:31 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 04:25:31 GMT
ENV PG_MAJOR=14
# Thu, 11 Jun 2026 04:25:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 11 Jun 2026 04:25:31 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Thu, 11 Jun 2026 04:33:29 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 04:33:30 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 04:33:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 04:33:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 04:33:30 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 04:33:30 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 04:33:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:33:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 04:33:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:33:31 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 04:33:31 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 04:33:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9879978988d3514916adbb0e2d83185ae5bd8c8d0b8c65f0be2d53ba96bfa7c8`  
		Last Modified: Thu, 11 Jun 2026 04:26:47 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ea0380ce54b8d13335a48ef988ec86e91b21fcc1e842cda5e67de076d30f45`  
		Last Modified: Thu, 11 Jun 2026 04:26:48 GMT  
		Size: 5.4 MB (5368652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2467c481adaec6c7c016d4400a90964a0c95a9e2e53cb55f6162cd82b54af0`  
		Last Modified: Thu, 11 Jun 2026 04:26:47 GMT  
		Size: 1.2 MB (1208199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b6bfa79d3857d5a20416feaf6e46abc27c0a7e730f4656e0a617059df2960b`  
		Last Modified: Thu, 11 Jun 2026 04:26:48 GMT  
		Size: 8.1 MB (8066524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ce9565433b149801f0155b1840aa9aa755fc09b6329a68b351a67d87af82f4`  
		Last Modified: Thu, 11 Jun 2026 04:26:48 GMT  
		Size: 1.3 MB (1283632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b009d3d2307709cc92dfb72deb0105d5270a35feb1fc8cf28f4fd61c4c26f4d`  
		Last Modified: Thu, 11 Jun 2026 04:26:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3b066eb70f2b5963e0a2adeb18c1dbb057037c113b667965d5800b009296d8`  
		Last Modified: Thu, 11 Jun 2026 04:26:49 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46ae92c408d719c14db1c9470161495910277e889154ee58339a42e2d68f4649`  
		Last Modified: Thu, 11 Jun 2026 04:34:16 GMT  
		Size: 116.6 MB (116579239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f270d6a89249af5cecee40722648d1e61d75b302338871bd7d222fca6330c5`  
		Last Modified: Thu, 11 Jun 2026 04:34:13 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4306b44ebdf295818b3e664a4c2711cc2a800786a74fd85d40137c1bd1e917e7`  
		Last Modified: Thu, 11 Jun 2026 04:34:13 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180aad624484e39a88ab94c54d8723aa6e19440a0cca2123782881c7838abc45`  
		Last Modified: Thu, 11 Jun 2026 04:34:13 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70c92576b79c62f3743c2c6491f0fdf1cb893263bddcc88bc305a0e62514355`  
		Last Modified: Thu, 11 Jun 2026 04:34:14 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae3ca19d4d3c8677070979b8663490a9467c72a82cfdbc7bc41f7735fc6c4f3`  
		Last Modified: Thu, 11 Jun 2026 04:34:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:994c99db82cb871824ce843f83c224af9e6139bab93c80bc06092fe0f349768d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628e805fd08272aac714fcacbce799a02d9ac313f2cf5306b33bd2cf8fde5ac7`

```dockerfile
```

-	Layers:
	-	`sha256:2d9d17e8e17aef36e1440e6a3745bb6cfc885af7d697b52e06bf18c929dc8b8c`  
		Last Modified: Thu, 11 Jun 2026 04:34:13 GMT  
		Size: 5.8 MB (5801674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d55378baf976b9348b6ceea586961e75524b6c9faf51f87c2d5b74a6de60fe`  
		Last Modified: Thu, 11 Jun 2026 04:34:12 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:022655dad64765c126a1254ab40e2625119d94c460a396ca9219503ca8076905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161059262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d51dc025f39bf4b4be10e93d36218409e641d55060542895f940a936b4e07be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:01:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 01:01:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:02:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 01:02:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 01:02:10 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 01:02:10 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 01:02:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:02:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 01:02:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 01:02:13 GMT
ENV PG_MAJOR=14
# Thu, 11 Jun 2026 01:02:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 11 Jun 2026 01:02:13 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Thu, 11 Jun 2026 01:39:50 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:39:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:39:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:39:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:39:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:39:50 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:39:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:39:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:39:50 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:39:50 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:39:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41504c1843ac4e735cc4f370f1111b09af120059e17d3b179573dd148eb58b6`  
		Last Modified: Thu, 11 Jun 2026 01:15:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4054cd17ffc15426234948fb1028e5bffa7d4a4bd42f7c86ebc0f9b7a3879548`  
		Last Modified: Thu, 11 Jun 2026 01:15:30 GMT  
		Size: 4.4 MB (4391151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a24cb20665b6f40c93753e076ff8644c19d95a9fd8f750ec5bca42c02bffcb`  
		Last Modified: Thu, 11 Jun 2026 01:15:30 GMT  
		Size: 1.2 MB (1222811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d328b42e87da196375b033db06d7dce81bde40a35768a20953018d2fc0767ff`  
		Last Modified: Thu, 11 Jun 2026 01:15:30 GMT  
		Size: 8.1 MB (8120760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80d260f0d8e13014f57274beceb487684ec18ff7befcccaccc9fe5d046e3dc5`  
		Last Modified: Thu, 11 Jun 2026 01:15:31 GMT  
		Size: 1.1 MB (1097091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d08017fe86d85b0b771ea846453fc15c587b442d05287f3a952831d37d9b42c`  
		Last Modified: Thu, 11 Jun 2026 01:15:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba0ade5fe08a27e2653e91b916e8953569b3a10761e82cdfdc16188facf06bc`  
		Last Modified: Thu, 11 Jun 2026 01:15:31 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28429cc35f4551ae2a82a39e561762aea61815680ecb5a4bcfcfc69961f2d225`  
		Last Modified: Thu, 11 Jun 2026 01:40:24 GMT  
		Size: 119.3 MB (119313408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1810fdeb339d2b294ef30879cbc2e259d80204f5b8f7ed3ca848ade4a948e7`  
		Last Modified: Thu, 11 Jun 2026 01:40:21 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8099e00796be6ef309b61356fd8a57882f2ab429d55fbb507978ab276c4af121`  
		Last Modified: Thu, 11 Jun 2026 01:40:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2fc8fd004dda72c9ec2c1b93ca6d2df51753685eb828144225619b51cb1311`  
		Last Modified: Thu, 11 Jun 2026 01:40:21 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0df800e484cfc0da78a052e61f3d4a835c4a74cda2e8b4a0c914d604c5b44a`  
		Last Modified: Thu, 11 Jun 2026 01:40:22 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facc2423240ebe8c3ee8ff741cdd48ca3ef5ee5d3d51e02bff1037d78e5f4f3e`  
		Last Modified: Thu, 11 Jun 2026 01:40:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2fc31235782e7ef583528e063fb81bf6fbbf3b5e6dc62ea5f9e4eeb64139482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ab0eec68f8579290b6834f5aa057a138eee244ac700bee514382c5b2107716`

```dockerfile
```

-	Layers:
	-	`sha256:17f92d73b4e56811e98adeaf012f6ff1c341490c7ba03ef225274a80c076c8d4`  
		Last Modified: Thu, 11 Jun 2026 01:40:22 GMT  
		Size: 5.8 MB (5804757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:466ece0211a6becab40e0c6a1264d47edfd7bba9b19177c473cdeec8ce4c9dc5`  
		Last Modified: Thu, 11 Jun 2026 01:40:21 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
