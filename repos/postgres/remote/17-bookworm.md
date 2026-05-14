## `postgres:17-bookworm`

```console
$ docker pull postgres@sha256:bb10a012b5a207232618899a7228ad4169ab828aaf8f47ff3a21643998682912
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

### `postgres:17-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:6238cd4cd68e0c47646ac083581841e44922f7654cf145f09e301acdd3f458f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156101639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbfb378e2d6f8f8d828a203ef61c540bd8f3ab3096382771718a8d4e5204efd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 19:01:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:01:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 19:01:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:01:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:01:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 May 2026 19:01:31 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:01:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 19:01:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:01:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 May 2026 19:01:34 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 19:01:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 May 2026 19:01:34 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 14 May 2026 19:01:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 May 2026 19:01:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:01:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:01:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:01:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:01:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:01:44 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:01:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:01:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:01:44 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:01:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:01:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436f2bc184debeb5db9e85ece4f71a6acb961b8312df98f04cfc951c9a22e429`  
		Last Modified: Thu, 14 May 2026 19:02:02 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a3334f272da04f572efe04015fe5a2215acdd4a12b5ecabd2849cb147191f4`  
		Last Modified: Thu, 14 May 2026 19:02:02 GMT  
		Size: 4.5 MB (4534175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64425a2e068a1c5c89c685f91c47e382ce51f1daa8e70029e42528efbb3bb2ab`  
		Last Modified: Thu, 14 May 2026 19:02:02 GMT  
		Size: 1.2 MB (1249516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125e262718be74903806b04945341a07527562ee8f5703fd97b928e3b948cf5f`  
		Last Modified: Thu, 14 May 2026 19:02:02 GMT  
		Size: 8.1 MB (8066516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586fbef7a97ab41cc0167fe42b9ccadeb6cdc0f1c438ef8dffe847b53e927d1c`  
		Last Modified: Thu, 14 May 2026 19:02:04 GMT  
		Size: 1.2 MB (1196374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22657e792bad610056c3854d43a1b2ee6917674c65b471787d7bfb1081228fb2`  
		Last Modified: Thu, 14 May 2026 19:02:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7443bf8a16ec4f5cb84add88d1fd3a942cef2165f8ca6d106144576abe8fdc`  
		Last Modified: Thu, 14 May 2026 19:02:04 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb6beb01bf4cbe6e3012434df5c391f049cca9d96137491a89bc76e71b44e65`  
		Last Modified: Thu, 14 May 2026 19:02:08 GMT  
		Size: 112.8 MB (112797464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59f7b1ad75d8a17c79e7bf4558d23a0b5b0d37949e90375d202b2bca087364e`  
		Last Modified: Thu, 14 May 2026 19:02:05 GMT  
		Size: 10.3 KB (10296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb13f99a5f8c94acf0ce7ac97ad0a14f4f207f450d6f3223b961f8680c974fd3`  
		Last Modified: Thu, 14 May 2026 19:02:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6e01a69a5e8392215594e13c6fcfe447e07d5f17cf293bf22230c85d8978ed`  
		Last Modified: Thu, 14 May 2026 19:02:05 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cef981236865b1480658b49a7daaeeb9e300e67090f0dded9d3f926e1500618`  
		Last Modified: Thu, 14 May 2026 19:02:06 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891c16122c8f74f397204ed60cc33c7e57084751c88325187d5133b0747ec6bd`  
		Last Modified: Thu, 14 May 2026 19:02:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:45b5feb2ead434c7957d7e3c58e32dfd66759faa5f5b5340cdcb3a20b4d3f7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bec64f6d43854de7752fcb163f00484f3efae281237e4155a1b2de8fb076360`

```dockerfile
```

-	Layers:
	-	`sha256:dfe59e5ebbfa6432806346b76120523dd3f0831b22b832554d8a5c61d013e906`  
		Last Modified: Thu, 14 May 2026 19:02:02 GMT  
		Size: 5.9 MB (5927472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1e266b9cecdc166066f6d447d0c7d9de6afa444cbddf399fa26ecff36e8fa8`  
		Last Modified: Thu, 14 May 2026 19:02:02 GMT  
		Size: 53.3 KB (53301 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:051852a77dbf95cd6ae195ab368244455e89cde1847f452196cf9af3a9555fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149135336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaafefdff0b25df22cbbcb62a4f6fe1161633ba169e21e5264b830c9057975b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 18:58:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:58:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 18:58:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:58:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:58:32 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 May 2026 18:58:32 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:58:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 18:58:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:58:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 May 2026 18:58:39 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 18:58:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 May 2026 18:58:39 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 14 May 2026 19:16:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 May 2026 19:16:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:16:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:16:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:16:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:16:40 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:16:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:16:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:16:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:16:40 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:16:40 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:16:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0496e5b1fd9475851f8b3578080061a05ea61be300ea5a278a4a08a883855adc`  
		Last Modified: Fri, 08 May 2026 18:33:05 GMT  
		Size: 25.8 MB (25765670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fa571f70804ab9b1ad67269f3ee78303895d970865dfe76865770f0d826716`  
		Last Modified: Thu, 14 May 2026 19:17:00 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5015faefdb625b45b66070f1f36df93989442e8b5af05b583fccca56d027b96`  
		Last Modified: Thu, 14 May 2026 19:17:00 GMT  
		Size: 4.2 MB (4151317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d89393edfad0a3724a7465368da0f27eabe048da4121fff79a22c6dcfc5f9fb`  
		Last Modified: Thu, 14 May 2026 19:17:00 GMT  
		Size: 1.2 MB (1220169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7aa823f91946ba7393407932ab90a041c93d2ed690b493afda9305823737c0`  
		Last Modified: Thu, 14 May 2026 19:17:00 GMT  
		Size: 8.1 MB (8066566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbdd6ed6282daece4335e0a3f2e9eaf4e9ccb5064d46e0ba2056fb534a5da35`  
		Last Modified: Thu, 14 May 2026 19:17:01 GMT  
		Size: 1.2 MB (1195065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b7bf24ca03f795f9fea914e66d7f0bd4963d5ddc9b2595b9377956c60c281e`  
		Last Modified: Thu, 14 May 2026 19:17:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bd4ebfb8698259cda6fb5c144b8943bfaec8114c095bcca74c99b82578732a`  
		Last Modified: Thu, 14 May 2026 19:17:01 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c254df88a9f186dedecce75703ae9757cf9ce34c8c8a0378d127a02d454458ff`  
		Last Modified: Thu, 14 May 2026 19:17:04 GMT  
		Size: 108.7 MB (108715237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288bfc216b7db409219ec33f4031b8c481c4344b1e40e7e56ea8ef687fd9e0b5`  
		Last Modified: Thu, 14 May 2026 19:17:02 GMT  
		Size: 10.3 KB (10299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedad2295f955b4d8cb2f6d36c7ff0b72ef081b924d1f131483d2d9a931ccde4`  
		Last Modified: Thu, 14 May 2026 19:17:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbe3d141e13100999ab4361ca076a1aab3f4e693cddc8edea1add696c08a15c`  
		Last Modified: Thu, 14 May 2026 19:17:03 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6310ab61e398cfff16e8a6a4b2fe5a468c0561056ca7ed565261903808f5f770`  
		Last Modified: Thu, 14 May 2026 19:17:04 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c40199b9971ead055aad9cd443dfbef9224059902a742e4efa002c28b8f7a16`  
		Last Modified: Thu, 14 May 2026 19:17:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:700cb5469a10be580224c816d4917e2b0720dea3f918e064204748af65dea603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf4e79094f5c2bd5195e495459cea6065c8a02fd2bab3efb50f583071909280`

```dockerfile
```

-	Layers:
	-	`sha256:1f77328b84ac8b9d7f90f4fa8af03c4bef3292afa98ffae73eb22155cff29f8c`  
		Last Modified: Thu, 14 May 2026 19:17:00 GMT  
		Size: 5.9 MB (5945789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a1ed13cb1cf7fd2b0f437c31fa89721a9fcfab544b65b10ea3533d83763d74`  
		Last Modified: Thu, 14 May 2026 19:16:59 GMT  
		Size: 53.5 KB (53508 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:0873b1a4abe6b2babce2e8b574300484d8e6538335449a7dcc3246a0c006325e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144127554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e7ea4c348a0d27aac21d3d5453ef6e6fc09fbe4b2b952a29e64b2ae78be919`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 19:01:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 19:01:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 19:01:18 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 19:01:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 19:01:24 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 May 2026 19:01:24 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 19:01:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 19:01:28 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 19:01:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 May 2026 19:01:28 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 19:01:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 May 2026 19:01:28 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 14 May 2026 19:20:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 May 2026 19:20:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:20:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:20:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:20:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:20:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:20:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:20:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:20:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:20:52 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:20:52 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:20:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1c5a0b31b39e45b38b0c73a2e506eb60bb1de512092b4765e565207648f55da2`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 23.9 MB (23941406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811f17cdc86facf979fcd1f9ee4026cccf473ad95272b0c01cae3edd0fdd6fd6`  
		Last Modified: Thu, 14 May 2026 19:21:11 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072b54653c82689fe1f5e390099f98cb482a1868345e208289176b0c83356388`  
		Last Modified: Thu, 14 May 2026 19:21:11 GMT  
		Size: 3.7 MB (3742716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1a0eb6046589e5b4129664ba70b691ccace0b2c238dffc7daaa0efc6095d91`  
		Last Modified: Thu, 14 May 2026 19:21:11 GMT  
		Size: 1.2 MB (1216036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3197aca5c60660bb94ef6482c74d3e765ac60b114ee0c023ed2770f572b96a9`  
		Last Modified: Thu, 14 May 2026 19:21:11 GMT  
		Size: 8.1 MB (8066428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d738e9f0d9271fc8a32df6281fb6218cff7aa8cfa11742a2a3fba5cae76754`  
		Last Modified: Thu, 14 May 2026 19:21:12 GMT  
		Size: 1.1 MB (1067305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afc3c273704c31a804f05404dd4bff252370e8d63298b4303a315da727cae28`  
		Last Modified: Thu, 14 May 2026 19:21:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a864df97b5e07e7b60596dc70bf3a3366eb0fd7d561fd51ea4f608f8b003e4bd`  
		Last Modified: Thu, 14 May 2026 19:21:12 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedf77f477cdbf71a36975a0ef36837aa733e43ecd5fb26a981689ac1ca00a8a`  
		Last Modified: Thu, 14 May 2026 19:21:15 GMT  
		Size: 106.1 MB (106072347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105c9187f8c31ce754f712d946f9a0cc37f52da9f544e54cfdf921171672c72a`  
		Last Modified: Thu, 14 May 2026 19:21:13 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faf595a6829b449fcfc5e667a4073dbd3a62d33f645e33a86d50ae1c56c7c0f`  
		Last Modified: Thu, 14 May 2026 19:21:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2177e1ff188e2c8263bd4ef55c47a06a908c65cc23b1af343ba9f34dad7daa8e`  
		Last Modified: Thu, 14 May 2026 19:21:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608e06b98692d5af1b00b8402d870ce7fe39ea03b224e02d325181a45dec13e3`  
		Last Modified: Thu, 14 May 2026 19:21:14 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e465f7b12a782a5c5e8b7f1e9dd8c2b87dc5c0a708bec5efad526066fc596dd`  
		Last Modified: Thu, 14 May 2026 19:21:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:e92ea82fcb62fae10d127446ea2f7298f395b92e42ce562a8180d8db6ee60023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5998551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e95f5e0fb02896038e7fd76f08c46d6d1fd9aca3ac37aa17893bffcdcab1228`

```dockerfile
```

-	Layers:
	-	`sha256:852f81b10dd010f974ed80716a4804d0d02b0497cb37788a9b6563260aec73c1`  
		Last Modified: Thu, 14 May 2026 19:21:11 GMT  
		Size: 5.9 MB (5945044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806c4fb16fa6cd08e5ddf402833b9dcc8f8f39e1e64637bb42d3e46fb6b5bd30`  
		Last Modified: Thu, 14 May 2026 19:21:11 GMT  
		Size: 53.5 KB (53507 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:6d2abccba50f9bb7cd6dcb739de7d249934460e61fdefcbd327e0960f89ecaad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154117917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b828e0ec02831dd0967072f572ec182713324a0cb96306e1c938b3dc43d006`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 18:58:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:58:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 18:58:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:58:26 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:58:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 May 2026 18:58:31 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:58:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 18:58:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:58:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 May 2026 18:58:34 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 18:58:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 May 2026 18:58:34 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 14 May 2026 18:58:49 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 May 2026 18:58:49 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 18:58:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 18:58:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 18:58:49 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 18:58:49 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 18:58:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 18:58:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 18:58:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 18:58:49 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 18:58:49 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 18:58:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8ff3a2ec45f037312351a6456fae809f163fdbe70de3df73db18de3917ad8c`  
		Last Modified: Thu, 14 May 2026 18:59:08 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eafe62502d59eb0d131bc50e6c34da9440a1b480c39717a5f03dc46667828a4`  
		Last Modified: Thu, 14 May 2026 18:59:08 GMT  
		Size: 4.5 MB (4519550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622efd23bcf75b8abddc39692ca042400fac14d2d6819a8ee9fe9a10bbe351ba`  
		Last Modified: Thu, 14 May 2026 18:59:08 GMT  
		Size: 1.2 MB (1203326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac7284ffe7e6e1516b9535aa14bf7b0696d00e48e1df772058da3c8f6fa1c73`  
		Last Modified: Thu, 14 May 2026 18:59:09 GMT  
		Size: 8.1 MB (8066455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52076c42e52b6d6017653159b6cd6b2dd2b60902605964f7e87e98098549e01`  
		Last Modified: Thu, 14 May 2026 18:59:10 GMT  
		Size: 1.1 MB (1109020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6925887a4cee1675408d05ddad7f5796b81583db0f06897b52afbda168bf34`  
		Last Modified: Thu, 14 May 2026 18:59:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71e9cae09de03cac17238fbaa0836bc2f438a1a766ee05c27456d24eec030d9`  
		Last Modified: Thu, 14 May 2026 18:59:10 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1de4780c2ed4abea23faabc8ec8aaf42e9cf6055764ab8ee60922bff055838`  
		Last Modified: Thu, 14 May 2026 18:59:13 GMT  
		Size: 111.1 MB (111082086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd0d06a676b4d303ac9689105113fba04f59ec0c6115a5fdce5b89a95bced41`  
		Last Modified: Thu, 14 May 2026 18:59:11 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10f34047ba1a0a4e569baf9da07c79aa999871c276d3ccd4bc0ba700264e81c`  
		Last Modified: Thu, 14 May 2026 18:59:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a541ffbfbe446f3adb6103e3f947cb172b04796c97fa20be4dabc133619d07`  
		Last Modified: Thu, 14 May 2026 18:59:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3a1f87bb34327b27c3fa3dbd5671fc77f6f336249970b57c732804ccc037d4`  
		Last Modified: Thu, 14 May 2026 18:59:12 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701cbc1669138312b487ffe5ee0e650d68d7da4a7204f41c3a8251d8252d774e`  
		Last Modified: Thu, 14 May 2026 18:59:12 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:8f6ee873da896d4a11fb9f37a49ea631de733c8b0abcb2053f69e69a3eb4eb2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5987329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004cba756dfe829f1a7eb79e118f09248677b4c14fd6a861724b35c61cc99b12`

```dockerfile
```

-	Layers:
	-	`sha256:d628682bc8768f226af93d49a09918936eed71bef57a649506d83f72ec48662e`  
		Last Modified: Thu, 14 May 2026 18:59:09 GMT  
		Size: 5.9 MB (5933783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3830f29c1e1bacdd16fc04f7e8cd1775c267386616d87568899a0940bbdf540a`  
		Last Modified: Thu, 14 May 2026 18:59:08 GMT  
		Size: 53.5 KB (53546 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:8dd4048d411c69fef11143d6d2b8f8b304636311ea8fbb21a8150ebac5fdb615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164986259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d8f54cd850cf83638e5986f3cc8ffc0317d0801c5dc5fe50d098bebc6c32f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 18:58:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:58:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 18:58:32 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:58:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:58:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 May 2026 18:58:37 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 18:58:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:58:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 May 2026 18:58:40 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 18:58:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 May 2026 18:58:40 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 14 May 2026 19:10:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 May 2026 19:10:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:10:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:10:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:10:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:10:35 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:10:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:10:35 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:10:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:10:35 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:10:35 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:10:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d90092c8edd324a692787fd4188906e71211941e12cf7df45f29d2b706aba9ab`  
		Last Modified: Fri, 08 May 2026 18:30:44 GMT  
		Size: 29.2 MB (29221767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58950aa3abc92090fe202ca80427fa5cf76900eddfd2f6c202cf43851cdcb736`  
		Last Modified: Thu, 14 May 2026 19:10:55 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f2e7d4ab9879f01c6a2d6fdcad6b01880e67f313c6562d9003bf5a135d8885`  
		Last Modified: Thu, 14 May 2026 19:10:56 GMT  
		Size: 5.0 MB (4966071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ebf3624f9d5b67257f5493a6fffa702c94a6c3825e63e9828f5460f2d1b3fa`  
		Last Modified: Thu, 14 May 2026 19:10:56 GMT  
		Size: 1.2 MB (1218640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9e18bde977a17b2a1426e6fe4bf5c096f89a754bd30d0bfef62bfaddb9296`  
		Last Modified: Thu, 14 May 2026 19:10:56 GMT  
		Size: 8.1 MB (8066440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc02165ed4ba5ee0827b91668fcae42f87752c5f712a459ec9010886e49a9951`  
		Last Modified: Thu, 14 May 2026 19:10:57 GMT  
		Size: 1.1 MB (1137485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6880dedd0e17457b1c9f1b0d6c17c227ef71296aa70fd8f7ac12236abaaa3a`  
		Last Modified: Thu, 14 May 2026 19:10:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13cce75b23fcef7cdd560b00e1030e514de5982f184cf5b7fbff4b024d5b7e2`  
		Last Modified: Thu, 14 May 2026 19:10:57 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cb97849921a28d629aa182db35362b6306845e5c54b27e0718ee2b76241e44`  
		Last Modified: Thu, 14 May 2026 19:11:00 GMT  
		Size: 120.4 MB (120354542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf7e74f4d67bdd2718d5bfa00cd0002373ccef98e97e45d75e981f03ed926c1`  
		Last Modified: Thu, 14 May 2026 19:10:58 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2f23c987e0c0f638f3a65c3c0869611cb27d7ab17513b7db040c6ade450b6`  
		Last Modified: Thu, 14 May 2026 19:10:58 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0120b9ec15573963594c24b52dbfdbf9023643dd8ce39d14893c91213b368b49`  
		Last Modified: Thu, 14 May 2026 19:10:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf7645317dac7eabd82afc9738b4c9be47c19c6c0d44656921c02de513634cd`  
		Last Modified: Thu, 14 May 2026 19:10:59 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9ec18f433cbb3f9f0f0f9a6afc37d242ee8c9ffdc4fce2c47f7e56aa610b15`  
		Last Modified: Thu, 14 May 2026 19:10:59 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:606eb80b083f766378152e4647964bfefb31606d5a652defe95095faea2355ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5997189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea1e05a142143a7c0c0b82abbce7490383fcd223c716e458e7551125416a243`

```dockerfile
```

-	Layers:
	-	`sha256:0a8bc59457ece4e9ca763206a1520163aec2bb25d495a04ed5a0e8f0c590d76c`  
		Last Modified: Thu, 14 May 2026 19:10:56 GMT  
		Size: 5.9 MB (5943932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c29063024f2d71cf1af8eca3563cad61a0f00ec56c489b93eca608caa57279f`  
		Last Modified: Thu, 14 May 2026 19:10:56 GMT  
		Size: 53.3 KB (53257 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:c966b6d60a4c0627c16b745940ce2a55a8cfbf99e8aeced851c94a8bbdb6a040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154931843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ade8a3f17557235a75ab78a4686f517226757acd3b3f53dd70b1b00fc5c4ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 00:06:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Sat, 09 May 2026 00:06:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:07:14 GMT
ENV GOSU_VERSION=1.19
# Sat, 09 May 2026 00:07:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 09 May 2026 00:07:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Sat, 09 May 2026 00:07:42 GMT
ENV LANG=en_US.utf8
# Sat, 09 May 2026 00:08:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:08:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 09 May 2026 00:08:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Sat, 09 May 2026 00:08:05 GMT
ENV PG_MAJOR=17
# Sat, 09 May 2026 00:08:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Sat, 09 May 2026 00:08:05 GMT
ENV PG_VERSION=17.9-1.pgdg12+1
# Sat, 09 May 2026 02:35:19 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 09 May 2026 02:35:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 09 May 2026 02:35:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 09 May 2026 02:35:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 09 May 2026 02:35:25 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sat, 09 May 2026 02:35:25 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 09 May 2026 02:35:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 02:35:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 09 May 2026 02:35:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 02:35:29 GMT
STOPSIGNAL SIGINT
# Sat, 09 May 2026 02:35:29 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 09 May 2026 02:35:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8e1a6f4f5a9e9628f902e3c8df639d1691d7f1000dc904f820155d1b9b2fa2ff`  
		Last Modified: Fri, 08 May 2026 18:20:04 GMT  
		Size: 28.5 MB (28526280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd791120c9d0fd5ae541f4efa02eac6975d5d521dc7713c7c0a5580ce265c4a`  
		Last Modified: Sat, 09 May 2026 01:22:41 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadbfdae50a5c8aa838603ee76bf9e1fc8ec6b440308f4db99142611dc5993e1`  
		Last Modified: Sat, 09 May 2026 01:22:42 GMT  
		Size: 4.5 MB (4475224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b923703b3af581ebee9e4272469b019a1b7c32026c82e2e5bceb9fe34f99e7b`  
		Last Modified: Sat, 09 May 2026 01:22:41 GMT  
		Size: 1.2 MB (1159237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b79102effcd09fd07d148fe64add7df15e3fd82ad665383ab1497a3dbb472c`  
		Last Modified: Sat, 09 May 2026 01:22:42 GMT  
		Size: 8.1 MB (8066715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1edfe569d18ce1b4a1ff0a80ffb62bdb50d73a0907b94ba210053462a9123ca`  
		Last Modified: Sat, 09 May 2026 01:22:42 GMT  
		Size: 1.2 MB (1182949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a94ef0e8381b9e5f5762910a868bf0ff569db77c3db867fb3fb03a4b4f12cda`  
		Last Modified: Sat, 09 May 2026 01:22:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3144afc30e2cc8cbb96a6cbb6e4779570c8f8913d38f069dca79e86d70e260c4`  
		Last Modified: Sat, 09 May 2026 01:22:43 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4193480c5a6dd13b6aa69888b402499bf483d83715226726161c4a049016430`  
		Last Modified: Sat, 09 May 2026 02:37:39 GMT  
		Size: 111.5 MB (111500123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f681a1097f5563fd558af546ae7bdfc0eaaab4543ca79f2010c25f67d454b794`  
		Last Modified: Sat, 09 May 2026 02:37:28 GMT  
		Size: 10.3 KB (10305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b3dfa95d49cbc8bed48f172e45b4493951299e939b36f3d2eb6f301c1efca`  
		Last Modified: Sat, 09 May 2026 02:37:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c8c6c92c3b1ba62319cf214ae6301aa4faa7b190b3dfaa5d702e29e2a1c095`  
		Last Modified: Sat, 09 May 2026 02:37:27 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6abf2e0f9c68c9a0810c2cebd1e25b8bf05bf17c4a03fb5268a35e524800ea`  
		Last Modified: Sat, 09 May 2026 02:37:29 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209286b1dfa3cf7ae106056ce13abe1ebcfeddd64d6b38d45496e92a00fd03e5`  
		Last Modified: Sat, 09 May 2026 02:37:29 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:83265c57ffe1408d3d951c60632d226cb2629dcde6f6a5478a732c1c9018b72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b903ffb9647350451cea00eeb28e19f931059a17380dfadde2716c28a9cf8b`

```dockerfile
```

-	Layers:
	-	`sha256:2b74f51a2fc8f47a3259c2691a16dd172a2a645d88ba9797cb4f83d878b63d8c`  
		Last Modified: Sat, 09 May 2026 02:37:27 GMT  
		Size: 53.2 KB (53156 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:e99e786ad842e0bea2e3af5dd87c4e2181b7d6b5811766b723edd85e15fe68fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168947133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a4014a544941a4288dd064741ce1c1a720c9a9eb0458d3b68d7c50977425d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 18:56:46 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:56:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 18:57:11 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:57:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:57:19 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 May 2026 18:57:19 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:57:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 18:57:26 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:57:28 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 May 2026 18:57:28 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 18:57:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 May 2026 18:57:28 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 14 May 2026 19:34:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 May 2026 19:34:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:34:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:34:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:34:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:34:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:34:49 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:34:49 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:34:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:34:49 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:34:49 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:34:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614fc7ae1a80404187537d601659ac6f6efc8abeacff6acf89d33971b141f54d`  
		Last Modified: Thu, 14 May 2026 18:58:55 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950f95304b8249d2e39e765b46cdc1e775c7ce3627f450c87f0c949e6940f35`  
		Last Modified: Thu, 14 May 2026 19:35:28 GMT  
		Size: 5.4 MB (5368620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166d6b4fe0299c0893e32254b41019859e96e2278d959f43966534261286b7b9`  
		Last Modified: Thu, 14 May 2026 19:35:27 GMT  
		Size: 1.2 MB (1208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f185cd98cdd449c5f6423a531cac842b44e65d12537f26ebfa829f54ed0b9c`  
		Last Modified: Thu, 14 May 2026 19:35:28 GMT  
		Size: 8.1 MB (8066525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2773d70473b84253614b4dde3895acaa356ea93e171e00000131f3876b3cd239`  
		Last Modified: Thu, 14 May 2026 19:35:27 GMT  
		Size: 1.3 MB (1283643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343e2ec5d0037fd6c7177eebcd4afb9992e687c89b6c7396bcf398d4cdfe111e`  
		Last Modified: Thu, 14 May 2026 19:35:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f7632b9a5ca5af6d6f98df020895070bf0b1bf3a97ad383bb6045b68d03dcb`  
		Last Modified: Thu, 14 May 2026 19:35:29 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abcedeebe297ada1a63fcdc81ff21cb411a3ae3405872175aa8f128ce47d546`  
		Last Modified: Thu, 14 May 2026 19:35:32 GMT  
		Size: 120.9 MB (120920375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f39f19c3dd1e54aa4004713cbec1ac2b0d9c4868336f31c11802514e462c27`  
		Last Modified: Thu, 14 May 2026 19:35:30 GMT  
		Size: 10.3 KB (10297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b963d231279368867abc86113c7f5b889e6fcee86b6b9773d4aeda9cbcd3ebf3`  
		Last Modified: Thu, 14 May 2026 19:35:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37eb5e170e6be7084bd7da76b4f9ecacfa73162b2fec9165036437fcb40fc7b0`  
		Last Modified: Thu, 14 May 2026 19:35:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ff8b5d3a648299f8ab020171bf603d36c427bd8458538508ac041ab2b2ee4d`  
		Last Modified: Thu, 14 May 2026 19:35:31 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089d917d467774e3e12be90a97708c60a1df160cee892aaae6c9b56a2f9da209`  
		Last Modified: Thu, 14 May 2026 19:35:32 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6984e500bd1251d042fc4ae785ab58d8abd0787707e0c5de2fd4221b5f3fb93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c869b3b9ba1ac12793df6dfec9b08290b00573214897d6bbf08f679e3d5b4b`

```dockerfile
```

-	Layers:
	-	`sha256:3c3abfce9fd5412f6f8e41b3810ee47fda92f41a0101a818cedb8b1547b30c0a`  
		Last Modified: Thu, 14 May 2026 19:35:28 GMT  
		Size: 5.9 MB (5934833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3cacda7aabe75cc52458f455553950dd7d04e2397a0da711dda8fee2644722`  
		Last Modified: Thu, 14 May 2026 19:35:27 GMT  
		Size: 53.4 KB (53355 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:848575f286918e7aafeb47583c224ae6841d663c363f150b5db95270cb0108b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165362253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabcb49599412e4b691c04fb32f7f064a27b66c78cccc953bdec5adfe4bd5396`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 18:56:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 May 2026 18:56:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 18:57:01 GMT
ENV GOSU_VERSION=1.19
# Thu, 14 May 2026 18:57:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 May 2026 18:57:06 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 May 2026 18:57:06 GMT
ENV LANG=en_US.utf8
# Thu, 14 May 2026 18:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 May 2026 18:57:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 May 2026 18:57:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 May 2026 18:57:11 GMT
ENV PG_MAJOR=17
# Thu, 14 May 2026 18:57:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/17/bin
# Thu, 14 May 2026 18:57:11 GMT
ENV PG_VERSION=17.10-1.pgdg12+1
# Thu, 14 May 2026 19:13:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 May 2026 19:13:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 May 2026 19:13:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 May 2026 19:13:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 May 2026 19:13:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 May 2026 19:13:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 May 2026 19:13:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 May 2026 19:13:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 May 2026 19:13:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 May 2026 19:13:17 GMT
STOPSIGNAL SIGINT
# Thu, 14 May 2026 19:13:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 May 2026 19:13:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaf94fad82206d81be865baa71364005148f1c3165d96395f66f0328b0041e7`  
		Last Modified: Thu, 14 May 2026 19:10:57 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c00d259ba20b6ab51f119533f05e57aa925852fd4fc1c29f480873e0ddd29f`  
		Last Modified: Thu, 14 May 2026 19:10:57 GMT  
		Size: 4.4 MB (4391176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2760924e83a6fe8a3664fa8546f3d4530036262eb9de70e3243df55ffb94f8ba`  
		Last Modified: Thu, 14 May 2026 19:10:57 GMT  
		Size: 1.2 MB (1222805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93b1431d35c25433419353987a4015a9fc9a7aacc21030e21d6e5b292e1b531`  
		Last Modified: Thu, 14 May 2026 19:10:58 GMT  
		Size: 8.1 MB (8120746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8c8fe17457b8afbde482aa40503ea03c75f93a0965d2edd3e34035d6dd3329`  
		Last Modified: Thu, 14 May 2026 19:10:59 GMT  
		Size: 1.1 MB (1097071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b697f88e88676483c5a221b30946f83f4453bf826727eb0b9c51fa738d38a3d1`  
		Last Modified: Thu, 14 May 2026 19:10:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417663ac4a9d1c6f036ae01c1ad33f5f2a79ca3bc94533e283eaa2d871033ee3`  
		Last Modified: Thu, 14 May 2026 19:10:59 GMT  
		Size: 3.1 KB (3146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de66194a61186bb757fda090411d7582298eca019c98ced0347ca26936c657e`  
		Last Modified: Thu, 14 May 2026 19:13:50 GMT  
		Size: 123.6 MB (123617531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057898d96a453a160448e3ab90ebdfda71038575b774b04569ce7459cd757d2b`  
		Last Modified: Thu, 14 May 2026 19:13:48 GMT  
		Size: 10.3 KB (10306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e870232b1bc77c3dbdf56b326f96fda667fffbf18b236ad354969d66669703ea`  
		Last Modified: Thu, 14 May 2026 19:13:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edef096a7d63d0a480ffa1a9854b549f45b2318a5b01740a945f3542f2c8272`  
		Last Modified: Thu, 14 May 2026 19:13:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0c20172cd1b23684a583b0b54da01e8b2165a4b1a333a96a5c0809fb2d33b7`  
		Last Modified: Thu, 14 May 2026 19:13:49 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a69e93184cc4986fe96af784dd73c450f25a3c36bbc815303f0ca18dc49f592`  
		Last Modified: Thu, 14 May 2026 19:13:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2c53f03d3fd1916d72f146a7663dcf3d2aee5c15074498d9dca5707da7456b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5993708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c279ba6834296c697c707a5ebcc14864c99ebe8e5e55119aeaa01a6f5c9d6d`

```dockerfile
```

-	Layers:
	-	`sha256:1d32c0ead68e32c9518b0beb68fbdf16f4cf968cd1420509be2ac1ea1a736b29`  
		Last Modified: Thu, 14 May 2026 19:13:48 GMT  
		Size: 5.9 MB (5940408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:071ab7d593130ea149b1d14e0223c6686cee2aa2ae911abb2574f683710d4d1f`  
		Last Modified: Thu, 14 May 2026 19:13:48 GMT  
		Size: 53.3 KB (53300 bytes)  
		MIME: application/vnd.in-toto+json
