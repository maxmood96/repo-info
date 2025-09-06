## `postgres:15-bookworm`

```console
$ docker pull postgres@sha256:916fdd52a7883a9bd120f7fb5025eb335ee38006faa05849acd150051ac6bb95
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
$ docker pull postgres@sha256:aba4b79cb3f162a9ebbb7c7e12de43fec5ace339b5106b80d49b626a38d42fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153190387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76765299daabf955899fa8066801b98ff9d74b74581d2be4ea7a2bf9a32ecefe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde9b6d2c51239ae34af4fc3e36ad2cdf574dcef2e94ee5ab903b9ebcf556ab6`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3516d2d2b52e544e7092afaf838807510b8ec1b6ed6966a8b002adcb5130aacf`  
		Last Modified: Fri, 05 Sep 2025 21:46:46 GMT  
		Size: 4.5 MB (4533747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64261c6d429a0e1bf0d6d16c36c01c12e788b0ba8452a28d79b28a7497540a3`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 1.4 MB (1446770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79104e4eac6f341185b5c1011e3369ee922bb082be2e55561e0974b5a47942ee`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 8.1 MB (8066289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512875c9736885f9a3ac9bd051c3fd5b003ae12e19d5f98aa2eb876e0074f466`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 1.2 MB (1196132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727bbdbc0133757343c4c7460728743ad7e3c2ead79725d6a98ed148da09ab73`  
		Last Modified: Fri, 05 Sep 2025 21:46:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dc17a4278f3bc691075c8481d4d96396e9b32e67950ac26ff1a5d186a1267f`  
		Last Modified: Fri, 05 Sep 2025 21:46:46 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9be6f7f3ddfc1319bc9904dd57cd425471124b397c542bc62487b9d9d6dd0a`  
		Last Modified: Fri, 05 Sep 2025 21:46:54 GMT  
		Size: 109.7 MB (109696576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64e5d9d03e0d846eea143d39e35e86e97c8b01ba7e3c669d81adcb77334bc2c`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 9.8 KB (9778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b6db481c32d2e62d5c4d8a3242437c349888e5fb383e1556d4f88f604d247`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a360cb1dd4d1c81f6f956f7ce7339efa450c059cdead1bf2496ba73959471346`  
		Last Modified: Fri, 05 Sep 2025 21:46:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74d011ead195c37568cb4f854a5274f0bcd1bb4e896aa49e9c86b3f9ce42fd5`  
		Last Modified: Fri, 05 Sep 2025 21:46:47 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282d66646413d8996020a10ea5dec9018cc2a48ca3b20650560ec09738b68247`  
		Last Modified: Fri, 05 Sep 2025 21:46:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:02d40671d791347b4712f8f3e8dff19e8c632354d41cb55c8f04c639c9726379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5976655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54a2a2fe9018dfe5cad9834bebe39235b3ab1251ef1f991259faad5ef65e07d8`

```dockerfile
```

-	Layers:
	-	`sha256:30ec015fed754cc4edd8fae63b75fdde37f7bdd1894f6eb2f4549dd007393c7d`  
		Last Modified: Fri, 05 Sep 2025 23:09:48 GMT  
		Size: 5.9 MB (5923316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8277c0a0a2b459f197a3f47079e4112e7fc1a30471d61f77d19b0b73c4b2f720`  
		Last Modified: Fri, 05 Sep 2025 23:09:50 GMT  
		Size: 53.3 KB (53339 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:d088ff9fcf59215828741af36ab4d0e6696352e6ddc9e66d421bab88f8af4d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146181607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9c91a6f4817e44cf27c52e727d7a17d54b10452bb02cb287fab8cbd63b9fdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e771eaf0b2bfa5de9a2c5fa7e308bc05d40fa781fde08616a2d56370ee37a0b2`  
		Last Modified: Fri, 05 Sep 2025 22:03:14 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f1e1aee78eaf3a27474bda5d48f46b0da439a6dbe530d421da20438c9b40c1`  
		Last Modified: Fri, 05 Sep 2025 22:03:15 GMT  
		Size: 4.2 MB (4150929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3414b0914af45e1212b6db4bfdd8ca04331ecec31cd6cfc11dacf00675ce8a3`  
		Last Modified: Fri, 05 Sep 2025 22:03:15 GMT  
		Size: 1.4 MB (1424030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f22f9ee4db61ce459e87e716417260b261457d77fa7625a6708b5eeca1e5118`  
		Last Modified: Fri, 05 Sep 2025 22:03:15 GMT  
		Size: 8.1 MB (8066389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11becb55631235ffea55bbe41d246f9ea164b0d3594968db51f9ea367fe818cb`  
		Last Modified: Fri, 05 Sep 2025 22:03:15 GMT  
		Size: 1.2 MB (1194876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92531631611f293dbabde69958e8458568c9ecc5bf83bcc9833ee8decdae888a`  
		Last Modified: Fri, 05 Sep 2025 22:03:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ece0a196a2178d509c64fb7f71d0b263f8688beb1c3b2c9459f99e5b8683bdd`  
		Last Modified: Fri, 05 Sep 2025 22:03:15 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df7df2a7bf875aa3fc2ef9588f17bddbe4d73ee237ccd5869495fb844fe41c`  
		Last Modified: Fri, 05 Sep 2025 22:03:28 GMT  
		Size: 105.6 MB (105562043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c8cdc3a2bfb975d983d9a27a56042fc09e4c5ec4b926602d2f0b19e30c5bb2`  
		Last Modified: Fri, 05 Sep 2025 22:03:15 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fa1f3593848bc4ff7fed2524777ca312fe20f86aad2e1606521df9557fa7cf`  
		Last Modified: Fri, 05 Sep 2025 22:03:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f25a5369de93ae8666aebaf7516df4845f75a3b56e8caa44a5a46e70c4ffa4b`  
		Last Modified: Fri, 05 Sep 2025 22:03:16 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db9e4288d602c18f4a7f2262b7569fdc4aa7ac835ee1bc7d1dd7088bf971aea`  
		Last Modified: Fri, 05 Sep 2025 22:03:17 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641b2ff333857ff7ce04071f5f5b990183fac7d01cdbd59c88519c7fc0afc08`  
		Last Modified: Fri, 05 Sep 2025 22:03:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6ab75f42d680bd971163f895dd027acc664ee862ff4445c95536d595e1499938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5990966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8863fa70a236ca0adc6b99e1829fd0081820e126a74899d00fac01aec9c41f47`

```dockerfile
```

-	Layers:
	-	`sha256:decc3bfb37a188ccc6b5da79807df1352887e6106f4498d8d96fc07c6848244f`  
		Last Modified: Fri, 05 Sep 2025 23:09:55 GMT  
		Size: 5.9 MB (5937421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f5e1302e06e7ae69a18d9f273a51820c64d4a9d7a9775a84a52facaf36d81ef`  
		Last Modified: Fri, 05 Sep 2025 23:09:55 GMT  
		Size: 53.5 KB (53545 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:f389350ffbc81cb276a78dbb24d6c056f299a8e0783d503e16b7d538e6c197e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141230146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b1fa12ff300905c4c7323fe429f11cf2c127de3930a3791fcb0575bf711640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac432ff18635a0855d2711f6e293bcce773ed8c162194133ef9cfd0d27eaad4`  
		Last Modified: Fri, 05 Sep 2025 22:22:52 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c419307c9845de1bfd56073fad36b938e7a2445217ba53096192fd1e6effce3c`  
		Last Modified: Fri, 05 Sep 2025 22:22:52 GMT  
		Size: 3.7 MB (3742535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f0f0bcf49a1b39f19d9b68389995a00c724df1d3fd9df869d6fd4ac73531e0`  
		Last Modified: Fri, 05 Sep 2025 22:22:52 GMT  
		Size: 1.4 MB (1413739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14ae35ab959efb4b51adf006cb0ab0f887efb1bba8dabcf9f132f1717e6b3e8`  
		Last Modified: Fri, 05 Sep 2025 22:22:53 GMT  
		Size: 8.1 MB (8066317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37da3c19a58e91e79766e899cd8f44e431f98a16072437dce01dd75527ee27d7`  
		Last Modified: Fri, 05 Sep 2025 22:22:52 GMT  
		Size: 1.1 MB (1067002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d256556e6ae1229a29548a0cdc6c5b020035f81baba88efd1b930ddc97ceea9`  
		Last Modified: Fri, 05 Sep 2025 22:22:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5340fc1e7e87c61697554fca008830957d3d4161f19795ed7037e9f9089d125`  
		Last Modified: Fri, 05 Sep 2025 22:22:52 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb235d1f998fa982dc1436ab626ff64c2f5e517a4c9a24ffb431587ee1d22a`  
		Last Modified: Fri, 05 Sep 2025 22:23:00 GMT  
		Size: 103.0 MB (102980993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a6696c4532a1a3aaf139e583a96985946f33856f5d39517e7a0eb82bd70d99`  
		Last Modified: Fri, 05 Sep 2025 22:22:52 GMT  
		Size: 9.8 KB (9785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660c6207e54b370d5c4d14efa44668f2b52cad56783d05b1db0d1c6a4d7a6c79`  
		Last Modified: Fri, 05 Sep 2025 22:22:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be8a45eb79af8c8d719591d56c415ee87ed1392ede7173c1aa5dcadf6b45db5`  
		Last Modified: Fri, 05 Sep 2025 22:22:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7910709172f7c139612af87f481e5a503c3e2b71b00b1e465c12e93a81177e1d`  
		Last Modified: Fri, 05 Sep 2025 22:22:53 GMT  
		Size: 5.9 KB (5932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f4968471c423c3671bdcc6297ea2ad609bc98cba54f715d27e76513d6c3e8`  
		Last Modified: Fri, 05 Sep 2025 22:22:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:12c13f2a0860c8ade5e3977035e579a54fa86a5a6095cddf8905f46af3b5febe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5990230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f81e4cecd619ea3d740a3d54e048c34bcf0992a1d77d530c71bebf77af87b26`

```dockerfile
```

-	Layers:
	-	`sha256:0e45b02f661787cc89a1e14eaee4d412a82ffcc5061b633906e6fcbcfc469235`  
		Last Modified: Fri, 05 Sep 2025 23:10:00 GMT  
		Size: 5.9 MB (5936684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f3977799aeb15cbecfa692673c94cdb7f163b98c204dfb8b979645a3211aef`  
		Last Modified: Fri, 05 Sep 2025 23:10:01 GMT  
		Size: 53.5 KB (53546 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:60b4f21948bb87ad582baddb3e39a5336c8da914ed340aec050d9f7f87d93bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151109780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4624d007b8c69f20214911e11ec5be086680abe0b2b228be4c974d2fe9dc980`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befcce40b621fbe95f73a30721620ad16271d6676bbabf57d0cbfe4c57d1891f`  
		Last Modified: Fri, 05 Sep 2025 22:03:56 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85675c2ca9ed184523c98566332f026377c55f0117e027c5a1ba435afc02291d`  
		Last Modified: Fri, 05 Sep 2025 22:03:57 GMT  
		Size: 4.5 MB (4499254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80c060c058ee212d05ba29cfb6571be7642a92de24a2eae93be3aafc2aff1a4`  
		Last Modified: Fri, 05 Sep 2025 22:03:57 GMT  
		Size: 1.4 MB (1378825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1164de88ca69203ab67dda98d627ece2406d2fe10c7b559b9dfa387c7261ac`  
		Last Modified: Fri, 05 Sep 2025 22:03:58 GMT  
		Size: 8.1 MB (8066341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733f770a9b39eca36486462244b70ce86b1775d43ac5af04ce22d7231e829de6`  
		Last Modified: Fri, 05 Sep 2025 22:03:56 GMT  
		Size: 1.1 MB (1108763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53319d5765b41067de981c4ae327dcae12baa8896ea884b95d10e3dad633c2da`  
		Last Modified: Fri, 05 Sep 2025 22:03:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52400312eb8ac3260e942134ff18ffa7a6f2fd9ad760e2b6016868f7b0cf525c`  
		Last Modified: Fri, 05 Sep 2025 22:03:56 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41262ee9112d6e9a33188ec6daf3764c0b52b0171ee7e0e2249e21c8a808ba5a`  
		Last Modified: Fri, 05 Sep 2025 22:15:22 GMT  
		Size: 108.0 MB (107953979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5c66f0679f69387edeac69bfd9214605a7884b7a978bea3d38fa925fb5669b`  
		Last Modified: Fri, 05 Sep 2025 22:15:15 GMT  
		Size: 9.8 KB (9781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd61997cf212629a83eb5d2aa2f2d5ba3fb0319c01f544d6331cd4d183d9db8a`  
		Last Modified: Fri, 05 Sep 2025 22:15:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7462d7edc0f8f2503ebf3d2592b115750c85c90e7693eb71625ab51db5f1523c`  
		Last Modified: Fri, 05 Sep 2025 22:15:15 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e8d359a252a01474c4e80205698ddc2362a656dcea7a47a979383524ee54a3`  
		Last Modified: Fri, 05 Sep 2025 22:15:15 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7987c4766907859d87b5cbf73f64e6f7fc4884835d81cc5e905b30af7582cc4c`  
		Last Modified: Fri, 05 Sep 2025 22:15:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1065851419013d8defc58ed2dd50b2adcb0d5533dc9c08afbb05b5936df5d420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5983215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ecae1fdb584b3d7a52c8d09741ec821f9d3f210685e0bb85ed8362b49b2c0e`

```dockerfile
```

-	Layers:
	-	`sha256:eb14233e8a5326c817084cbec526d2999ca28165b1eb98969b26c90de8a62d3a`  
		Last Modified: Fri, 05 Sep 2025 23:10:06 GMT  
		Size: 5.9 MB (5929631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d035e5ebc37193a6744aa1855b91ee3969e844cf711cd0a5d312b64d9379ec31`  
		Last Modified: Fri, 05 Sep 2025 23:10:07 GMT  
		Size: 53.6 KB (53584 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:a8a99eb3321568a7983e9964a3b046f83570185e8d37e9517cf948568eda5a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.0 MB (161960745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03147bb5a99042c5df7664cd000def18ae18c85ad4152f38f1988d4cfbc66911`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72d8ac87e9d873c5e07151c745e78d355837fa7a4113b62ee1fc93bf009bd9c`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9026bb7a24b70663ccc1c72e38abc33cd14c4502b3c801d418846d638e91252e`  
		Last Modified: Fri, 05 Sep 2025 21:59:01 GMT  
		Size: 5.0 MB (4965102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8c64dab8df416706ad1fd1b1f7a4be449e8a455a12b2cc3c39148130d3ea37`  
		Last Modified: Fri, 05 Sep 2025 21:59:01 GMT  
		Size: 1.4 MB (1422288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b594c18069deb930f310a83fb63ef79fad31247209e557cbe878c23a7abf115`  
		Last Modified: Fri, 05 Sep 2025 21:59:04 GMT  
		Size: 8.1 MB (8066261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d60312df0a312c5f2f9905d031cca3f47096b076615176adc3dd386b2c775e7`  
		Last Modified: Fri, 05 Sep 2025 21:59:00 GMT  
		Size: 1.1 MB (1137169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6907b3b064614b556c4297d0a58b116efdda9729d296d76c3c6c25730a9eba1`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270b526d29aa7826bd2e6e37e76e1cc5adbce73e1170b3f041ce6514cef67825`  
		Last Modified: Fri, 05 Sep 2025 21:46:46 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a83a6f5adb0a640364f72a64806a16bbf7f34d5d30cc4fc05b1c80e53abd6e`  
		Last Modified: Fri, 05 Sep 2025 21:59:11 GMT  
		Size: 117.1 MB (117136695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9d2ef77fad59788f183cd77bbbc27a8ff5f7058cbc67eea6f916c4acecc878`  
		Last Modified: Fri, 05 Sep 2025 21:59:00 GMT  
		Size: 9.8 KB (9786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658c2836d655f5a7e88d53666b8c0606f92dcbc18b4d57e862884c0b475c8bf`  
		Last Modified: Fri, 05 Sep 2025 21:59:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def1ee845cd58ec7428ce9178a4d5e228ec98a253fe3b1ce41ed97567dabd0a9`  
		Last Modified: Fri, 05 Sep 2025 21:59:00 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96266f46c74c0dd94366c3584305a0992f3b1d2aa10528f1dccae85a173a29d8`  
		Last Modified: Fri, 05 Sep 2025 21:59:00 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4161b281efb85c20cca78a37ba0f9eda54129e54237759b2a19e37074870975f`  
		Last Modified: Fri, 05 Sep 2025 21:59:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d5f2bdd477d28b3e8e3f8c7b9fc9b0d3c22c04826cbaff7f258dbc50a5c1c62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5988845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c38906fea08022b2f504487b83973f80ed8f9bc4d27eace9eac28c1af5e741`

```dockerfile
```

-	Layers:
	-	`sha256:dadaf65a235891be40fabb4cff6e39fe204eaaf3a3d98d5473608f77cb35a9fa`  
		Last Modified: Fri, 05 Sep 2025 23:10:12 GMT  
		Size: 5.9 MB (5935552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2541de0fccc4ba9d04670850c3a107e242c421980f1cc3591e0a2dc7363457c`  
		Last Modified: Fri, 05 Sep 2025 23:10:13 GMT  
		Size: 53.3 KB (53293 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:1e35580a81e18fc8025dfe4e1c7a6b12c422ba905a2d375d98311ec6f56e2172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152024879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7cbfe88398564cd5de9f15b17a903c59e513d59dcbd0c41c9ec581dc23aa55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
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
	-	`sha256:ccbb209ad78137fb56cf40c5f53795d23f01ca135a38de242720465b94e5aec0`  
		Last Modified: Thu, 14 Aug 2025 23:04:15 GMT  
		Size: 108.4 MB (108429119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eaf13fc2902a3c94c5458ba504f90d207d2696a977147fef68b196182d9ca22`  
		Last Modified: Thu, 14 Aug 2025 23:04:07 GMT  
		Size: 9.8 KB (9783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f7b4e47ac75c492d137610d601e36d48481c37f3519958088e64d0998a52ba`  
		Last Modified: Thu, 14 Aug 2025 23:04:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b556028c0437a330a604aa27701a2edea7316bebc6c6b124bc09f68fac7a6501`  
		Last Modified: Thu, 14 Aug 2025 23:04:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5965e789ecaf89c334b301b93c907d8ea6360938588f2d03c8e7d6e4e5467c15`  
		Last Modified: Thu, 14 Aug 2025 23:04:08 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c0c11d9ba62aa4c794346ebccb844dabd4685849293b3ba0797fd2ba57a9f7`  
		Last Modified: Thu, 14 Aug 2025 23:04:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:221e7a9c3d4273f6fe85d63de7c52de774fd7f9e9b327f8cc9e0d7b6aaf3fae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251630eafdc311ce7a18767a58b937feae867c004c92f39bfe26c173e28ae934`

```dockerfile
```

-	Layers:
	-	`sha256:388456053e0a5b6a0502caf78082e58f664ab1628cd21a9c6a778400bb1b9ef8`  
		Last Modified: Thu, 14 Aug 2025 23:11:17 GMT  
		Size: 53.2 KB (53206 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:a28079cf9ead77a3790deb6ee6cf379dbbc4306ed6b98304c17de6a8adac80f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165871013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ade2c2c5c30bbbc8aca3057fdbbd259810b89fc982640b278383ee45082d1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV GOSU_VERSION=1.17
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV LANG=en_US.utf8
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_MAJOR=15
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Sep 2025 21:48:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Sep 2025 21:48:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 03 Sep 2025 21:48:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Sep 2025 21:48:27 GMT
STOPSIGNAL SIGINT
# Wed, 03 Sep 2025 21:48:27 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 03 Sep 2025 21:48:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8f0a138243b625b991a13aae0989588d5d8ed19498390d04eb08c6603f00fe`  
		Last Modified: Fri, 05 Sep 2025 22:44:30 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416aab4a8205a7d21a17e854f13baf4d5b29cfb10a1c0c27149794378300678f`  
		Last Modified: Sat, 06 Sep 2025 00:00:33 GMT  
		Size: 5.4 MB (5368241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9f651748581d2517f6c288b5dd529db3839f0c45a7c62ab58f183211c40b27`  
		Last Modified: Fri, 05 Sep 2025 22:44:36 GMT  
		Size: 1.4 MB (1368769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c91846e8cb9e3d992f9ff61bc1e6f62caf973d753acf3e858878ae587e76595`  
		Last Modified: Sat, 06 Sep 2025 00:00:34 GMT  
		Size: 8.1 MB (8066446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a34128c53d8f3aa219f4b4ad96d559d8605eacc192ed31b7db853d31ec69ec`  
		Last Modified: Fri, 05 Sep 2025 22:44:41 GMT  
		Size: 1.3 MB (1283591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ab6eb21a0d2d2a67d227a28669c9cdcdae932cd343cba6a91dc0725791cd9f`  
		Last Modified: Fri, 05 Sep 2025 22:44:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219addbe85ed3cab3dfbe4ccb5e6575ac78543f97b380120b661fa6884f5cb8f`  
		Last Modified: Fri, 05 Sep 2025 22:44:48 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6709d9905e11fb6a654df79d314f40375b9f58ea62f0edbbbfee8e4838c78c`  
		Last Modified: Fri, 05 Sep 2025 22:38:08 GMT  
		Size: 117.7 MB (117689920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d69ac041835e1daa3e7f7e2b06e48bb21650e3952dacb5717a500910b021017`  
		Last Modified: Fri, 05 Sep 2025 22:38:00 GMT  
		Size: 9.8 KB (9780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51da10dff72d7c743acaa6e0426c92de61773fd3aa3d4e6ff05a9a69f162a74`  
		Last Modified: Fri, 05 Sep 2025 22:38:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e314b602c8611b0315751e3de0466c3aaf0bb55946fe2bb054abfbb9bca6be0`  
		Last Modified: Fri, 05 Sep 2025 22:38:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53013b32bfc7c4ffea04f18abc12c934b06b393931dea8e16d627ebe68feb3f5`  
		Last Modified: Fri, 05 Sep 2025 22:38:00 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51739c96af545b9dbf64cf8a36ca35556c58214e94694a098d4578e5169937fd`  
		Last Modified: Fri, 05 Sep 2025 22:38:00 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:05678d96c84678cfccf2a71e956b524ec722eb6c8d5a32b5886e5f92c731193f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5984090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c5115a73ccc9826b3feb9655fa66258461098088bd9518e55bbd4bada7509f`

```dockerfile
```

-	Layers:
	-	`sha256:97edbc8fc84c8969d48190a78d0f9081e250ed45765d880819b0c8d08baeb40a`  
		Last Modified: Fri, 05 Sep 2025 23:10:20 GMT  
		Size: 5.9 MB (5930697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8130c13aad4533c3d7ac1734ff1330da7d5c2f6da737f820a2df29646f2d025a`  
		Last Modified: Fri, 05 Sep 2025 23:10:21 GMT  
		Size: 53.4 KB (53393 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:581cf2928a11071a0d25c7224e6b22090aaa10152df543d0da2ef6577cd4b9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162400102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a73e9dbebf559fcb4887f88161d503ee9a057887db1da8022e4db96b63e54ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_MAJOR=15
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PG_VERSION=15.14-1.pgdg12+1
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:40:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:40:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:40:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:40:39 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:40:39 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:40:39 GMT
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
	-	`sha256:bd4432f861eb44ae3559f63a63fc45ec3011f163b88a7302fcda6c30373bc89d`  
		Last Modified: Thu, 14 Aug 2025 21:50:06 GMT  
		Size: 120.5 MB (120470545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6466bd1b6c56108f64ab5119b18cd7c6e49af737e2c5684bd4372161a8da20`  
		Last Modified: Thu, 14 Aug 2025 21:49:57 GMT  
		Size: 9.8 KB (9778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ee755f84163409d3140474e124abd39d550d1f1657e8bbbfa46987a8af7eaa`  
		Last Modified: Thu, 14 Aug 2025 21:49:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc6f5b43ec821a1893c5d49dc5a9ad45434f9677ef5a4f137f999350c03c269`  
		Last Modified: Thu, 14 Aug 2025 21:49:57 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb47fc0f3b8b52d40d7f676bb4922e5d931cd5da6a7c33e5e1b96f037f385b0`  
		Last Modified: Thu, 14 Aug 2025 21:49:57 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d33066d8104100e9c4c2d2880f5d5b9ca7971eb34a0f3b14759bec44880b46`  
		Last Modified: Thu, 14 Aug 2025 21:49:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1bcf1e9551d17add27b254466f4fda3a7f59fb4464a2256e588282eca1f3057d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5985372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fd1fdad1d4792a631f8bb0b351354627a2c72c7a661b8965932256c4e7584a`

```dockerfile
```

-	Layers:
	-	`sha256:df04a855ea9f88681a594ebaabb0cd61412cb93b4c6eaae02d62ff4ea4143730`  
		Last Modified: Thu, 14 Aug 2025 23:11:24 GMT  
		Size: 5.9 MB (5932032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056ac3a4cfaeec528197f1c387a888fe2b9e29b1999c2312ffd5a43f189b225b`  
		Last Modified: Thu, 14 Aug 2025 23:11:25 GMT  
		Size: 53.3 KB (53340 bytes)  
		MIME: application/vnd.in-toto+json
