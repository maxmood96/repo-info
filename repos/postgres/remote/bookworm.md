## `postgres:bookworm`

```console
$ docker pull postgres@sha256:1829ec00953c4b23e8d930331082b2a0ae422f0953c6a35c14a8f8b67139806c
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
$ docker pull postgres@sha256:ac713b34d0aa9872bd8e05aade67005b1e34eab42875b51edf86c1701fecf33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157185275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4984829ec593842a6084e421a8c517395820ba66b7aea6961acafca3ec69fca1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:32:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:32:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:32:56 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:32:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:33:00 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:33:00 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:33:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:33:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:33:04 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:33:04 GMT
ENV PG_MAJOR=18
# Wed, 24 Jun 2026 01:33:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 24 Jun 2026 01:33:04 GMT
ENV PG_VERSION=18.4-1.pgdg12+1
# Wed, 24 Jun 2026 01:33:18 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:33:18 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:33:18 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:33:18 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 24 Jun 2026 01:33:18 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 01:33:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:33:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:33:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:33:18 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:33:18 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:33:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b1c55d5f7193e99ca9114db20f77cbf6f8ac2665f2fcdc6a2f7ae372dacfc5`  
		Last Modified: Wed, 24 Jun 2026 01:33:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c511dfc50a83d74c3752c2717fb1601d53ea5d1795941db25b8633afe5ea18db`  
		Last Modified: Wed, 24 Jun 2026 01:33:38 GMT  
		Size: 4.5 MB (4534245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c160f6c1be79bd852b990395a53c6c8ac0ac55270622dc6d570ca797c287dd`  
		Last Modified: Wed, 24 Jun 2026 01:33:38 GMT  
		Size: 1.2 MB (1249498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eff3a500cfa56e52c913ee90673f6947915b690dc4e814b81363ab768b6a7cb`  
		Last Modified: Wed, 24 Jun 2026 01:33:38 GMT  
		Size: 8.1 MB (8066432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa8b8ad69ea07f5da499fae5f4825da86df84d00848f29ea22f7a4c8279695c`  
		Last Modified: Wed, 24 Jun 2026 01:33:39 GMT  
		Size: 1.2 MB (1196405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8df7ac4259f0848f3bf0bc91f55469a7e6448ffa9e360c5e112f8e0a203d9f`  
		Last Modified: Wed, 24 Jun 2026 01:33:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7931df14d872f4f5d1b726f08c1d59191e91216d756cc071fc377275c1afc8d7`  
		Last Modified: Wed, 24 Jun 2026 01:33:40 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c9aafdfdd3ccca60f71d468dbca2cea68d12c3fc0ac1fcdc64583908c35dfe`  
		Last Modified: Wed, 24 Jun 2026 01:33:43 GMT  
		Size: 113.9 MB (113870993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32bd2436143cf1bd222f0a141111ddf3e426a6ff700421738e6174adb9feae1`  
		Last Modified: Wed, 24 Jun 2026 01:33:41 GMT  
		Size: 19.2 KB (19230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a429d6e4ed30cff7f99e0aae3b8975eb43455355d47204ad11981076189949`  
		Last Modified: Wed, 24 Jun 2026 01:33:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1240b1b343c7c26796c92f6621da178bb92c79f7395b02acc55c125c7639c104`  
		Last Modified: Wed, 24 Jun 2026 01:33:41 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a29732b37f614e69bc58918c0e06ed39faace1a503126a9d23613702abe53d`  
		Last Modified: Wed, 24 Jun 2026 01:33:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:aad5e8418b6fa12d20f1447702547fc4284b8c698da8d07fe4ba7ec36260e118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6208123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07778d70ebb4240379e184656de27bd9f7f91dc231d4e23aae758a82b9727eb0`

```dockerfile
```

-	Layers:
	-	`sha256:872fbd062bed55be18b78ee7c5572e3625b69fe9f2c2c74378992afdfeaef816`  
		Last Modified: Wed, 24 Jun 2026 01:33:38 GMT  
		Size: 6.2 MB (6156533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3451ee88fe7f25f3e88adada52c468badcd00441e921d226a1c32eaee87e6b96`  
		Last Modified: Wed, 24 Jun 2026 01:33:38 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:b0e09467c10e6cfc426422b7c1313f3dce94c72d4ce6bbe9a328bd68236c8039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87265002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a7b48934bf9a55deb1500049ba7a447f8259f66505f9bdc7e82fa84c6716c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:43:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:43:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:43:43 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:43:43 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:43:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:43:50 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:43:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:43:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:43:56 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:43:56 GMT
ENV PG_MAJOR=18
# Wed, 24 Jun 2026 01:43:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 24 Jun 2026 01:43:56 GMT
ENV PG_VERSION=18.4-1.pgdg12+1
# Wed, 24 Jun 2026 01:56:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:56:15 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:56:15 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:56:15 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 24 Jun 2026 01:56:15 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 01:56:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:56:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:56:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:56:15 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:56:15 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:56:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:56a07f407b343196efb8a614d5b61dad4cbe8fd8c8e97a11342cd7a61eadc02c`  
		Last Modified: Wed, 24 Jun 2026 00:27:42 GMT  
		Size: 25.8 MB (25773229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd9601a57c2aa5a30aa806afe8de15a3040b9fc96cb978d592f2f39cdfde5ca`  
		Last Modified: Wed, 24 Jun 2026 01:56:27 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871469ce9cd491bfdd03d244a508d6d1a01c4713c0de1522a3599e5349e07acd`  
		Last Modified: Wed, 24 Jun 2026 01:56:28 GMT  
		Size: 4.2 MB (4151330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70c8f736cafd8ab66af1b3d3e2512a602ebccdd8cbbfdff6015ded2bd198122`  
		Last Modified: Wed, 24 Jun 2026 01:56:28 GMT  
		Size: 1.2 MB (1220113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e84920db3f5ab06b9f89e61e56affce9a10cbe43ee1dcdc5a13da9e3c205fb5`  
		Last Modified: Wed, 24 Jun 2026 01:56:28 GMT  
		Size: 8.1 MB (8066579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3198888aad33f186a1af90d51159e98b2e827933dd9ba01afff2c1103ec85ba`  
		Last Modified: Wed, 24 Jun 2026 01:56:29 GMT  
		Size: 1.2 MB (1195076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb664eb2b80971dd6523a484579324fe1b62edd1fa3c3611d960847ae855b7`  
		Last Modified: Wed, 24 Jun 2026 01:56:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53b0d4e5d4b2b6bd3e20810a966fdd8046854c4472c3ab1244f5570997a876e`  
		Last Modified: Wed, 24 Jun 2026 01:56:29 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce8bbc03051e3a18ea85b89d24115740abcdc41de41733b1a0b1ee1fe4f9cef`  
		Last Modified: Wed, 24 Jun 2026 01:56:30 GMT  
		Size: 46.8 MB (46828607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdec238475dd57904ada7119e84c7ad410b1e2ac8a303fb7c74b28295cb3194`  
		Last Modified: Wed, 24 Jun 2026 01:56:30 GMT  
		Size: 19.2 KB (19233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf84c39c35d2d0e55391915e7b557345bc75a77eef98fd9a8a17f316c88be670`  
		Last Modified: Wed, 24 Jun 2026 01:56:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552080d9b131914fb1a2e49a4f7686ec6960c4ee71fa603d73b413b25d0a00ef`  
		Last Modified: Wed, 24 Jun 2026 01:56:30 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eed356c2961916acbfa90f3c20babbf045aee90e58341f54a14f7986e10f4df`  
		Last Modified: Wed, 24 Jun 2026 01:56:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:29410cf2f96a2822c4cf21b97d670cee407fa080829b3cae741ab07a551e05ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2cc8334f16d5393f80d427a6619672a541d3a8135992c1ab16fd00ee5e2a11`

```dockerfile
```

-	Layers:
	-	`sha256:91638b9ee4be03f9dd29127e38799ccc129c98712faae6bdd1b391f9113f6203`  
		Last Modified: Wed, 24 Jun 2026 01:56:28 GMT  
		Size: 5.3 MB (5317052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:754c63f173cf1131b24436dae2c034a57bb8110d076d181fbc0a25710bd8bc38`  
		Last Modified: Wed, 24 Jun 2026 01:56:27 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:c951a3420d2fb3a92e8fcda0ffb0063c9444380dbc4e8aae9991dd803a480205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83368525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d84f57979b26d50f6b637c653cc1cc9d61987ad641c522f7ef1f7ce3f42c782`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:56:39 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:56:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:56:52 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:56:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:56:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:56:57 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:57:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:57:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:57:02 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:57:02 GMT
ENV PG_MAJOR=18
# Wed, 24 Jun 2026 01:57:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 24 Jun 2026 01:57:02 GMT
ENV PG_VERSION=18.4-1.pgdg12+1
# Wed, 24 Jun 2026 02:08:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 02:08:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 02:08:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 02:08:52 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 24 Jun 2026 02:08:52 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 02:08:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:08:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 02:08:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:08:53 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 02:08:53 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 02:08:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0ead8fe4feab98996b3feb5f196406b6d02e126a6955d96078d2f12294dacb62`  
		Last Modified: Wed, 24 Jun 2026 00:27:49 GMT  
		Size: 23.9 MB (23944532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93ddd8b888494d2b25a46e7adb89cdbd164a6524a61d5755dc2bc70f51c53a`  
		Last Modified: Wed, 24 Jun 2026 02:09:05 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5ace89f19f6ee7ce6314e3917841dfadb375116b8b511d3ff8b90f1330d52e`  
		Last Modified: Wed, 24 Jun 2026 02:09:05 GMT  
		Size: 3.7 MB (3742702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d48f0fcd9f316b6ed03ebcd04d4ec420d21cc55193c006459fba1d7de4b51a4`  
		Last Modified: Wed, 24 Jun 2026 02:09:05 GMT  
		Size: 1.2 MB (1216015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c115f395d6cd3383deedc48c7fca0dfa7221db65c1759eb4f51db225c15ee08e`  
		Last Modified: Wed, 24 Jun 2026 02:09:06 GMT  
		Size: 8.1 MB (8066402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b473c4f50d947bf51373e91bd7a7fc4af679da06c3ab6ea4a9d86525b4e7000`  
		Last Modified: Wed, 24 Jun 2026 02:09:06 GMT  
		Size: 1.1 MB (1067279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a726efbdd89c9f8faae78cf3a49b8dc410348629831a7cc3cadbc82abd504e7b`  
		Last Modified: Wed, 24 Jun 2026 02:09:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f797ef0fa218c149057afe4e9aa01b20dabc520fc93f7cedd56301ba85f0dfcc`  
		Last Modified: Wed, 24 Jun 2026 02:09:07 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9310fc366df8e913fcb7f4a9dc1e1232077323a4a47ef9aab267a8c91a694791`  
		Last Modified: Wed, 24 Jun 2026 02:09:09 GMT  
		Size: 45.3 MB (45301530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda1008cde7e77356e190d653cb24e0c666283055e9c96fa3ee786cdaabe1a42`  
		Last Modified: Wed, 24 Jun 2026 02:09:08 GMT  
		Size: 19.2 KB (19231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a419baf42c5b46b481fac37e4e53fb8c4824a1db14ba77a3bfccdf65c25b1a`  
		Last Modified: Wed, 24 Jun 2026 02:09:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8462784f01d35607be41a611dd6915818daa3f547395a901c56dd7cf8aee76c1`  
		Last Modified: Wed, 24 Jun 2026 02:09:08 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fe056a1ac8568bb4f99dec840017b919917005ca24c927074142c6f1de4c35`  
		Last Modified: Wed, 24 Jun 2026 02:09:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:50edd0208cc87ff443684f71244899faa54b34e52aa0d3b952428f811f622a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5368090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15dbf9bbc65c33abb7548e596cb0a737dcc1a0b47baf03fc7e6425a2957a3d7`

```dockerfile
```

-	Layers:
	-	`sha256:c3f7f29ba3e5edc4f87aeb592363439fbe41277afbe13691feec2a13805c0f4d`  
		Last Modified: Wed, 24 Jun 2026 02:09:06 GMT  
		Size: 5.3 MB (5316303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e3bb31d6d0ebae4b444a8f0761255e96a5fca8d9057e08b20ec338538e22b4`  
		Last Modified: Wed, 24 Jun 2026 02:09:05 GMT  
		Size: 51.8 KB (51787 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:972d4f61d624534af03ca1d2d29f36f0d3334a7bff980f70481adc7b751ccbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155177522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c648c6552d1298aeb33f30b1cf4024d024fe14a549b24c9743f9eaf4d978a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:35:04 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:35:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:15 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:35:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:35:20 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:35:20 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:35:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:35:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:35:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:35:24 GMT
ENV PG_MAJOR=18
# Wed, 24 Jun 2026 01:35:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 24 Jun 2026 01:35:24 GMT
ENV PG_VERSION=18.4-1.pgdg12+1
# Wed, 24 Jun 2026 01:35:40 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:35:40 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:35:40 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:35:40 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 24 Jun 2026 01:35:40 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 01:35:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:35:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:35:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:35:40 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:35:40 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:35:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb348413c19e67427fcd336346925138b24cf790349c09ef7fcfb094dfb6c3b6`  
		Last Modified: Wed, 24 Jun 2026 01:35:59 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfb635597b1312d7a2578505842d8c3140b3614383d0aedaf195de3062ea9cd`  
		Last Modified: Wed, 24 Jun 2026 01:35:59 GMT  
		Size: 4.5 MB (4519521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4713e1f8a3b2ab29174fd045ecddbf53a378bd5c9c85809fa6b4f48194e4b7`  
		Last Modified: Wed, 24 Jun 2026 01:35:59 GMT  
		Size: 1.2 MB (1203266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48eac96a88c07b40567eb32c1260bdb970ff3bed58fb25484b6150ca25d5c3f4`  
		Last Modified: Wed, 24 Jun 2026 01:35:59 GMT  
		Size: 8.1 MB (8066468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920742cd3d8c68db5c13695364ca3d18aec6924d79812d7da09dd73059417a98`  
		Last Modified: Wed, 24 Jun 2026 01:36:00 GMT  
		Size: 1.1 MB (1109013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de444ba98e0bee3d19802e77d7bf1c4acda8c21dddc943ff3700faafaf28d27`  
		Last Modified: Wed, 24 Jun 2026 01:36:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e70e7c27a4d9f7e99347929b517ef0618b3029bad1bc03aec789c961fc282b8`  
		Last Modified: Wed, 24 Jun 2026 01:36:01 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bc1624e78fa7ae724db25c84ed19bf61fdc73f3e0df5489287a46097923dd5`  
		Last Modified: Wed, 24 Jun 2026 01:36:04 GMT  
		Size: 112.1 MB (112126780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8128c21010eb11881e83b7da28a822899a189423a7e85e9cfd5d16013f152da`  
		Last Modified: Wed, 24 Jun 2026 01:36:02 GMT  
		Size: 19.2 KB (19227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdfed40ef4fbd1510ce46179a9f14dc106c8ee98ab09849b7476c2b32f2b034`  
		Last Modified: Wed, 24 Jun 2026 01:36:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6185757aca524e3628e2050161e28671b103484a04269045897b3f70a89f6577`  
		Last Modified: Wed, 24 Jun 2026 01:36:02 GMT  
		Size: 6.1 KB (6094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a80b936b2ff939c672a2b9d46f077e41d7e9354ea3ce3d9f9a0c74918d6c2`  
		Last Modified: Wed, 24 Jun 2026 01:36:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:217b4d46c9ce2d0d891007ca606cf31a1a8a6a968797b1b2218ea327e38c30d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6214690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2049e091e37a8ba57a1b93263993820c77fb205e60891a72b233821b94f193`

```dockerfile
```

-	Layers:
	-	`sha256:17041d56347bfc0c568a3574b8fa6b4cd35fe0ebd3a0b248f22d5b78f19d5f6e`  
		Last Modified: Wed, 24 Jun 2026 01:35:59 GMT  
		Size: 6.2 MB (6162858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:157ea184414092706ebc4a5b9f59a0cb8cc2510feee59b522c8977e8d15b88c7`  
		Last Modified: Wed, 24 Jun 2026 01:35:59 GMT  
		Size: 51.8 KB (51832 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; 386

```console
$ docker pull postgres@sha256:7bb4295f32171ce12afc6da2a5caec33271f0993ddf1cfebe9acf75a89b4e58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94049391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62c3234f812d80848145a2cc7dfbcf7493a77a033382e94c0fe75e4c36edeba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:30:49 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:30:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:30:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:30:59 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:31:03 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:31:03 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:31:06 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:31:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:31:07 GMT
ENV PG_MAJOR=18
# Wed, 24 Jun 2026 01:31:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 24 Jun 2026 01:31:07 GMT
ENV PG_VERSION=18.4-1.pgdg12+1
# Wed, 24 Jun 2026 01:39:21 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:39:21 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:39:21 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:39:21 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 24 Jun 2026 01:39:21 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 01:39:21 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:39:21 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:39:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:39:21 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:39:21 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:39:21 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:df519b11ac99d8e2d452cbd55f824e658d0b86f649745abaaf8cbe33e2736a30`  
		Last Modified: Wed, 24 Jun 2026 00:28:03 GMT  
		Size: 29.2 MB (29225809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f63abe53075e6fd2d038c0bba552b7a472807a2f959f64edd3c7bf29b2daf68`  
		Last Modified: Wed, 24 Jun 2026 01:39:33 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b2b1ca2bc156d6c55b559249f05d75c74e0fd0c8ec9c1ebe977a53c2d8911e`  
		Last Modified: Wed, 24 Jun 2026 01:39:33 GMT  
		Size: 5.0 MB (4966078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37410cc81db902beb500527ef3f053cc5aa97092a7c3d6cd332ad814ab90be41`  
		Last Modified: Wed, 24 Jun 2026 01:39:33 GMT  
		Size: 1.2 MB (1218614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f66605aeb1c42699330b7419bd1f5d2db6e3e398efdb9459d8f70f198d1abb4`  
		Last Modified: Wed, 24 Jun 2026 01:39:33 GMT  
		Size: 8.1 MB (8066437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec02c116aaabced066b0a6e6d5ae2d64f24b74a8704674aab0481da7c662b4ac`  
		Last Modified: Wed, 24 Jun 2026 01:39:34 GMT  
		Size: 1.1 MB (1137464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27155b206794c0ed6cbca6f5d7a7761b488c7bfc36ff5fc37f63919d0ae1b7c4`  
		Last Modified: Wed, 24 Jun 2026 01:39:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f41a5c4c5b25a5b82c01e80df45f2bbbbee506538fdac811f77b297d34de56b`  
		Last Modified: Wed, 24 Jun 2026 01:39:34 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c268b20aabdfa7b6093ab73d01fbaad3763a2fadabc39a6d00cce0343850d0d7`  
		Last Modified: Wed, 24 Jun 2026 01:39:36 GMT  
		Size: 49.4 MB (49404921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383b072398d9e380128166b29772e0927b6726cdd8e809d189d2c7bf9b1e9869`  
		Last Modified: Wed, 24 Jun 2026 01:39:35 GMT  
		Size: 19.2 KB (19229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b508fe493ca8075d27e2ad59653a28389db1d1bf69ae4ceb286e69c85ed6fa39`  
		Last Modified: Wed, 24 Jun 2026 01:39:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf08341f10e277d28d259d96f32706695a9ae762151fe51fe58874fe74a21a9`  
		Last Modified: Wed, 24 Jun 2026 01:39:35 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601d09cd9ff79de01204ef86912957d1533124f74b8ed5a59879d67fa33e594c`  
		Last Modified: Wed, 24 Jun 2026 01:39:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:410d8ba2cdbfef267c659e5be986415dbdf1e654cb0cae9b982004ccce2bfe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acaeaae2c091563e344c941e20d47988d888f92495c9b8d67236fe9604617132`

```dockerfile
```

-	Layers:
	-	`sha256:c56a8ecc990626c4acb6e18bfc411804ebfa7fc7151e7947b99e7a370b3b3e2c`  
		Last Modified: Wed, 24 Jun 2026 01:39:33 GMT  
		Size: 5.3 MB (5311618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c83df1f73ef89a1f8b932eb2f91ccdb42552478be212a89cc4c8f4c06bae73`  
		Last Modified: Wed, 24 Jun 2026 01:39:33 GMT  
		Size: 51.5 KB (51538 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:9dc09d73566199a2e39825f56b3258082b8a9e4fdee37491410ba29a129ad5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156046671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e9ce806812229d281f2a5cd2c930156d6368b7c44ae3bfdbd8fbcb585bd112`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:00:00 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 09:00:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 09:01:14 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 09:01:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 09:01:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 09:01:42 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 09:02:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 09:02:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 09:02:07 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 09:02:07 GMT
ENV PG_MAJOR=18
# Thu, 11 Jun 2026 09:02:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Thu, 11 Jun 2026 09:02:07 GMT
ENV PG_VERSION=18.4-1.pgdg12+1
# Thu, 11 Jun 2026 11:37:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 11:37:31 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 11:37:33 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 11:37:33 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Thu, 11 Jun 2026 11:37:33 GMT
VOLUME [/var/lib/postgresql]
# Thu, 11 Jun 2026 11:37:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 11:37:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 11:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 11:37:36 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 11:37:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 11:37:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:879bfe7978458b45ee339ecbde9dc371ed3cfa3f270b4e7b489be70df0161f68`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 28.5 MB (28528814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940ca48530c93bf9d9103fdb7fe687bd5da05646fcc94f0b258e4f3d909b9884`  
		Last Modified: Thu, 11 Jun 2026 10:21:29 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e321114937eba67d8436d805683b2b1215aa653ee449f00f00d17f2620133df5`  
		Last Modified: Thu, 11 Jun 2026 10:21:30 GMT  
		Size: 4.5 MB (4475226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59208d2083c48f6fe780155d8a17d62952eefee530f3e60b31b95e55405e6fe8`  
		Last Modified: Thu, 11 Jun 2026 10:21:29 GMT  
		Size: 1.2 MB (1159239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c443ecfdebe639eb98b3031ca7874a9be9a7fcc89bc6f5ac7572ab43286a1dd`  
		Last Modified: Thu, 11 Jun 2026 10:21:30 GMT  
		Size: 8.1 MB (8066644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c1ab6e6a8c9225dba664a86b661d27724e45c4e5ed73ade3a0e38ddce68f61`  
		Last Modified: Thu, 11 Jun 2026 10:21:30 GMT  
		Size: 1.2 MB (1182940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daab5e73663878ca55a35351214f19b34b7d1d0b8245b998d7f408fca642cbd`  
		Last Modified: Thu, 11 Jun 2026 10:21:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9448e9da0c1a4d5196a588ab8a3b60780804af37b016fd79b2c0fb6235d46a6`  
		Last Modified: Thu, 11 Jun 2026 10:21:31 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb9d1b98f43e4dab6a67117c3fcbfb24697ba7720f6ce81178038c494d109ee`  
		Last Modified: Thu, 11 Jun 2026 11:39:54 GMT  
		Size: 112.6 MB (112603738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336c6f181815eeb14db0fcefef2946684362116fdfb4cb6168476ee40bc75abd`  
		Last Modified: Thu, 11 Jun 2026 11:39:42 GMT  
		Size: 19.2 KB (19231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c46b83e99015279202a6fbcce83045dfbbc170873d9e3ceba53dada72c09b7`  
		Last Modified: Thu, 11 Jun 2026 11:39:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddb830321d12fda2f18d7678f06c520b5d45bdb418ddbd0be884f2252ce82ac`  
		Last Modified: Thu, 11 Jun 2026 11:39:42 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91c75ca8245588df7619639279a606be3b076edcd94e066f060c0e246e01327`  
		Last Modified: Thu, 11 Jun 2026 11:39:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:4f9641ffc6fc061541c7d93789dd3bf3e4bebd6baa8265580e8ae14a71a64c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 KB (51462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677f0b6193acbf3ff78b721427938156a5e58e7f9a7058dff93b8f03ccc7db05`

```dockerfile
```

-	Layers:
	-	`sha256:abbbce574c968b747a62931b4a0a1e100c8cd2bf1dd92b839833f13430febcc3`  
		Last Modified: Thu, 11 Jun 2026 11:39:42 GMT  
		Size: 51.5 KB (51462 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:5c7efc4b701f5aa800741c73dd89771eb87a136aa37456dca08cd9bc7f62b86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170080880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ef7282fe219c5f59a477208c2a9373b82628f50d296f2ea7af40d43e5cd7cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:05:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 03:05:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:05:27 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:05:36 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 03:05:36 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 03:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:05:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 03:05:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 03:05:46 GMT
ENV PG_MAJOR=18
# Wed, 24 Jun 2026 03:05:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 24 Jun 2026 03:05:46 GMT
ENV PG_VERSION=18.4-1.pgdg12+1
# Wed, 24 Jun 2026 03:07:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 03:07:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 03:07:58 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 03:07:58 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 24 Jun 2026 03:07:58 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 03:07:58 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:07:58 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 03:07:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:07:58 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 03:07:58 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 03:07:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:aca68162e30a6a797424ddae2250996b638d7dd3b09085b7da2b627f63083af5`  
		Last Modified: Wed, 24 Jun 2026 00:27:33 GMT  
		Size: 32.1 MB (32081978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e642caebe44c6d1baa20259cf0595d274a5e88fd90ebe8c357738a030195d6`  
		Last Modified: Wed, 24 Jun 2026 03:07:06 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dd4e8a754f640d4c9b2e2f8c5f7388eeacd17c79552c564653bd8068f47604`  
		Last Modified: Wed, 24 Jun 2026 03:07:06 GMT  
		Size: 5.4 MB (5368595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5aa40b3a2880a5b5f3b32d689358b6f65bcf0a619d4ed3e8c9ae1c1a0b1a21b`  
		Last Modified: Wed, 24 Jun 2026 03:07:06 GMT  
		Size: 1.2 MB (1208168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711844b58f07dccf8131212563d554b022326f3a2d2cb4ce8afae9d1f1ce3275`  
		Last Modified: Wed, 24 Jun 2026 03:07:06 GMT  
		Size: 8.1 MB (8066503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131f5a261c60856ea1234bfc1e0823be1145e989a2428daecc78912cefe9afe0`  
		Last Modified: Wed, 24 Jun 2026 03:07:07 GMT  
		Size: 1.3 MB (1283621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c53140dc5281cf5b3a6815387761b2d96e5ac059a86a4bd923e7e37f4741f7`  
		Last Modified: Wed, 24 Jun 2026 03:07:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45099e3263bb77cb32749129b702695c7b62c197a821d7a84b14d9a48bdfaf7b`  
		Last Modified: Wed, 24 Jun 2026 03:07:07 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055d34036eb5c74b6f76b44f88922ffcdbf14c92d8f7662ad170c9f64d7ff27f`  
		Last Modified: Wed, 24 Jun 2026 03:08:40 GMT  
		Size: 122.0 MB (122041940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950f2882cde6c4cb9bda59fce8ba97f0b2fce8fb11401ca94f834651cd60bc40`  
		Last Modified: Wed, 24 Jun 2026 03:08:37 GMT  
		Size: 19.2 KB (19234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bb6d28961617cd016fc670f30218392ba2024f3dfca8e4d148a750724faeef`  
		Last Modified: Wed, 24 Jun 2026 03:08:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6c838a1251c8d7845728449e5e71b12ea15541ef2b8116f64a992dc33518c3`  
		Last Modified: Wed, 24 Jun 2026 03:08:37 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c3f19bfa0d6e386babe49561d3d7f7999d5dfdb9df2610d00b1383cddce299`  
		Last Modified: Wed, 24 Jun 2026 03:08:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:db836295ff1825708b65c505b1482b93524daf95a9a88cae00d78badce4db234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a398001e67276ae825c7e32c4181a2b22767b03ba104b4c73eadd3536207bf`

```dockerfile
```

-	Layers:
	-	`sha256:5a25c1b9a4b3135389d4d8c07408f4ddeccc4ddb5b16c112ebdaa4815445e736`  
		Last Modified: Wed, 24 Jun 2026 03:08:38 GMT  
		Size: 6.2 MB (6163918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d782fc953d5846f9bd1aa56bdd263f6726425e701abbc9928be3831784d2f20c`  
		Last Modified: Wed, 24 Jun 2026 03:08:37 GMT  
		Size: 51.6 KB (51647 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:9a04d513b1805102ebd96f8cec2ec5b194fcc81782883c9745cf72c41f04fc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166499493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20da289654a735b2e8219f25eb79d0ee0ae14e167d560b18beb273502920b1bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:02:01 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 02:02:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:12 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:02:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:02:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 02:02:16 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 02:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 02:02:20 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 02:02:20 GMT
ENV PG_MAJOR=18
# Wed, 24 Jun 2026 02:02:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/18/bin
# Wed, 24 Jun 2026 02:02:20 GMT
ENV PG_VERSION=18.4-1.pgdg12+1
# Wed, 24 Jun 2026 02:15:52 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 	if apt-get install -s "postgresql-$PG_MAJOR-jit" > /dev/null 2>&1; then 		apt-get install -y --no-install-recommends "postgresql-$PG_MAJOR-jit=$PG_VERSION"; 	fi; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 02:15:52 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 02:15:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 02:15:52 GMT
ENV PGDATA=/var/lib/postgresql/18/docker
# Wed, 24 Jun 2026 02:15:52 GMT
VOLUME [/var/lib/postgresql]
# Wed, 24 Jun 2026 02:15:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:15:52 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 02:15:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:15:52 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 02:15:52 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 02:15:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35a8d0facb58767607cd7a923fb4ec97e7a0198d64e6fd44b33a67876107cdd`  
		Last Modified: Wed, 24 Jun 2026 02:16:23 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5813aba06bea57dcd027971022665d5461513a86b1097aaac1f9274285ded84`  
		Last Modified: Wed, 24 Jun 2026 02:16:24 GMT  
		Size: 4.4 MB (4391230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2eea54b388939097edb4705b5eb99ab3af069538576543cb2e6280e9315587`  
		Last Modified: Wed, 24 Jun 2026 02:16:23 GMT  
		Size: 1.2 MB (1222878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c00f59b6975020a02b5537a82ceda825e2f2c4b6a59c53586731a61e4ce3fb`  
		Last Modified: Wed, 24 Jun 2026 02:16:23 GMT  
		Size: 8.1 MB (8120785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a7da455fe113508cce23529fd8dc1e538645d81be0edb3d0878c67de2bb9f5`  
		Last Modified: Wed, 24 Jun 2026 02:16:24 GMT  
		Size: 1.1 MB (1097095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126521e6fcad067e8f942b1ec27cbb5053d105ef2dfbb84535da55ad51df0ff`  
		Last Modified: Wed, 24 Jun 2026 02:16:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57325788e39b93d8f9295c5dbc83d8d04ac1be46cbf8640cc977e317e25dcda7`  
		Last Modified: Wed, 24 Jun 2026 02:16:25 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a19735bd8d5519f62e45b335c951ea316e9a2c53b37940200e210ec0e796a0e`  
		Last Modified: Wed, 24 Jun 2026 02:16:27 GMT  
		Size: 124.7 MB (124743855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b428b5745e587d1e3bd8189918c83976ceb3bf6dd0f2c74ac766d79f323870bb`  
		Last Modified: Wed, 24 Jun 2026 02:16:26 GMT  
		Size: 19.2 KB (19229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8de89550ab867de4bb476fbc36d8bef5d2e86ef3c13e05910151786396dc6b`  
		Last Modified: Wed, 24 Jun 2026 02:16:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cc46b65ef4da52f62edb0526e9aa51fcb60794101df130515f8b2f04022b96`  
		Last Modified: Wed, 24 Jun 2026 02:16:26 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b710424028e7626798d48300a76231ff0e3f04fc93c4c60b327ef52cacbbd5`  
		Last Modified: Wed, 24 Jun 2026 02:16:27 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:752c6ef7dff58214f040146b84de960c6d1b41a1a14145a9276aa2623cbb67f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bd6fd5796be67a34e35708d08d0fb6a4bb92e34a4c9f351f559ae2c762ac48`

```dockerfile
```

-	Layers:
	-	`sha256:30f05cc28294a03806c04efb2c5685e324601d723b8435a121ea2f66bbcfa663`  
		Last Modified: Wed, 24 Jun 2026 02:16:23 GMT  
		Size: 6.2 MB (6171191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6c339f50074afb8ea0311c647a1677410a8dae80ce65b74fb35cdd1a36bff3`  
		Last Modified: Wed, 24 Jun 2026 02:16:23 GMT  
		Size: 51.6 KB (51590 bytes)  
		MIME: application/vnd.in-toto+json
