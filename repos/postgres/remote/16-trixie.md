## `postgres:16-trixie`

```console
$ docker pull postgres@sha256:ab47a724d0e37131ac950b98ff2beeb3fdb3bfcc592d73c6cc4b4e7626649671
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
$ docker pull postgres@sha256:7267ecfc493a386732ce3ebc1a69660981002e2dcf693be1e35e1b436695dcc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160173799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6199d53bd7eb16a9e9eab402cc677468b0b6ed584c2fff8f17e20dafbb43f36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:34:56 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:35:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:09 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:35:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:35:14 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:35:14 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:35:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:35:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:35:18 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 00:35:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 00:35:18 GMT
ENV PG_VERSION=16.14-1.pgdg13+1
# Thu, 11 Jun 2026 00:35:30 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:35:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:35:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:35:31 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:35:31 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:35:31 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:35:31 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:35:31 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:35:31 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:35:31 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:35:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0352260f869381b7cec8d1df72463dab96cd2409a36c6cca16af5c335efa3dc2`  
		Last Modified: Thu, 11 Jun 2026 00:35:49 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b70b78d9f6adb818857c9e19b5d4f165a24a5d1030dd065dcf3e25cda659fbc`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 6.4 MB (6442989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a63031ae85f640ce4bd78f41166f05ff4492463a2ea5b95385ee53deab74f3b`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 1.3 MB (1256745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4ac08b472df65efd3eccecfd567b3f99b5775a2dcf802935809bc7973db5fc`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 8.2 MB (8203807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ce352c2a65445708b1a3cbc1fe128561326757ee8b8af0ddad147dd423686f`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 1.3 MB (1311651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdf4f8bbaaed40697fa8d3b62813de16306274157fde07ee427efbcd0003137`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a9ab0024618357fdb89a6f66028793480e19d6f3b008a577ea17450b3e5887`  
		Last Modified: Thu, 11 Jun 2026 00:35:51 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdc52f1f685268c91e796a4750e6312e3a8c2d1ceb51f14775cf69172c64e17`  
		Last Modified: Thu, 11 Jun 2026 00:35:55 GMT  
		Size: 113.2 MB (113152125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60f4e1c4498d3c6efe08f93e1c76599a91d7b14f552a2fcd3a96b86a34c418a`  
		Last Modified: Thu, 11 Jun 2026 00:35:52 GMT  
		Size: 10.1 KB (10065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278027784603259dabae2f6e66f74c7417c0340a93d85afde0f6566272e4f08c`  
		Last Modified: Thu, 11 Jun 2026 00:35:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3483ead7358228b1fddaf5f45b03d48d5e190ebd18e28db2dd7fc95fbd5a67`  
		Last Modified: Thu, 11 Jun 2026 00:35:53 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09188ae9fe233e79739474a5f30e1d8ff5bc0b72a73d8596337a48745f813d2e`  
		Last Modified: Thu, 11 Jun 2026 00:35:54 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00227982303cf358440a964289977d1f29f05f8dabd1cc0c35fda3775bb525cd`  
		Last Modified: Thu, 11 Jun 2026 00:35:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:c756d809ed430f71af8ef326ffe462a051e2ff6a2ab6b731b978d8ce156fb880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5762780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6762b3ee2d0f38be808b01003b49131d464a62b4087a7903f69b5ea48bb04b34`

```dockerfile
```

-	Layers:
	-	`sha256:3be6fc6ca9673e5be24e1974d51437b665a1b9ff4b170db8b4e20724f838f3e8`  
		Last Modified: Thu, 11 Jun 2026 00:35:50 GMT  
		Size: 5.7 MB (5708912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63daabc3a33275c4710c6b570d7a28b212c9705f936b78f4b1d19f09b8498091`  
		Last Modified: Thu, 11 Jun 2026 00:35:49 GMT  
		Size: 53.9 KB (53868 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:9a75798e6aed70a5b3401ffc2d4e957717dc79e76ff01c75647e810bfa6082be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154205805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6949bcbeafa89794526b10e22f280afc0976a9f6e1f10b5820c3cd35947eef1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:49:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:49:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:49:35 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:49:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:49:44 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:49:44 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:49:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:49:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:49:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:49:53 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 00:49:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 00:49:53 GMT
ENV PG_VERSION=16.14-1.pgdg13+1
# Thu, 11 Jun 2026 01:06:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:06:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:06:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:06:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:06:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:06:54 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:06:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:06:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:06:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:06:54 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:06:54 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:06:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d1331533039cca94d8a64feca3162825136098effe2271bad4c70ee9e53f11`  
		Last Modified: Thu, 11 Jun 2026 01:07:13 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e2500e66d00e65938fe4b2f08d308347c84aef32564b0bc50022cdeb3f13c8`  
		Last Modified: Thu, 11 Jun 2026 01:07:14 GMT  
		Size: 5.9 MB (5932371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1f2c6c0f1a80093f29c6faf06f9143c7e19407652fd4fb42e6c4c3c41df363`  
		Last Modified: Thu, 11 Jun 2026 01:07:14 GMT  
		Size: 1.2 MB (1227605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc77d0994d429f9c129cbac36dbd1d3f7292e80630ac4bc2c9cd4ba530a10fd`  
		Last Modified: Thu, 11 Jun 2026 01:07:14 GMT  
		Size: 8.2 MB (8204327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1928bab37f1b802a8166a4399d3c1359def7a00208ac1dc639578850f9ae388`  
		Last Modified: Thu, 11 Jun 2026 01:07:15 GMT  
		Size: 1.3 MB (1317325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ea2cbc603ea7bd4ac266909f34d62e05ff31058dc54cbb451775ce16a567bb`  
		Last Modified: Thu, 11 Jun 2026 01:07:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401b019ee65510a5fcdef6ce59033737a779970903e1b515dd9e2cf6eea0924a`  
		Last Modified: Thu, 11 Jun 2026 01:07:15 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4617c22fb70b0e972355a4e94dcf0c64daf0aa451e107901a2a6952ada8815`  
		Last Modified: Thu, 11 Jun 2026 01:07:18 GMT  
		Size: 109.5 MB (109543920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74edfbbed8048b0b3c090c299146e5bac9a9bd3086a292d3e819fb41c891f80`  
		Last Modified: Thu, 11 Jun 2026 01:07:17 GMT  
		Size: 10.1 KB (10058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491179019cefdbff9a1e259e40a848d8fcf6c5bc5cecd0d2e4664b36d120e538`  
		Last Modified: Thu, 11 Jun 2026 01:07:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535708c9aba76db3980f195e9a00f89fc903ad3ebff4cc6dedc267b9b97f3815`  
		Last Modified: Thu, 11 Jun 2026 01:07:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc8ad43f0e51d25572f7d68c47b043bb99ee56704c11d7d21dcda3ea9991bc7`  
		Last Modified: Thu, 11 Jun 2026 01:07:18 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263d466b600be82c4022192f9282595503301e92771e81ef704958be5db47c6d`  
		Last Modified: Thu, 11 Jun 2026 01:07:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:a30cf01698124c0de0b237004f4e5dfe9384e20d6744e368249d197b86577a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01594267525e7973d30148a6856bc84e3dbc2c64bbebc0a66e4d67eb5c3f9ecb`

```dockerfile
```

-	Layers:
	-	`sha256:988cb1b5084b4f1c021790b17c1cac4dbc04ead867f096d4496d9124e0f86b4c`  
		Last Modified: Thu, 11 Jun 2026 01:07:14 GMT  
		Size: 5.7 MB (5725554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9444e6002609f6e658ffb3726d427ed8be39dd7b1cde9e3844cb61766ec642a`  
		Last Modified: Thu, 11 Jun 2026 01:07:13 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e149e7da9edc8d7f2de2cb2bf806c304eedc2513266331495d6771cb80573a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149248156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0752eb9777e3833c75ea36508c328d1fb8adbefd8a5d7860c0448e376c52a110`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:05:06 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 01:05:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:05:22 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 01:05:22 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 01:05:29 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 01:05:29 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 01:05:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:05:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 01:05:35 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 01:05:35 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 01:05:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 01:05:35 GMT
ENV PG_VERSION=16.14-1.pgdg13+1
# Thu, 11 Jun 2026 01:20:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:20:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:20:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:20:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:20:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:20:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:20:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:20:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:20:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:20:46 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:20:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:20:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa7f5cac2b35adf59597e043b1262d3b57d0635ed753815ff85a4a01832d07c`  
		Last Modified: Thu, 11 Jun 2026 01:21:04 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3bea52c38194930df258c86f37e1853fcde0b61661e796a262803eaf42943e`  
		Last Modified: Thu, 11 Jun 2026 01:21:05 GMT  
		Size: 5.5 MB (5497355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c77c34fc9454e43e49d133b6d402a3248024844be197f3a60341e831107a14`  
		Last Modified: Thu, 11 Jun 2026 01:21:04 GMT  
		Size: 1.2 MB (1222437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877c47f3eaaf32ce15df7feeeb7af4c72145daf2203f46385dccf6f38bfc663d`  
		Last Modified: Thu, 11 Jun 2026 01:21:05 GMT  
		Size: 8.2 MB (8204107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfd466278adb749f1432cc75190581b3bcdeb9f21ad774b0bd9ca4a7e5fc08b`  
		Last Modified: Thu, 11 Jun 2026 01:21:06 GMT  
		Size: 1.2 MB (1172623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee4c6beede1150e4390a3c045599b47cfb49eca4e29bbc6ce23123d3623a6c1`  
		Last Modified: Thu, 11 Jun 2026 01:21:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a459ba4ba332b52aaf0c71e4d0adcaeab4651b0510bbfc23d3c0faeed35bab`  
		Last Modified: Thu, 11 Jun 2026 01:21:06 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9f9cf5eaad59ad90c6d774f4bc1f0a8da74862f62af11861de100fbda79f31`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 106.9 MB (106919551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5308445ccd857aad23607cf98613f2d77cbe3c21d23020fed9f6797d771538`  
		Last Modified: Thu, 11 Jun 2026 01:21:07 GMT  
		Size: 10.1 KB (10074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c7a9f1af295b24331abb0461bd4036b45650c5a807673e87d6ae19e8a35f9b`  
		Last Modified: Thu, 11 Jun 2026 01:21:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcb77c1b9add54aba5b9d2c9b898abba4a81c0c10be77912901dd61d689356f`  
		Last Modified: Thu, 11 Jun 2026 01:21:08 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267fa32b954c13fb4a98d3d3aecd39849dc24c4952167fb8abd880367c6a5c00`  
		Last Modified: Thu, 11 Jun 2026 01:21:08 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24484bdbaab4ddd407bdc35b3bd2cd64a791d57d8563ad41da429f776bad7999`  
		Last Modified: Thu, 11 Jun 2026 01:21:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ec7ed19497f6e8d74ba0fe757b2be9fb35e059607897ddef6c9e9659b633bef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c4edba455388795035a0473fa6b2f30512385b6d14ba36b0e306985c72d906`

```dockerfile
```

-	Layers:
	-	`sha256:7e09ae48da82aa0ad50d6c42b454424e4f7970f5813c078544a4345f6d729a5c`  
		Last Modified: Thu, 11 Jun 2026 01:21:05 GMT  
		Size: 5.7 MB (5724859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c20563c8ba0efb6c3b588dd7bd62d4f1c97764bb6ea688e5202327346f7ffa5a`  
		Last Modified: Thu, 11 Jun 2026 01:21:04 GMT  
		Size: 54.1 KB (54092 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:bd2740e836cc644b8753c7a195483a3c26c121974be13be0c343f76635d2f2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158797185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f961d097a9cedd37779baef1aab3fe87ef1c63b3b34d361f90a98ea5c9b77e56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:35:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:35:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:30 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:35:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:35:35 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:35:35 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:39 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:35:40 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:35:40 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 00:35:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 00:35:40 GMT
ENV PG_VERSION=16.14-1.pgdg13+1
# Thu, 11 Jun 2026 00:36:50 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:36:50 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:36:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:36:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:36:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:36:50 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:36:50 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:36:50 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:36:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:36:50 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:36:50 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:36:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf107e9ced296b2cf7b764ac39772fc84832350a08f96a457d5e3279a3168f2`  
		Last Modified: Thu, 11 Jun 2026 00:36:22 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c3acb06f50e2aef98ba17051a0816784c1428699e417402716f1dbafdad4b2`  
		Last Modified: Thu, 11 Jun 2026 00:36:23 GMT  
		Size: 6.2 MB (6235173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9cfaff3447e48d82e5b8092a32f6650af7467102a07bc785bf46b0d89e2a2e`  
		Last Modified: Thu, 11 Jun 2026 00:36:22 GMT  
		Size: 1.2 MB (1209596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a70aabb22c1c15cca9b6b98e4fe1f97a2a3b68d450c724f9203d75a4a647a64`  
		Last Modified: Thu, 11 Jun 2026 00:36:23 GMT  
		Size: 8.2 MB (8204061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1839ffb73fec6c7b63a6c127cc17b193a9db85fe80c3c26fb260b695163de9c`  
		Last Modified: Thu, 11 Jun 2026 00:36:23 GMT  
		Size: 1.2 MB (1220601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea1edd0577deb996d310427e3acfae2aac86fbedd6890d542e6ce1ad2c4e13c`  
		Last Modified: Thu, 11 Jun 2026 00:36:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ee1976a32ff9342938829c9cb94c48c8e7566914b95bee4bff6aeeab9ce64b`  
		Last Modified: Thu, 11 Jun 2026 00:36:24 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe1d7dcdafa24774fdbf3c821c9cc57d9616d151400694fe1fc73aed2d922ec`  
		Last Modified: Thu, 11 Jun 2026 00:37:12 GMT  
		Size: 111.8 MB (111758159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3227aeabe2d658e74ce610c69e0b1c1bedf588baab858fbcee594e534de4eef`  
		Last Modified: Thu, 11 Jun 2026 00:37:09 GMT  
		Size: 10.1 KB (10062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e702653a3571e57283b6d8668e815b8f1be7d5dc50d7212cc1d03c9d5bb65d`  
		Last Modified: Thu, 11 Jun 2026 00:37:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ca93767432ef9ab2d55a13d5f3d08e249450fd76f819766936fe4b2d6fed8`  
		Last Modified: Thu, 11 Jun 2026 00:37:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b02b39f094c59e4de1395167abd9815ff29484b8bbdf8bd0a453e2d48bccba`  
		Last Modified: Thu, 11 Jun 2026 00:37:10 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce9e660c9e627fa5b8ad585e968b82ed0c6f1576f55846d22fc964e3b5bda89`  
		Last Modified: Thu, 11 Jun 2026 00:37:10 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:df2604412dc2032eed56bf75900e594b1918681a17a78a69bdc696c37ad2ce03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a315540571c1931f62922663afa320f94c400ea1b3b5bbaf7da5caca14e6b527`

```dockerfile
```

-	Layers:
	-	`sha256:5fffec89869a185f34c40992f70cdcbb939ebb638917f1b06f388a8f6bfbf633`  
		Last Modified: Thu, 11 Jun 2026 00:37:09 GMT  
		Size: 5.7 MB (5715250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5034399c254a7c2563423ddcf2066ced6e0ec88f82cc1874ba57e3c6e251232`  
		Last Modified: Thu, 11 Jun 2026 00:37:09 GMT  
		Size: 54.1 KB (54138 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; 386

```console
$ docker pull postgres@sha256:b88f1736205f1bdbb670d4b356770e6afa1ec88be6d7c52df4956b60faac2fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169309689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b33c3e977e8660cd124e7cfb7eb58bb00b81c21d4859ad8ea5744e9c6ddb56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:32:21 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:32:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:32:36 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:32:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:32:41 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:32:41 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:32:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:32:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:32:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:32:45 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 00:32:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 00:32:45 GMT
ENV PG_VERSION=16.14-1.pgdg13+1
# Thu, 11 Jun 2026 00:43:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:43:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:43:28 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:43:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:43:28 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:43:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:43:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d48350a446704b0d95b690d647c5bcadd2347d974a6f2684606469009d47d2`  
		Last Modified: Thu, 11 Jun 2026 00:43:47 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98ff9fc62f21a37ae09e34620c47a521555bfb3a15b287d18945c02a5f2a818`  
		Last Modified: Thu, 11 Jun 2026 00:43:48 GMT  
		Size: 6.6 MB (6631354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6b5773ad070e9b434f9a414579dbe6645eae68d2e72103dba5aaf3a2c7b27a`  
		Last Modified: Thu, 11 Jun 2026 00:43:47 GMT  
		Size: 1.2 MB (1225848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cc339ab2065d5b839efe95ce1ad83e18c83250fc0f6db05796537507b80912`  
		Last Modified: Thu, 11 Jun 2026 00:43:48 GMT  
		Size: 8.2 MB (8204086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7ba48aae047386231bd3249d42cdd385e89f9d7ff380da3f046b808b6b4290`  
		Last Modified: Thu, 11 Jun 2026 00:43:48 GMT  
		Size: 1.3 MB (1308281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269473341af96e7b2cc54cab072c6239188f8f39a26dd1d26a7f3a99b591612d`  
		Last Modified: Thu, 11 Jun 2026 00:43:49 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f51216ed590a16e2fdacf46471c49c3e309fac615d99b7e02f703b88279b15`  
		Last Modified: Thu, 11 Jun 2026 00:43:49 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b650a45d1f6bf73c8b2e23d1b1d6e95c3fe7f96bc80a39d05fc7cf41d6eec78c`  
		Last Modified: Thu, 11 Jun 2026 00:43:53 GMT  
		Size: 120.6 MB (120617865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6476d08d5f5eeefac999d1ddbf4b48da8e4e167a922246e602d3f4f7278a2fdd`  
		Last Modified: Thu, 11 Jun 2026 00:43:50 GMT  
		Size: 10.1 KB (10065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32779d490d2a71960fc16a9b3ec49ac202363c7bafe6eb8c87f3838a23b568fb`  
		Last Modified: Thu, 11 Jun 2026 00:43:50 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693535089909d5b0c0b648bd8aa19daba944ed2a6bca3120da0d0092622398d8`  
		Last Modified: Thu, 11 Jun 2026 00:43:50 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41385d0ac4bf6ac00dc8b8549fea20ead3a9c94e710dccb43c11a405c220b5a8`  
		Last Modified: Thu, 11 Jun 2026 00:43:52 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc271dbc779fc62e641226b18e7da63d4f66eca84ec17a4b83173b9186be7a51`  
		Last Modified: Thu, 11 Jun 2026 00:43:51 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:346b741106c0dc44ccfdd0fd405236a555e52b867464af9b975ef5694b1e12d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6fa2de8a064add2fb8186be38d8e2a50b969932a16d041278f2a5618636ad7`

```dockerfile
```

-	Layers:
	-	`sha256:b51565a9cf5ea0fca95a82420f10b765b906e51213874ed7a9e4deb5f99cee23`  
		Last Modified: Thu, 11 Jun 2026 00:43:47 GMT  
		Size: 5.7 MB (5724447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f37fcf3e50bfa0c70b1e568d89333b63fb412d2da20d951ac4a0a7fb036050a8`  
		Last Modified: Thu, 11 Jun 2026 00:43:47 GMT  
		Size: 53.8 KB (53814 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:d77266a67524cad3df8e54ef41eb1db69805f73d0090e1f17372377503a8a8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.4 MB (172440665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3754cfe698053da3f1e227a827faf12f0557b9421526dc7c68c2bab7d65b3118`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:22:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 04:22:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:22:45 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 04:22:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 04:22:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 04:22:57 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 04:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:23:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 04:23:06 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 04:23:06 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 04:23:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 04:23:06 GMT
ENV PG_VERSION=16.14-1.pgdg13+1
# Thu, 11 Jun 2026 04:29:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 04:29:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 04:29:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 04:29:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 04:29:27 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 04:29:27 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 04:29:27 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:29:28 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 04:29:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:29:28 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 04:29:28 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 04:29:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e93abe7480356a6fc8ce6943b71e051b601733a1b3eec3b84b51ba066f7ebb`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e50b953d51df1ad75aa8423fe4c0b925ff04cb0f00fc9bf7d832470c0113811`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 7.1 MB (7076806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b50b5ff568aaa483897ee3a1d850dd075b9e6655d095d44de11470d6f8fc009`  
		Last Modified: Thu, 11 Jun 2026 04:24:34 GMT  
		Size: 1.2 MB (1214789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd8cddd4d91d1f798bf8f04a08fd19f0142e2c39271c68c2550b9e9fd0cc832`  
		Last Modified: Thu, 11 Jun 2026 04:24:35 GMT  
		Size: 8.2 MB (8204074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bda34c5d2b40061a1e23c1b4ffa3a2ae3eaf4b9cb20d75b9698f949074d325`  
		Last Modified: Thu, 11 Jun 2026 04:24:36 GMT  
		Size: 1.4 MB (1394935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7053b7edc10475c2c4219fcbafcdaa68460b254fc0f37b9ce94c177fb20f36a2`  
		Last Modified: Thu, 11 Jun 2026 04:24:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc5c991fdba4277fa6991ebe8b974a0fa349af5e7830ce228f1bfac146a2248`  
		Last Modified: Thu, 11 Jun 2026 04:24:36 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b9024d95d2d73eb0d20cd4a3a036bb683900444cc493c9c0cb777f6f8c1c89`  
		Last Modified: Thu, 11 Jun 2026 04:30:11 GMT  
		Size: 120.9 MB (120922666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c798bdbb4eaa0852bfeafd4fbc0690375f739aa93f6de2888702b8310d97d274`  
		Last Modified: Thu, 11 Jun 2026 04:30:08 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c56de57162889cb30f5a3f1dcb598af3fea1bc95e885a3b5382257a61ed7081`  
		Last Modified: Thu, 11 Jun 2026 04:30:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4102d190f3ad3011377fe6e02408f172249c1b3017bfd3c2d9e2e0ee2a4d8274`  
		Last Modified: Thu, 11 Jun 2026 04:30:08 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e6f8d9ade0e00d65cf864839a662f40f3a9a3a8f88555ee220452d4ec57b39`  
		Last Modified: Thu, 11 Jun 2026 04:30:09 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457c78d33901fa35ac90ade17b9f187f4902c0e125154280bb6262f1b0944836`  
		Last Modified: Thu, 11 Jun 2026 04:30:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:1c9450b243af7b4e24b0cce3de4f552e4dd91ac3bf4a74333a230a886ec2fb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5769460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c6fc9fce56936ff631862b79cca5a222c23d04e8bb9eec8889165c8c84845a`

```dockerfile
```

-	Layers:
	-	`sha256:c3eb14a756ca57c5d1273f4a49611e6ee399924cf64740fa6d4241dc8388f134`  
		Last Modified: Thu, 11 Jun 2026 04:30:08 GMT  
		Size: 5.7 MB (5715525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed66150a501f55d765d76eadb432c669983890cb1f7ebc665ddf0f396e1b910a`  
		Last Modified: Thu, 11 Jun 2026 04:30:08 GMT  
		Size: 53.9 KB (53935 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:0ba805475ef730721e4e34f72b2d84f8aa8f5b64de1692da84474dd81607047f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91603131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe234043b8bb9c29ed746ed01170d8869d7e056b5b19019a64e5e199a759fd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 02:50:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 21 May 2026 02:51:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 02:52:03 GMT
ENV GOSU_VERSION=1.19
# Thu, 21 May 2026 02:52:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 21 May 2026 02:53:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 21 May 2026 02:53:05 GMT
ENV LANG=en_US.utf8
# Thu, 21 May 2026 02:53:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 May 2026 02:53:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 21 May 2026 02:53:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 21 May 2026 02:53:48 GMT
ENV PG_MAJOR=16
# Thu, 21 May 2026 02:53:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 21 May 2026 02:53:48 GMT
ENV PG_VERSION=16.14-1.pgdg13+1
# Thu, 21 May 2026 09:09:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 21 May 2026 09:09:44 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 21 May 2026 09:09:44 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 21 May 2026 09:09:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 May 2026 09:09:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 21 May 2026 09:09:45 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 May 2026 09:09:45 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 21 May 2026 09:09:45 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 21 May 2026 09:09:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 May 2026 09:09:45 GMT
STOPSIGNAL SIGINT
# Thu, 21 May 2026 09:09:45 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 21 May 2026 09:09:45 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80fab2ceef62152f851f145dff3e1b25c48ee0dc516ea3c5f794f1de277e4a`  
		Last Modified: Thu, 21 May 2026 04:57:58 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebf27cb3c66e3558679585eb0ce15e35dffeb04046d13139cfa9828b8aecbe8`  
		Last Modified: Thu, 21 May 2026 04:58:00 GMT  
		Size: 6.3 MB (6293113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6e1d6536f4a123cdebd63843f1424aa7930dccbf70ff78c5840e6f97d7db65`  
		Last Modified: Thu, 21 May 2026 04:57:58 GMT  
		Size: 1.2 MB (1202056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3c1ee862684d21c2fb3519828f08b7512c7907ca5be82aefb1f418bc2b9541`  
		Last Modified: Thu, 21 May 2026 04:58:01 GMT  
		Size: 8.2 MB (8203742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0d86390b30ab815ee7aa2d1e66b827fd12b514cc6ac7eff4c2abf72df3b699`  
		Last Modified: Thu, 21 May 2026 04:58:01 GMT  
		Size: 1.4 MB (1402363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20245b197882c3268c4db6f39ac5a5b749ab3f254b9b660a1853e75ef0e4fcc`  
		Last Modified: Thu, 21 May 2026 04:58:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477520d6c39ceaa1976a3cc022938c17efc9385750f79c2651eacd989e9aa5f4`  
		Last Modified: Thu, 21 May 2026 04:58:02 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a572d0241d0bd40450f58f0147ecc15e6ae04ee1ea43c4a1d3c20ea106741cf4`  
		Last Modified: Thu, 21 May 2026 09:12:18 GMT  
		Size: 46.2 MB (46203190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3933b88f57a7089c45ec66446b78ba2d752e20417dd4fce8cf324d8f91d68b`  
		Last Modified: Thu, 21 May 2026 09:12:10 GMT  
		Size: 10.1 KB (10067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5676f102f0d2ff5b11ac3af5b96f8715dadcb337e1b2e47fd8da35eb7a4aec5`  
		Last Modified: Thu, 21 May 2026 09:12:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7a506b9e5de5b9265f88ae5557f32e5f1591b04ca9a10ced1ba4b04b57ab0f`  
		Last Modified: Thu, 21 May 2026 09:12:10 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab64f40574d89ba46666abec3f0b2fc68e6f87ace491d31970381fb8e3ba023`  
		Last Modified: Thu, 21 May 2026 09:12:12 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366cb211de7431978721f4cc7430a7716c6e9c0aab70371c43a117c359437646`  
		Last Modified: Thu, 21 May 2026 09:12:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:2dd36e2752e71f1ae4a609316d9081eecda39a2b44bff9548c0024d38fbc584f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ae718fe4ea7e6803ba2a545b8af3a62e2206895a95b6563dbfbafe7e13d5c4`

```dockerfile
```

-	Layers:
	-	`sha256:12e0e798379f94948c62fe09f0785fcb74c5ee1e7d23ea24380f8916212442ff`  
		Last Modified: Thu, 21 May 2026 09:12:11 GMT  
		Size: 5.1 MB (5075087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11b447155b34f3ce8921fe32c5bcb2392170b7e5b7d33168199547bc3b74412f`  
		Last Modified: Thu, 21 May 2026 09:12:10 GMT  
		Size: 53.9 KB (53929 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:2f81e68fef8b097a81c4878ed775beabc61f3d79d9de85bbe1ad6d3c4bb2cf08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174707205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040b4fe66fb1587634dc6ba150133b54a52c26e67959ba2c43a8dbc6915d9f6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:00:40 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 01:00:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:00:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 01:00:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 01:00:58 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 01:00:58 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 01:01:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:01:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 01:01:02 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 01:01:02 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 01:01:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 01:01:02 GMT
ENV PG_VERSION=16.14-1.pgdg13+1
# Thu, 11 Jun 2026 01:26:36 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:26:36 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:26:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:26:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:26:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:26:36 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:26:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:26:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:26:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:26:36 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:26:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:26:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dd188131c90506fcb0f3f26d26ed351d49a693abad8182c3afda4fa6d755b1`  
		Last Modified: Thu, 11 Jun 2026 01:14:23 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b6c6191c2eb66aa27cab597eb6d10d02197fd1265fe716a9bef498f85efbc2`  
		Last Modified: Thu, 11 Jun 2026 01:14:23 GMT  
		Size: 6.4 MB (6408457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1bda51e85fcfd8a3d159fcba8768faa6c0df08e2923fee6eae45876097c3ef`  
		Last Modified: Thu, 11 Jun 2026 01:14:23 GMT  
		Size: 1.2 MB (1230209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43b2d7764a44d9841fe0bdc2f91eee46bcd7429579a8fad294e26a37c008035`  
		Last Modified: Thu, 11 Jun 2026 01:14:23 GMT  
		Size: 8.3 MB (8258935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467d3b790824e42df0bcf828ab33342b4db2e33aa7df3d86f46bf05f2554a8d5`  
		Last Modified: Thu, 11 Jun 2026 01:14:25 GMT  
		Size: 1.4 MB (1398207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72de4c74a2edc0646d25dac113bfb364eb4278a07c67398b987e55cb365bb8f`  
		Last Modified: Thu, 11 Jun 2026 01:14:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9e139a01894a737b87c4e0a2731ba8e661db61e3894716ba6f53881ec597c8`  
		Last Modified: Thu, 11 Jun 2026 01:14:25 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcc3f2ef4ceb8e4c144f4ad6a14c97056d88c1256b48eb01ae8d9fd42f7c72e`  
		Last Modified: Thu, 11 Jun 2026 01:27:09 GMT  
		Size: 127.5 MB (127538986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0577c6aceef5f2cec1ea7b95d95d076484589627aecd943402c29f664bc6508`  
		Last Modified: Thu, 11 Jun 2026 01:27:07 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a805659ee6b0da3865e2c9f7b26ab9881d91564326b34d837c38c6d7e6ca155`  
		Last Modified: Thu, 11 Jun 2026 01:27:07 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae2626034129b85aa8f1fd652c3b7ef7d8c2c1e361aa40a9c3919e5409f5ad3`  
		Last Modified: Thu, 11 Jun 2026 01:27:07 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3a70e91f3f466b32001f5fe45fe352cccbe9c9bb39b7d69e987590ac19730e`  
		Last Modified: Thu, 11 Jun 2026 01:27:08 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d37685f30d69a869bc77be794cd482847ed0569d6d37e26bddd47cdc2737b2`  
		Last Modified: Thu, 11 Jun 2026 01:27:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:d9181f9e8afc47a11f63a06dd83de9796cbbe17f59572b63e92550f5131c72b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4654580599800390f9d9febebcb1d16fc05dcf86f63b6674ba5be8030105dc0`

```dockerfile
```

-	Layers:
	-	`sha256:37159e72c9905e4254c8c6959b16179bd28ad5dbad7ba0cb54c12126edaa5250`  
		Last Modified: Thu, 11 Jun 2026 01:27:07 GMT  
		Size: 5.7 MB (5725585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b528d9711ea6eabeedefcf08392083ff894aad44754ae9dd7d4fd795f32d8fa9`  
		Last Modified: Thu, 11 Jun 2026 01:27:07 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json
