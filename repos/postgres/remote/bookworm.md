## `postgres:bookworm`

```console
$ docker pull postgres@sha256:7ae0f6fddafc3e5040359e72576e3d979ae0219790562d7e4a5f94d420603c3d
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

### `postgres:bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:a40f5f7a480e2555f57baeaaf36450446c6b36ee21bdd223afd382d499ac7375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157126425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e46c43007657f30d859c2b11fb5b4c44901b00c1954b062b4aac6d3f752b58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:31:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:31:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:32:01 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:32:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:32:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:32:05 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:32:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:32:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:32:08 GMT
ENV PG_MAJOR=18
# Wed, 22 Apr 2026 01:32:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 22 Apr 2026 01:32:08 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Wed, 22 Apr 2026 01:32:22 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 01:32:22 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 01:32:22 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 01:32:22 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 22 Apr 2026 01:32:22 GMT
VOLUME [/var/lib/postgresql]
# Wed, 22 Apr 2026 01:32:22 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:32:22 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 01:32:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:32:22 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 01:32:22 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 01:32:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39537a938278b0eb76a960f2c6b3271ac91738b088478f773e853cef972278e`  
		Last Modified: Wed, 22 Apr 2026 01:32:40 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c47429d5a7a9c4c37325cfaea21a8e6ae1218910b0c6cda24e47c1743f761a4`  
		Last Modified: Wed, 22 Apr 2026 01:32:41 GMT  
		Size: 4.5 MB (4534218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112b2748e2f7991e7de0d16e9421ce20a0dd1d7aa0dd3ce61f077f7a7dcffa41`  
		Last Modified: Wed, 22 Apr 2026 01:32:41 GMT  
		Size: 1.2 MB (1249505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22267dbc312f6029f8cde1fa3f73c4a4c940e51dbae1a35986f3f39629ee0202`  
		Last Modified: Wed, 22 Apr 2026 01:32:41 GMT  
		Size: 8.1 MB (8066443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8722f746b4f8bb2ba31e0d0b36d31f75116b4fc83acf03e02d9eea4f4ada34`  
		Last Modified: Wed, 22 Apr 2026 01:32:41 GMT  
		Size: 1.2 MB (1196400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670af0e23811e0bb4104fb6d46b75889871f5d61265f6675b3950e3904d11630`  
		Last Modified: Wed, 22 Apr 2026 01:32:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d8f072c5c60a14e6bad10d37f114057f8763768a4b8fdec9547b730250797`  
		Last Modified: Wed, 22 Apr 2026 01:32:42 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd982f631ddae449d36fb112ca0d51a1b7051d578edcda04606a092e78b54dc`  
		Last Modified: Wed, 22 Apr 2026 01:32:45 GMT  
		Size: 113.8 MB (113813548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2b57a450d0ee50d77f75e0f1bab1ada407defbfddad34043e9dd8d443f9303`  
		Last Modified: Wed, 22 Apr 2026 01:32:43 GMT  
		Size: 19.2 KB (19226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52dcbc0469d4c058207c23ccfa7af8117ac3f13c4d443f72408b57cedfab9dc`  
		Last Modified: Wed, 22 Apr 2026 01:32:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fff4fd028db6b3bfebc1af44ae6d0d0412e192e53187d2cbedec0278f749e8`  
		Last Modified: Wed, 22 Apr 2026 01:32:44 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a50ca4e78eb6ab788c487feb24b07c1884aa7613772f7fe634558824d9fb8`  
		Last Modified: Wed, 22 Apr 2026 01:32:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a2529adb62c2d6a2da42b30269e6316bf38be8ac6094ea07526e887824799ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe36e2a925e234c7a3bf782403106f8649c49c94e64e01df136940fe3aaac33`

```dockerfile
```

-	Layers:
	-	`sha256:28c39e517c5a004aac283c432a6f687b33e2f7f7989775d2c08e271d9320088f`  
		Last Modified: Wed, 22 Apr 2026 01:32:41 GMT  
		Size: 6.2 MB (6156497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95926bba5d1615988851d1d004784a1e9d2f3b51b9699ef323f0695f3ab8643a`  
		Last Modified: Wed, 22 Apr 2026 01:32:40 GMT  
		Size: 51.6 KB (51589 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:b899e1ce870ec3c716fb1068946e34a84cfeb77ffafe2109e44dd4ca7b80ec07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87223025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5759a87220b333f7b63fff1e055218fc72ade7116a1fa07f7a04a6d18838872`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:19:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 02:19:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:19:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 02:19:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 02:19:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 02:19:40 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 02:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:19:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 02:19:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:19:47 GMT
ENV PG_MAJOR=18
# Tue, 07 Apr 2026 02:19:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 07 Apr 2026 02:19:47 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Tue, 07 Apr 2026 02:32:04 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 02:32:04 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 02:32:04 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 02:32:04 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 07 Apr 2026 02:32:04 GMT
VOLUME [/var/lib/postgresql]
# Tue, 07 Apr 2026 02:32:04 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:32:04 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 02:32:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 02:32:04 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 02:32:04 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 02:32:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4748d6bbb5a5b9e671dcabe2f909bdd7514f760a5cfdcd37d5b04627424120f2`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 25.8 MB (25765667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250b541138bf361848237aaefdb9b20f836308acbe3c833782e6bc7d75bad358`  
		Last Modified: Tue, 07 Apr 2026 02:32:17 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f95597210f8a7d2c4d3345f7a3f16ac93660569d18b06f2ccaeadab82033d67`  
		Last Modified: Tue, 07 Apr 2026 02:32:17 GMT  
		Size: 4.2 MB (4151297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d534945b1192cf0e32b3064dfa737de633dad38e3408542542a0a58c59e408`  
		Last Modified: Tue, 07 Apr 2026 02:32:17 GMT  
		Size: 1.2 MB (1220124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279eeba8279a04ef67fe5c6d90503cc78939dfded81a88af5211cb27294c2139`  
		Last Modified: Tue, 07 Apr 2026 02:32:17 GMT  
		Size: 8.1 MB (8066580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac64f3a39408578a5db85aa07177a86b45b89fc4c807c67815e439bb8c099ba8`  
		Last Modified: Tue, 07 Apr 2026 02:32:18 GMT  
		Size: 1.2 MB (1195087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41ac3e5f5cfb1a12863ba7b6f47886657b0d2085eb1321805fdce6933feb2ac`  
		Last Modified: Tue, 07 Apr 2026 02:32:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a111d5accd3fdf77aed93073edf13a4dced1c34d91b2a3ae7fd4ae4c6b769f`  
		Last Modified: Tue, 07 Apr 2026 02:32:18 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41511d86c51b4fd6071d09f41d58d8f577218adcc31f2de8769676af47ec578`  
		Last Modified: Tue, 07 Apr 2026 02:32:20 GMT  
		Size: 46.8 MB (46794456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eece727589a920defe7a0f51c280a29a63ff8579626e88c6892fa1cf64080665`  
		Last Modified: Tue, 07 Apr 2026 02:32:19 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e63cad1fe875566823b6c778493eb92019c4fa0a4156d9e6a6bf47e17b0dc6a`  
		Last Modified: Tue, 07 Apr 2026 02:32:19 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c741d04566766c1e626e9eb78bdad7f01747c40a6b38ef33e910950a5d145a`  
		Last Modified: Tue, 07 Apr 2026 02:32:20 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3a4b1a625839f34e517a86ab716f21c32c2a507426280f005d47f6aff16204`  
		Last Modified: Tue, 07 Apr 2026 02:32:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:515bf00ba4f758c7e7b449b93f90848fae09447b16e05496f662b855174705b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b29f46940642b032abc032ee0c0bcfd0d452de93ef16fb928d389a5b9e50d00`

```dockerfile
```

-	Layers:
	-	`sha256:737666952a8ed0f181dc572d4738f35292928ea6b509b33d9ff9630e209e0898`  
		Last Modified: Tue, 07 Apr 2026 02:32:17 GMT  
		Size: 5.3 MB (5317016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53bf5307d3f5ab472f6676fe9b1d5c594103cd18d319e4cbecf748a1f7f64462`  
		Last Modified: Tue, 07 Apr 2026 02:32:17 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:48338900736fc0ff96e79075b5261ddfa5f905c89c1d0c4bcb2b846c7166bd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83343880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632cf431f20814dfd9ed42b549fd50a5be06f3dcecc46943b8a650b0a93de52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:36:11 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:36:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:36:25 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:36:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:36:31 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:36:31 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:36:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:36:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:36:36 GMT
ENV PG_MAJOR=18
# Tue, 07 Apr 2026 01:36:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 07 Apr 2026 01:36:36 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Tue, 07 Apr 2026 01:48:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 01:48:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 01:48:12 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 01:48:12 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 07 Apr 2026 01:48:12 GMT
VOLUME [/var/lib/postgresql]
# Tue, 07 Apr 2026 01:48:13 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:48:13 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 01:48:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:48:13 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 01:48:13 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 01:48:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d443fbe4a0e6423a64b646ad6edea8925cce40e0bf48de3c31726b7d94c67aa2`  
		Last Modified: Tue, 07 Apr 2026 01:48:24 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e199b3b376af2fb673c06a12150c495f903db93a482c4871a4cbbbbd430ba91`  
		Last Modified: Tue, 07 Apr 2026 01:48:25 GMT  
		Size: 3.7 MB (3742705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cdd415439032cfa38b1468aff82b8d323e2eee32e5ff9c66fe4de03055f47b`  
		Last Modified: Tue, 07 Apr 2026 01:48:25 GMT  
		Size: 1.2 MB (1216038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541d6a3d2c253cbf5cb61497b9a4167f201a6aad37617a1d4fca64dedeea9f6e`  
		Last Modified: Tue, 07 Apr 2026 01:48:25 GMT  
		Size: 8.1 MB (8066428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed970f24b64957fbd70dac7e383f3c81a9e2a6ce6100f6ec78f5f7f17a74b34`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 1.1 MB (1067267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37de465ca5639080b00af2e88dd0d91b9afe95ad27ab9e819ceb45de74bab9ef`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efa476c687fa958f8786685d75a9f198764e2ce070808fcb42986c19a62956c`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e40d11db649cccf1f114cf39514df9c67aaa5245d4e4d0d18cbc7e1323de0d`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 45.3 MB (45280167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65397803b01aa5b32634222711cf4af1190f6134d704d943e7e96ae13ae1558`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 19.2 KB (19231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc34bb6cabcc2f4a342ff8eb9659d8e28d29280d7322f5e142d901ef2371375`  
		Last Modified: Tue, 07 Apr 2026 01:48:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e39aeb102a6f89537c16c7276e202c77e0c5cf81739d9d39cf5d7cee1d933c5`  
		Last Modified: Tue, 07 Apr 2026 01:48:28 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d85981ef6848e327bdd649b2d39e8ac26533a3a2acd5034c6528a697ac96d8`  
		Last Modified: Tue, 07 Apr 2026 01:48:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b76170f04b81170d47b2a744c9aa7b304e4e1c240bcf63df8491df6953bfd056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df1c3c7ddb04e3773bae452439f19491d68f11d27549de82dc085af64f6bc5f`

```dockerfile
```

-	Layers:
	-	`sha256:03e92220978497122aa24c5ad076aabbb841754dea88888ba0d12318f4210b4a`  
		Last Modified: Tue, 07 Apr 2026 01:48:25 GMT  
		Size: 5.3 MB (5316267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ec330f4d5c15c46212055ed70f4bb7c86cd8792e1f02049679fd6b7ed41151`  
		Last Modified: Tue, 07 Apr 2026 01:48:24 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:13fae98985d1dd0cd32a38089a44b82234b054a46ee08d9fe2ceca50de878013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155112508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69901f2d4ecd9578255fcb2ea73b06ce25746387550cca90681f0823f640d4e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:34:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:34:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:38 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:34:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:34:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:34:43 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:34:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:34:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:34:46 GMT
ENV PG_MAJOR=18
# Wed, 22 Apr 2026 01:34:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 22 Apr 2026 01:34:46 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Wed, 22 Apr 2026 01:35:01 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 01:35:01 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 01:35:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 01:35:01 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 22 Apr 2026 01:35:01 GMT
VOLUME [/var/lib/postgresql]
# Wed, 22 Apr 2026 01:35:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:35:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 01:35:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 01:35:01 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 01:35:01 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 01:35:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08eed14005f34bb2aeec293980655dbe5aede955fe72541caaf8bddafc25477a`  
		Last Modified: Wed, 22 Apr 2026 01:35:20 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a014dec7c8cd32f43ddd5bb4147d718eb25745be001d818ba9b24d84522d992c`  
		Last Modified: Wed, 22 Apr 2026 01:35:20 GMT  
		Size: 4.5 MB (4519525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfb4c4884f5ce59c7fc8041e38e2e4208828a22f7d2886eafdbdc6ff0d266b4`  
		Last Modified: Wed, 22 Apr 2026 01:35:20 GMT  
		Size: 1.2 MB (1203278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d622c49201d1fb7e8ba4e42c99d89c7ddb01c261433c6beee4d4cdae2d94f3e`  
		Last Modified: Wed, 22 Apr 2026 01:35:21 GMT  
		Size: 8.1 MB (8066541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224544e94ad28559fe091964d70a412bf223edd455d1cb5f8008eb6e3358c5ab`  
		Last Modified: Wed, 22 Apr 2026 01:35:22 GMT  
		Size: 1.1 MB (1109001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acd19f9c113d408c35e048001e27ed93d5b5a16a9f61552a014d73f63b9aee0`  
		Last Modified: Wed, 22 Apr 2026 01:35:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc698f982457cdd91d562cb196f09004ea36aa77bd071f4f350267947c24ed3`  
		Last Modified: Wed, 22 Apr 2026 01:35:22 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7340b2ba999fddbea84b1769c22d6118f2305962ed9c0e8719fa11b08a75f514`  
		Last Modified: Wed, 22 Apr 2026 01:35:25 GMT  
		Size: 112.1 MB (112067988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f636d2ab10d702d25ef6e6239ad6de6166b0ec60cd051b66d10fd6a475ecaced`  
		Last Modified: Wed, 22 Apr 2026 01:35:23 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924e4c6160417e617074d3d87d5cff094f27b99705ff3c724add0e8ace61314a`  
		Last Modified: Wed, 22 Apr 2026 01:35:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777836f23854a8b452cbf19a971b4fbabc0c7c9b7c60f384cf80068d555da8f0`  
		Last Modified: Wed, 22 Apr 2026 01:35:23 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887facb75e7e8f4f31d42ed64757724a7237da33410459dc104f89f82443bb06`  
		Last Modified: Wed, 22 Apr 2026 01:35:24 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:55a824f081889f6bac64b6e54c6b84daace3c200ec4a5c6a47f167c093209cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e872dad97e9066a6ec0677227343b411f7bf5b9e4035ce00ec939de0f7f7d900`

```dockerfile
```

-	Layers:
	-	`sha256:b9a8f974276ef8a1fb13f68e84f6629a114f7526e12106166980727d63289776`  
		Last Modified: Wed, 22 Apr 2026 01:35:20 GMT  
		Size: 6.2 MB (6162822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f0a316a9e20ab65d722a7d1878aecd6c5802106649d2c3142cf72e5d6dbd8ac`  
		Last Modified: Wed, 22 Apr 2026 01:35:20 GMT  
		Size: 51.8 KB (51831 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; 386

```console
$ docker pull postgres@sha256:8d909a8cf0b00fb3ac0c7089e6aa442962b6e20d2561889dc342814357762f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93997320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46bce29b8d474bfdf062a7a5bec4c8a372d3cad1c7322a30d75bfc5701980b88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:35:32 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 01:35:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:35:44 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 01:35:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 01:35:48 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 01:35:48 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 01:35:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:35:51 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 01:35:52 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:35:52 GMT
ENV PG_MAJOR=18
# Tue, 07 Apr 2026 01:35:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 07 Apr 2026 01:35:52 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Tue, 07 Apr 2026 01:43:56 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 01:43:56 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 01:43:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 01:43:56 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 07 Apr 2026 01:43:56 GMT
VOLUME [/var/lib/postgresql]
# Tue, 07 Apr 2026 01:43:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:43:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 01:43:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:43:56 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 01:43:56 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 01:43:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b327ba64b58baecfbc5a81ae6c0f1db3aead661553c6928d56153864986f56ee`  
		Last Modified: Tue, 07 Apr 2026 01:44:08 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537458c30408745139c4562a4cb86ed5b929689ab7f234721118853377623787`  
		Last Modified: Tue, 07 Apr 2026 01:44:08 GMT  
		Size: 5.0 MB (4966077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ee29994c89f8e2402d409dcbfe2a5d14006c1fee4cc4ea336f7b01d526f563`  
		Last Modified: Tue, 07 Apr 2026 01:44:08 GMT  
		Size: 1.2 MB (1218633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03e8d0c56e554b18e551168e50dc0d10d102d18581df2d58c58a949b39423cc`  
		Last Modified: Tue, 07 Apr 2026 01:44:08 GMT  
		Size: 8.1 MB (8066428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4d9080d7a302b36ade1ab2e76d12210814e0764da24f88d360041e703e74d5`  
		Last Modified: Tue, 07 Apr 2026 01:44:09 GMT  
		Size: 1.1 MB (1137451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cd1ce67744451f0849eab9456440bf898b5435cb884f580a42242d4ad9ab6f`  
		Last Modified: Tue, 07 Apr 2026 01:44:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7336377545dfef74290357509851fd69f600e7275d720920168a442427efa3`  
		Last Modified: Tue, 07 Apr 2026 01:44:10 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49421e175672766dea407e5fe9439d0945694f3c79a576ef02991fad06cc1eb9`  
		Last Modified: Tue, 07 Apr 2026 01:44:11 GMT  
		Size: 49.4 MB (49357152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6e325d8577a6518498ea2d42d89fce9774da7116e09f1e8208943cbe492f6b`  
		Last Modified: Tue, 07 Apr 2026 01:44:10 GMT  
		Size: 19.2 KB (19233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37c597364a4b8bf8e7c6107e54e6a943fe6901daf7973f89995e885ee9e85dc`  
		Last Modified: Tue, 07 Apr 2026 01:44:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1a431084b1bd3458f98e461fe1a73965b3896af4a5cfcf45940c5f9187b2ff`  
		Last Modified: Tue, 07 Apr 2026 01:44:11 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4e7c1130cb891f74002186844ef7653d7692f5284a932b4ab6d44544968d2c`  
		Last Modified: Tue, 07 Apr 2026 01:44:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:62531700dc86104496ee9e04610aaf9958f618cd792adb470a5b6d65cc5b5d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd722d08631724087a717a457c01d0689e7a0bc213c67898faa37f6d0aa1a8d`

```dockerfile
```

-	Layers:
	-	`sha256:76e161c71bc9506cea2fc5b7e6546eaed7c11b5b91ef098edc71b1474888d744`  
		Last Modified: Tue, 07 Apr 2026 01:44:08 GMT  
		Size: 5.3 MB (5311582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034f018958a30b784b029047bcb331b68d63afe9fc8a867e01206c56f6a8844b`  
		Last Modified: Tue, 07 Apr 2026 01:44:08 GMT  
		Size: 51.5 KB (51538 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:68eb5fff8c6acbf222da32d43794444710ce9f37a2cd039d2dc3cd11ba7468cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155993866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d4e24bf69ae9a5a07ac8a35aa3b576c1627d4e5353293bbaa85a8c988f3722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 08:36:10 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 08:36:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 08:37:18 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 08:37:18 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 08:37:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 08:37:45 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 08:38:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 08:38:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 08:38:08 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 08:38:08 GMT
ENV PG_MAJOR=18
# Tue, 07 Apr 2026 08:38:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 07 Apr 2026 08:38:08 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Tue, 07 Apr 2026 09:48:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 09:48:58 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 09:48:59 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 09:48:59 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 07 Apr 2026 09:48:59 GMT
VOLUME [/var/lib/postgresql]
# Tue, 07 Apr 2026 09:49:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 09:49:02 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 09:49:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 09:49:02 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 09:49:02 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 09:49:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7377a524ccdc918cca6272a35a48618805ffa8fb443fe7f687971509cb1f8d53`  
		Last Modified: Tue, 07 Apr 2026 00:10:05 GMT  
		Size: 28.5 MB (28526285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8577deaa1ee6306b521ee5d84ddaf65f0450bfb69e5e2e10ace88d337c6cba4f`  
		Last Modified: Tue, 07 Apr 2026 09:51:03 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2193f14079132665de93d8fc43dbccb2d7e4a15aa9874d91ad7b6e9774f5548b`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 4.5 MB (4475247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9d1210a9eb3ea5aff9a27d0fed962b67d985e781ebf9b4aeae64f122914c0`  
		Last Modified: Tue, 07 Apr 2026 09:51:03 GMT  
		Size: 1.2 MB (1159244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e47fef44ca5ddd3d584b459d7fa9e53ad74dda9d20319868217ecaefd5e4ead`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 8.1 MB (8066561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64e531094ee8eda299eb99703ce16f6ccb0dec62e0d8395c5229bdf89943ae6`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 1.2 MB (1182905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66a1323700edb806f7d1852762ef08ab512cd2cb6d3d752c4ce5cc357bab520`  
		Last Modified: Tue, 07 Apr 2026 09:51:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c09b94ca6add0648b12298fad493162ceca74e3a56abda4b44871cf3d96266d`  
		Last Modified: Tue, 07 Apr 2026 09:51:05 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2915876d6bcd7a5b9ada9c4d2632f3aa2b2c1bb25b32542c759bf2ed48a87575`  
		Last Modified: Tue, 07 Apr 2026 09:51:17 GMT  
		Size: 112.6 MB (112553806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946b315d28152cc7c33dcc59f911ae428a9ac2af15aa4aa9fea3d5b6b4d5a352`  
		Last Modified: Tue, 07 Apr 2026 09:51:05 GMT  
		Size: 19.2 KB (19231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494278e2bae2a42709ba0a3412ab19e3b720dcf2c56556f2764ae3d1ab817b19`  
		Last Modified: Tue, 07 Apr 2026 09:51:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a4cc82ea4f81d4c4944885ca954e9d035c84fd92ec0cd53e563d302a5bb040`  
		Last Modified: Tue, 07 Apr 2026 09:51:06 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b34d1ababd91ab1f1cf391e92a8f99455d40f195c594a0372062787b0b88de`  
		Last Modified: Tue, 07 Apr 2026 09:51:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:afc58868a3c1e76ed468985418f665ab0afe2e31dd0f50948757c68380bec631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 KB (51462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e7a1c1ccf96f021386f8153df6faa0ae3c51b0e6f70b665088fb8b076eaa3d`

```dockerfile
```

-	Layers:
	-	`sha256:e85a575c87760c82c7fc89ba1ab23a0ebb4f7bf4d0160f46be800b13d5b68e90`  
		Last Modified: Tue, 07 Apr 2026 09:51:02 GMT  
		Size: 51.5 KB (51462 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:8ec257ec27d932a3c88916d5453da330c07a94c5a57f706d55a840acab007b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.0 MB (170031855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202c56c1818683746775f970b70e96fa26846dcd4552343e10300e944b7d0296`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:01:02 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 07 Apr 2026 04:01:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:01:34 GMT
ENV GOSU_VERSION=1.19
# Tue, 07 Apr 2026 04:01:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 07 Apr 2026 04:01:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 07 Apr 2026 04:01:43 GMT
ENV LANG=en_US.utf8
# Tue, 07 Apr 2026 04:01:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:01:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 07 Apr 2026 04:01:53 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PG_MAJOR=18
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Tue, 07 Apr 2026 04:01:53 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Tue, 07 Apr 2026 04:03:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 07 Apr 2026 04:03:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 07 Apr 2026 04:03:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 07 Apr 2026 04:03:24 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Tue, 07 Apr 2026 04:03:24 GMT
VOLUME [/var/lib/postgresql]
# Tue, 07 Apr 2026 04:03:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 04:03:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 07 Apr 2026 04:03:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 04:03:24 GMT
STOPSIGNAL SIGINT
# Tue, 07 Apr 2026 04:03:24 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 07 Apr 2026 04:03:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c73a4e80f8eee9e890cb47bedd35d02c67ef5bcca2b473c6d3e00a80965b06a`  
		Last Modified: Tue, 07 Apr 2026 04:04:12 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7947f119f83a299b47ca573148739e01949d18cbaa9318e7ab4a40e85e5823df`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 5.4 MB (5368665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2363b8d0c3c8477a5c830c8f04da66b6b2dbe1de9983fe4475a83363c62b90`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 1.2 MB (1208247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73441d3fd6b801869bfe2128fece0f8cfd3dae11351c3d17ba334f6a60758933`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 8.1 MB (8066577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825f5e783521a55f9a2725ca3ae6863c9ebc88d6eeb23db6ad9f4a50720cb7f`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 1.3 MB (1283671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255852130442a8dd66f03e76d6c53fb783681b9f0b0f0deb8976c69d771ebc43`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b958c25dd0ceaa8626e0e80c7b5ef496a8edd59a35e667fc15c63e5053d77b`  
		Last Modified: Tue, 07 Apr 2026 04:04:14 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870bfbc52a89cbde325818236d938595e637758cb99bc4767dd40ecd74878a47`  
		Last Modified: Tue, 07 Apr 2026 04:04:18 GMT  
		Size: 122.0 MB (121996414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4983e505271b5d9f4ce6dfbe757cea8791c9de07efb240cec1a930e78bd2f0a6`  
		Last Modified: Tue, 07 Apr 2026 04:04:15 GMT  
		Size: 19.2 KB (19235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea2f12fa1fdade688ea6fe2df464d65df014acd8e81bff5df22f3ea908c015`  
		Last Modified: Tue, 07 Apr 2026 04:04:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a490416ebfaaa9cbd0a01ce020a6bdd933fe139f72977bcea1cf80251b29a187`  
		Last Modified: Tue, 07 Apr 2026 04:04:16 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2f1dcfb46e2df4046840376e2a06a3451db20c80809af3472746428d42175b`  
		Last Modified: Tue, 07 Apr 2026 04:04:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a03e3fc1dd88e66bef75be2fd58a25836419d7055da0d9769c0d1386da288346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34890c82a24b015b569d0776db2d968ad22aab47186ac792e8c7da4b8a770a7b`

```dockerfile
```

-	Layers:
	-	`sha256:b0b41d014c43d2de00382b8a7a002a44bf4533bebee88f0b1b5796ee326b84c1`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 6.2 MB (6163882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebea073407c176bbab7101ad0fdbaca0030c67bf8f643ec8e3cf0e0c47382e96`  
		Last Modified: Tue, 07 Apr 2026 04:04:13 GMT  
		Size: 51.6 KB (51648 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:2866c093fadf48d37e4933e4f9d2ea7cbfe367b30ca16c559696a58fb663f17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166447050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2caba80476ae98a6d5f354a37dedd4c6241d7c39cdb5241e79cb3bce1e508cee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:57:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 22 Apr 2026 01:57:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:58:03 GMT
ENV GOSU_VERSION=1.19
# Wed, 22 Apr 2026 01:58:03 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 22 Apr 2026 01:58:09 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 22 Apr 2026 01:58:09 GMT
ENV LANG=en_US.utf8
# Wed, 22 Apr 2026 01:58:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:58:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 22 Apr 2026 01:58:13 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:58:13 GMT
ENV PG_MAJOR=18
# Wed, 22 Apr 2026 01:58:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 22 Apr 2026 01:58:13 GMT
ENV PG_VERSION=18.3-1.pgdg12+1
# Wed, 22 Apr 2026 02:11:19 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 22 Apr 2026 02:11:19 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 22 Apr 2026 02:11:20 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 22 Apr 2026 02:11:20 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 22 Apr 2026 02:11:20 GMT
VOLUME [/var/lib/postgresql]
# Wed, 22 Apr 2026 02:11:20 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:11:20 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 22 Apr 2026 02:11:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 02:11:20 GMT
STOPSIGNAL SIGINT
# Wed, 22 Apr 2026 02:11:20 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 22 Apr 2026 02:11:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902f96924f46ebf5f9f8ede07708f5b0c8adeebd2738997fa3533ddf09a9dbd2`  
		Last Modified: Wed, 22 Apr 2026 02:11:50 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd6b3c43306aab3a4d709a248ab52f9fcf51cea15d3562af15efab3e151778c`  
		Last Modified: Wed, 22 Apr 2026 02:11:50 GMT  
		Size: 4.4 MB (4391190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c975be715805f88cd7ca53c71cf4ad87abe05611622dbe51758f202354ccdf20`  
		Last Modified: Wed, 22 Apr 2026 02:11:50 GMT  
		Size: 1.2 MB (1222850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fb7898d62d3b5cc45226935beb6ef98f3b90ac1aa7a351b722965f433d5b91`  
		Last Modified: Wed, 22 Apr 2026 02:11:51 GMT  
		Size: 8.1 MB (8120734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa45b451fd41ac0fc29f0036aee5af47adbf50d0dbeba4bb9747a561a4ba57c`  
		Last Modified: Wed, 22 Apr 2026 02:11:51 GMT  
		Size: 1.1 MB (1097057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2886a6b125298c89789fc412cbff612f6352a3a79466fbc3688d9700b0204c`  
		Last Modified: Wed, 22 Apr 2026 02:11:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e4cbd2baa5dc3fe9ddda001bbb8dc69add1a85f600ca7ef0a8682c1462e32`  
		Last Modified: Wed, 22 Apr 2026 02:11:51 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561636353a932f78e7f11618724b5670de87f960daa4ee5222ba2ba05f8d0de5`  
		Last Modified: Wed, 22 Apr 2026 02:11:55 GMT  
		Size: 124.7 MB (124693590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce871e01dfb1c50ae62808487fc893e3d1ae3b539297d38b2808aafc0806690f`  
		Last Modified: Wed, 22 Apr 2026 02:11:52 GMT  
		Size: 19.2 KB (19229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b036813a2d2e93ec14d90da871f62b296a2b49856065515f7a0d2c45811cbbb1`  
		Last Modified: Wed, 22 Apr 2026 02:11:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2f4c1b002a09a57cbd0e96671aaa4bdd19af279e50463c1e1197a3d65c7dae`  
		Last Modified: Wed, 22 Apr 2026 02:11:53 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f67ed0a29bd34d9621712d209aa4a56e5a6ff86197d4daa20fe846f550b4267`  
		Last Modified: Wed, 22 Apr 2026 02:11:53 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6b0688045f7cbfe22e5222e484908758c119237490621ff07ba019a4b453bf2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e6e02c76213910573247e6fea9510ec6b48c31354b59f63be1ecf9e442c48e`

```dockerfile
```

-	Layers:
	-	`sha256:93f4662e285b09221776ce08bcfdfff81b6480320fc7a20f7b504effef8c2775`  
		Last Modified: Wed, 22 Apr 2026 02:11:50 GMT  
		Size: 6.2 MB (6171155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40fce43a9b01a898326f87d34597da9ad423e92d8b498e0a0603462b5bfaf1d`  
		Last Modified: Wed, 22 Apr 2026 02:11:50 GMT  
		Size: 51.6 KB (51589 bytes)  
		MIME: application/vnd.in-toto+json
