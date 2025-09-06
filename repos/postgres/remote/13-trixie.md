## `postgres:13-trixie`

```console
$ docker pull postgres@sha256:e600619222c99cee43933b27f56d27466b7fb8d2964a34cddcca02fdbb33086b
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

### `postgres:13-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:4042951ba4e905fe8119b9946d2d3733f664ffd647c0931d3663cb246f716e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156104146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9aca525616c32b5159b31d66575df83000ed131cd11db5316302ec0ba29ef4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
ENV PG_MAJOR=13
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=13.22-1.pgdg13+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbafe659a8788e729489ab8a6c500d460ce878826b321bfc7e25bb3cf9494d82`  
		Last Modified: Fri, 05 Sep 2025 21:47:50 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fe18e6fc9440339b2c9a7a3519d279403f07da5a009eb2a018904b8315d328`  
		Last Modified: Fri, 05 Sep 2025 21:47:54 GMT  
		Size: 6.4 MB (6436531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa1ce068802be387780370549dcaa2d105a7a0a35a9faad5a4bf6554e8bae03`  
		Last Modified: Fri, 05 Sep 2025 21:47:56 GMT  
		Size: 1.5 MB (1454191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b4c9205dc8077541018ffd1dad59d1e2b7ecdc570d1452c479d3a2576c788e`  
		Last Modified: Fri, 05 Sep 2025 21:47:59 GMT  
		Size: 8.2 MB (8203596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ed0723551975c9b1b7c9f78caad7e9b9ddcd84a3a968545ed16c78a4af78c6`  
		Last Modified: Fri, 05 Sep 2025 21:47:58 GMT  
		Size: 1.3 MB (1311349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f843814ada0c654f7362e3822601f2a413932b2bec3e380e69a7a2a5342e1ea6`  
		Last Modified: Fri, 05 Sep 2025 21:47:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d1d5b021b5e7b5097c4a81b5d01e179d2aa887a0c37fcbd9a4042efbb1c3b2`  
		Last Modified: Fri, 05 Sep 2025 21:47:59 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a21b07ee2ee27dc459041cf3033f6677ace815ffdea83ca7a2d2b76caf5db11`  
		Last Modified: Fri, 05 Sep 2025 21:48:13 GMT  
		Size: 108.9 MB (108904907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32ddc7aaf584fe27bbec6a317df5df8342983bef2109923c7f3d07c96dac517`  
		Last Modified: Fri, 05 Sep 2025 21:48:01 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d95d519512cd8806a6d14e75a9a427536facf93ddbfd89d0715e621eeff4e6`  
		Last Modified: Fri, 05 Sep 2025 21:48:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91694a92aab6371f97413fe9f78709b1fece2f192926a85add4518fdca5b4571`  
		Last Modified: Fri, 05 Sep 2025 21:47:45 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7c8847687dd1c330383fa51166f80bc40a81eb06bf27dbdb5bc4fe9f170c3d`  
		Last Modified: Fri, 05 Sep 2025 21:47:45 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7a908a53bfc1153574b67813f71c467b899b383940562271c6def93f54f2a7`  
		Last Modified: Fri, 05 Sep 2025 21:47:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:255433c91d1dde04797c2d885779df7c47fb9754d4dce3e4ab48e520e248d01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5687463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142bde6b5d48cff2a8c9acd5414ba9c5142a435a88b76e1d254c482f9f6534ae`

```dockerfile
```

-	Layers:
	-	`sha256:6ca225a67855f15747c083f81633fe1e785a028aee0ecac32e3a66b3a1b8b1b1`  
		Last Modified: Fri, 05 Sep 2025 23:07:31 GMT  
		Size: 5.6 MB (5633168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b73ed5c7cd9a309f5f8ad76d91f670b2dafea435767bd5256536ee9e72c38cf`  
		Last Modified: Fri, 05 Sep 2025 23:07:32 GMT  
		Size: 54.3 KB (54295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:d1a467665943f6aa07218c6a1c23044c63b430b0e2994f7d0e923cc12e658dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150175024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef1ac54c7e551f5e6c12d0edbd712d72ddba5b17aaad91f41b508ae69a48167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
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
ENV PG_MAJOR=13
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=13.22-1.pgdg13+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02cfb0f45153e3eb1ad467de056ad856b1312c3c2cc7a2e1399fb7e6275928a`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d2e5de6e56786bb5224c771d5c45f60afd7b3c4236149576e57ca3cd517da5`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 5.9 MB (5928857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a508c65596df72509e51857412bf4f016253866945dd3338c74afaad80e22c2f`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 1.4 MB (1431813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24af1b0569549451d483e7faec8f4b0abfc0593b470b3fc302e46be753804c0b`  
		Last Modified: Fri, 05 Sep 2025 22:17:45 GMT  
		Size: 8.2 MB (8203926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4beb74480c405e8088e518e4e5c355a526a53d5fa873acdb412d4f2b6d2432`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 1.3 MB (1317041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7a4b2ce275c0857c4c7136e725e7abed09476ec5df2ded8578181e25adf1f9`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc36c440a88345ce7cba828f3cde6bb6b68fe85cf530cbcef5cf5ccabe28095`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44c9b86999c4a0bf6b1959b9dbd6b1ff875b7f719165a517a99bbf44c7b4ef8`  
		Last Modified: Fri, 05 Sep 2025 22:17:51 GMT  
		Size: 105.3 MB (105331406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cd5ef9b3b17e22d479b3daec3461197622c5c9e113da62b5d6a6a64a7f0690`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9970d217e08e56877ff65ac1ca7799f2af07899d94cd49174a599c7151f26717`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a313533487f64fd5414c5a2094722aa27e61b52b153f91831d185a980f1fe96a`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71371a37694fd67eab265d41baa26ba1bdc9f3b04b15b682c14ece0e53b9d36`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b1e2229aee7e50a5b7751da345e2f1cf3e4480f66c52ca2a3f3159643343b2`  
		Last Modified: Fri, 05 Sep 2025 22:17:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:c626c21b75308f625605ebffa1a57ea5303fffe8bcc0ef100408ba8300bae16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5704292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a8728936292984d4426a757231802c969264e7c18f378280333dfcb33d20`

```dockerfile
```

-	Layers:
	-	`sha256:b8e017de61a564e2de462bd064e61afc84d330034832c5096556e72f50ae285b`  
		Last Modified: Fri, 05 Sep 2025 23:07:38 GMT  
		Size: 5.6 MB (5649774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1527369859b42c70dea78dd35a01ac06017ddff9507b9d7529b2367cec7fb14`  
		Last Modified: Fri, 05 Sep 2025 23:07:39 GMT  
		Size: 54.5 KB (54518 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:48cc5851619ec4d9e02ccb7c6910ad7102578ffbefcf5df548efb10e47bbbba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145321456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41719403a79bc0bef189328f368f32ebc7ab674c2dbea546bc8d37acb6244fb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22-1.pgdg13+1
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e177436960330c1003ca564bd12601a903395d0b0cbceb49906e76bb133bf9`  
		Last Modified: Wed, 13 Aug 2025 05:36:39 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881281975ed655f87d3850a9c5ffc603c4c28a60acdb55a90978d19ac3895cd4`  
		Last Modified: Wed, 13 Aug 2025 07:37:21 GMT  
		Size: 5.5 MB (5496723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44faa96ea4758b9d6990cb2d217216e0e259882f4e3d258a5f588b4ee3ecde0c`  
		Last Modified: Wed, 13 Aug 2025 05:36:43 GMT  
		Size: 1.4 MB (1421079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30ff06bfe1035684b16f4733453eed17aea6cb49af31f0215ccdb27a2f0df5b`  
		Last Modified: Wed, 13 Aug 2025 07:37:23 GMT  
		Size: 8.2 MB (8203738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc86471180219dce5a3290d91742b99996e732b743b368fb29bf7613c6ea0d02`  
		Last Modified: Wed, 13 Aug 2025 05:36:50 GMT  
		Size: 1.2 MB (1172344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a91e68d4e8d7ceae6ee126ed6a8c666d3fc98f2fcd5e7a4f54c97683917aa23`  
		Last Modified: Wed, 13 Aug 2025 05:36:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142085f25724adf875ea5aff59337bd6ba553b165dff76316376b3e5fa05d93b`  
		Last Modified: Wed, 13 Aug 2025 05:36:57 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1394dce1a186710f5283e10bc19bca55c90375482a7a2ff5e5d6f0727bb2c4`  
		Last Modified: Thu, 14 Aug 2025 21:25:51 GMT  
		Size: 102.8 MB (102799798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4414d71149fd83ffd88b839ff9f1df2bafae8bfdcfe75de51212e7121c2b30c4`  
		Last Modified: Thu, 14 Aug 2025 21:25:33 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7d3083dacb2eb4f139dc5cf61dc52bdac578ce48d9742f4af68d6b8c7320dd`  
		Last Modified: Thu, 14 Aug 2025 21:25:33 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d4e9655817d92a4a948b20567e55c23161b496f42d9680875bf148cb303152`  
		Last Modified: Thu, 14 Aug 2025 21:25:33 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a75ede5e51c4f57534043a90c0ee621792e3041ede14d58c1de526ece7a3c54`  
		Last Modified: Thu, 14 Aug 2025 21:25:33 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6058cb3ba69b1a401682d1037295fc5be7467b22f6cc19351576cac28aab625d`  
		Last Modified: Thu, 14 Aug 2025 21:25:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ef2dddb84fcf5d9cd4c6db4f51ee41334fc63f4a3842054f941495ad3c590ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b0b8fdb6f04b2a540da2012d04fac4ca169237d5a6c15df7411a98a3dc38d`

```dockerfile
```

-	Layers:
	-	`sha256:691db00cd418cfb194404923b0e8b460e2ada7f039f4ab0a00eef00b84d0c880`  
		Last Modified: Thu, 14 Aug 2025 23:08:06 GMT  
		Size: 5.6 MB (5649033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e122b911d15fa1d02d4d9e4565394f04136b9699dab5be9c46dfa92c7c7a25a0`  
		Last Modified: Thu, 14 Aug 2025 23:08:06 GMT  
		Size: 54.5 KB (54515 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0c0bdfec0b6a42b3a5094817ba04636b5aeaf929dde4a37d02c4bd1100a2d99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154726029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5864fd701a6c15c30a022ab16d0592c26522f33ee55cfb7dcfa41a62f68c669b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22-1.pgdg13+1
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7098fadfc7263d599e9af91cf79815094f50dc3cc507ade0066d04ad3c726ca`  
		Last Modified: Thu, 14 Aug 2025 18:50:02 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dffe450d7574d241fa48f7ff718c644e3321fd4302af3609a0c8ba64954b09`  
		Last Modified: Thu, 14 Aug 2025 18:50:04 GMT  
		Size: 6.2 MB (6231933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4db2875216f60ed11db0b51dfb0a8c245d707616c1fee2d5be3e7f4f57d7d7`  
		Last Modified: Thu, 14 Aug 2025 18:50:03 GMT  
		Size: 1.4 MB (1386103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc89b2d2c7ebd971d89d938c54a70f717c9fc7a490e68ac21907a55cb0bef1e3`  
		Last Modified: Thu, 14 Aug 2025 18:50:06 GMT  
		Size: 8.2 MB (8203710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94585c28ed89799a31e0ce000be0468632483f98c7bcb0a753b18b3ea98d3244`  
		Last Modified: Thu, 14 Aug 2025 18:50:03 GMT  
		Size: 1.2 MB (1220343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237ff033285bc1aa8935f4969aa89ecab2ebbd9a33046714e4a64a67a8475df9`  
		Last Modified: Thu, 14 Aug 2025 18:50:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd40904509c4302fd6377d5f113d3a63b7856101000b8f3c14e7e5f70d9a8f4`  
		Last Modified: Thu, 14 Aug 2025 18:50:03 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40afee5dffe1cee08baa82f329d0f01bfa6c3a631fe6014f9549d7d711e6fbd1`  
		Last Modified: Thu, 14 Aug 2025 19:28:14 GMT  
		Size: 107.5 MB (107527615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989577c4100b76eef052be1d5373ff441e361e3b69a0a1dd6404b66b8447243`  
		Last Modified: Thu, 14 Aug 2025 19:28:03 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f83189d38bb82af1781317cd8818dd413b2d946d29c23ab348cc0b2749d220`  
		Last Modified: Thu, 14 Aug 2025 19:28:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2d469b3e9f9cc47b6ecc9e8f9f41b28ca5449bf343cd626a62dcfba0d78f5b`  
		Last Modified: Thu, 14 Aug 2025 19:28:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077997d92555a4494523985b9c4dfeff2bff0071e1ef1691e53cb8a8419dd2fa`  
		Last Modified: Thu, 14 Aug 2025 19:28:03 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c12af6be9fd318be3bf3ee1bafdb034795e8fbc57b634c0171bd88b1a2d9e`  
		Last Modified: Thu, 14 Aug 2025 19:28:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:a6552a7b96eeb89f9b1a2b763bb4db38c37a6b6cdbdaad937e38646d5ad0f963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5694030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4623729369530f83b8e4254b0cac20367250a5dde17d96fe4c23481e63382c01`

```dockerfile
```

-	Layers:
	-	`sha256:e7cd1d9504b67ac4318467d46e7f1f2d01b28cb3cdf2b97d3cfd62fcf26762d6`  
		Last Modified: Thu, 14 Aug 2025 20:13:31 GMT  
		Size: 5.6 MB (5639464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd58623599d2a96f04020ad8dd3befb9067a4847e0c0e36bf3cbd10f248bd8a`  
		Last Modified: Thu, 14 Aug 2025 20:13:32 GMT  
		Size: 54.6 KB (54566 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-trixie` - linux; 386

```console
$ docker pull postgres@sha256:120235dd91a3641be5c78820e041db9cf3ec4677b5d7b3848a261f247d6d922c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165219080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60312c5ca00df5d515cbf1feeb8ee918fba2e5760b3875c589a90075058edcaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
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
ENV PG_MAJOR=13
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Wed, 03 Sep 2025 21:48:27 GMT
ENV PG_VERSION=13.22-1.pgdg13+1
# Wed, 03 Sep 2025 21:48:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
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
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c2a9181cfd26ca0861a859aaa69920d58707f2a1ba3bc7e2876fdacca9cd09`  
		Last Modified: Fri, 05 Sep 2025 21:46:45 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a7bd114a0fd4b539f8c5a427dc8704f7d352e355bd8b16dcff711b44cd67de`  
		Last Modified: Fri, 05 Sep 2025 21:58:17 GMT  
		Size: 6.6 MB (6629438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a65145bc6c71704c9f00f78d1470b0d60979ab8bcd5d31cccc41f25b0cc6f2`  
		Last Modified: Fri, 05 Sep 2025 21:58:16 GMT  
		Size: 1.4 MB (1429231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7e509f65d491d58de436933fa27c6f222d25da100074f8297b943eef0d886b`  
		Last Modified: Fri, 05 Sep 2025 21:58:17 GMT  
		Size: 8.2 MB (8203746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba8b08e189a7b4f43695ff2430f43eeac6317749e4f8c2eaf5933adf96d5b11`  
		Last Modified: Fri, 05 Sep 2025 21:58:17 GMT  
		Size: 1.3 MB (1308044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc572277ae0f9bafc101f590bbf6baaaf796f37fb8a792e7e76acb33f3e9f891`  
		Last Modified: Fri, 05 Sep 2025 21:58:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2681e5743dd57ed7b17b7c9211989a3ec628d1390b495adae0f5604da4b525`  
		Last Modified: Fri, 05 Sep 2025 21:46:51 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f9aad2dfe69620202effd17ec9b5d3d984d874a28d26d7fe3a69cdf0491b0a`  
		Last Modified: Fri, 05 Sep 2025 21:58:24 GMT  
		Size: 116.3 MB (116338957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27fe368535971c96e691d3177a79a0285711c3afddc0a7570b962a736b53d9c`  
		Last Modified: Fri, 05 Sep 2025 21:58:17 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e72e419cba3498b8591d3ff07749d77bd927be3696c130eee136fb337d38d`  
		Last Modified: Fri, 05 Sep 2025 21:58:16 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b174b14ff8c5414cc80896413893fdf244a6ab89c74343b35e3bb503d1b5a810`  
		Last Modified: Fri, 05 Sep 2025 21:58:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf899ffe96bf1367eaca7c588421dd5b97176407f1a2ea2f5a4eb0da2caa57de`  
		Last Modified: Fri, 05 Sep 2025 21:58:16 GMT  
		Size: 5.9 KB (5930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21f2596b72bda011b903ba4c4d2c9962cbda1523c32e8ef74697d8b55e386ee`  
		Last Modified: Fri, 05 Sep 2025 21:58:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:c581d6a46c85e853c1600c8bd99126f1785167c121475a19d43b1cd435032804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5702897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92139e615218afd8944bb25466d9783c7696993c0b592a9007c7410eb90fa2d2`

```dockerfile
```

-	Layers:
	-	`sha256:ad75d26507c8e4db18d4360564bcbe814a599af8dc5c2f5d2a332c97e72aa31b`  
		Last Modified: Fri, 05 Sep 2025 23:07:54 GMT  
		Size: 5.6 MB (5648655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f67bba17918d2253530d72eefc020b2584d56a33a08d924c0bb78a2de2fa9afa`  
		Last Modified: Fri, 05 Sep 2025 23:07:57 GMT  
		Size: 54.2 KB (54242 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:f5b1a807e925b1f0f5a2b3c46cde17810690e37f85a9aed198cd399c7c2f9a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168148550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690eb297f98628bcc7d7f0c7c566f9c831e1d36b6f29a133c89664bdf9e0f879`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22-1.pgdg13+1
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c84463a4e245bf480d1082fe107962d670170ad3ce4ceeb441eb1b8c1894de`  
		Last Modified: Wed, 13 Aug 2025 11:18:34 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab48c672011c47270df0eb9f0fe011c1b11f0f782ddd50fb47509877407eb692`  
		Last Modified: Wed, 13 Aug 2025 11:18:36 GMT  
		Size: 7.1 MB (7075804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584d3214f5520c6f324f729a7d22dc2da1d81fc79af946f19813211f6706f4b7`  
		Last Modified: Wed, 13 Aug 2025 11:18:36 GMT  
		Size: 1.4 MB (1375564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff07dd4e6093aa581bdc2a1d6498f992ffdd0a248c804aa83f4fd205de2e3eed`  
		Last Modified: Wed, 13 Aug 2025 11:18:31 GMT  
		Size: 8.2 MB (8203709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cf24a16b677bfe7b89b4f58449d622a0221b8096fb28ebcb30c3343a51a74f`  
		Last Modified: Wed, 13 Aug 2025 11:18:31 GMT  
		Size: 1.4 MB (1394663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfa5401d8ceef0f3dcc79af5565483fa1c14718a1c6174e89bce76e6bbc7d93`  
		Last Modified: Wed, 13 Aug 2025 11:18:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d071cb6d31991a1b46f9171cb924c00e562156ccffce21e0f904688a6c11a26`  
		Last Modified: Wed, 13 Aug 2025 11:18:31 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a8d3fc282f21b25051988e332709e59e0e53162b0b01cb103c42620b33c212`  
		Last Modified: Thu, 14 Aug 2025 19:57:41 GMT  
		Size: 116.5 MB (116484322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9213f3a170784a8a3eae80a245ca7a8749929fe96b5008ec85b35106da73b2`  
		Last Modified: Thu, 14 Aug 2025 19:57:34 GMT  
		Size: 9.4 KB (9440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7889af308c7acb408e143b7a60fde0ffeceead7c0c4ce154019e862eda0fbfe2`  
		Last Modified: Thu, 14 Aug 2025 19:57:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ddc8e631927d3dacc330c14093bb8c39920e4d715896328fdf667b071e5b42`  
		Last Modified: Thu, 14 Aug 2025 19:57:34 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291bea771e4713d65434641ee9a11924387bff890b4e3add93f0b7769e678102`  
		Last Modified: Thu, 14 Aug 2025 19:57:34 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f548f3b1b8ef65f7151b01ceeae3740dc232a3a791f1b19a5ff258997b9eb47`  
		Last Modified: Thu, 14 Aug 2025 19:57:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:2c65543d70ad441ac3348cedeb6ce8bdd82af68582e768b8694247b38fed7d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5694110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8266650da3539bad75219a391cdaabd3e70b50e819f195bc1f31e2c956dddcfc`

```dockerfile
```

-	Layers:
	-	`sha256:96091e40a583213b0216bf35e43fa9d3439a1947a82123135899e7edf28676e2`  
		Last Modified: Thu, 14 Aug 2025 20:08:29 GMT  
		Size: 5.6 MB (5639747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd537caf0fb6ca3029591ed970ac989c382acd626f549f3d0a4c1b61b1f89012`  
		Last Modified: Thu, 14 Aug 2025 20:08:30 GMT  
		Size: 54.4 KB (54363 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:13d89da7f4377d0f9882d4fec239c04ee033928e0f127a6949fe8d49d0b2b383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89058392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec5e49ae938d801e4f78f9628ae8b7fec76a67d1d48a198d478627e15e8e6f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22-1.pgdg13+1
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b0a0fa649236068d28b6d885c7775ab23b869ac6db4e99721c07dca1c50ea4`  
		Last Modified: Thu, 14 Aug 2025 06:16:19 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c311e323901b74143f4ee2884d975ecd86ed8fd237bb96964cf2be91acf129`  
		Last Modified: Thu, 14 Aug 2025 06:16:22 GMT  
		Size: 6.3 MB (6291226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1859f38dc7ac3a34086a8ca21cede764ff373b6b790b7ab2455d25147f08f2c0`  
		Last Modified: Thu, 14 Aug 2025 06:16:24 GMT  
		Size: 1.4 MB (1424731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4263087a9cf57f147ffe4441d83c3d579e380f2b9d478856eafc78d9cc3d071d`  
		Last Modified: Thu, 14 Aug 2025 06:16:27 GMT  
		Size: 8.2 MB (8203378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2955bd53e05478f76ceb79d6badbe79f640f15e6c74ce3d8e259997b9b615ed`  
		Last Modified: Thu, 14 Aug 2025 06:16:29 GMT  
		Size: 1.4 MB (1402099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51ed4fe98001ce8f4bb9728bc68f534f9afa7456ad3875b5c3ded0936775b5d`  
		Last Modified: Thu, 14 Aug 2025 06:16:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e6cca965baba9c5eeea11d99ae81468cb3309fdc4e3408aea55d986b94410`  
		Last Modified: Thu, 14 Aug 2025 06:16:33 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e73c96de102c2630b9ad1652e03776be9caaacc08a2b5f6abaf439c2577e8be`  
		Last Modified: Sun, 17 Aug 2025 03:23:58 GMT  
		Size: 43.4 MB (43445043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8428081beeff4988abb4190684ea7979b15202a0e027ce5338a9b3a0fc6a8da2`  
		Last Modified: Sun, 17 Aug 2025 03:23:55 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02eacc1067d5e43191a10ff55b97bfd17bc928dc4b4e93e098305982f71d2015`  
		Last Modified: Sun, 17 Aug 2025 03:23:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d7b1785d4156b506a8a9aecaf068c4f6665379dbe41f430168b0c76d16c23f`  
		Last Modified: Sun, 17 Aug 2025 03:23:55 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a546ac07d1f128241e7550df52142678881c88f9e3082dbcc3090cab215ed9`  
		Last Modified: Sun, 17 Aug 2025 03:23:55 GMT  
		Size: 5.9 KB (5931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aa6f2f59fab460ffc13b7224d26e61dc4d9a8772e83d59bdbd1670ad07da7d`  
		Last Modified: Sun, 17 Aug 2025 03:23:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:2d374941c78a7cbadc01b838b108405c67705562fb19b9f6442547a2e0fc7449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5110651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21508b49adf84e8725c3f9a2b4c79874f114546a9bacca1877f5aa7fab69f148`

```dockerfile
```

-	Layers:
	-	`sha256:b62adab71281c5459df1356ea83b2162a9df189bc8b5261358b3ac7c466cfba8`  
		Last Modified: Sun, 17 Aug 2025 05:07:50 GMT  
		Size: 5.1 MB (5056294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f76c0a47fa2c54b4e3338a5db8349052935dea29bde39e5de0c1fec9e5dd2e13`  
		Last Modified: Sun, 17 Aug 2025 05:07:51 GMT  
		Size: 54.4 KB (54357 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:e12f9bbd37d4ba46845c3d2eecf1ea71ccd9da339aa1f39e6c01ee0b3d3c652c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170577559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5eb6dfb607f163fa16e734a2367a241178af5ca217d3feb4a7a5a5ee97eca9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV GOSU_VERSION=1.17
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV LANG=en_US.utf8
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_MAJOR=13
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PG_VERSION=13.22-1.pgdg13+1
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt/ trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 14 Aug 2025 16:07:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 14 Aug 2025 16:07:16 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 14 Aug 2025 16:07:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 16:07:16 GMT
STOPSIGNAL SIGINT
# Thu, 14 Aug 2025 16:07:16 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 14 Aug 2025 16:07:16 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25aeb0c2b2f8a403705aaa83b95622da6bd82510bb53cdca36e1272cbd0ce1f`  
		Last Modified: Wed, 13 Aug 2025 01:43:34 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accebcf53414b9dbc815739458083b2a6f98a6550be094ea88b262aa973a97c1`  
		Last Modified: Wed, 13 Aug 2025 01:43:37 GMT  
		Size: 6.4 MB (6408735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8013a86d3b1526e8549f316b857c57782e17fbeb29e3cc082c40db534c04c72`  
		Last Modified: Wed, 13 Aug 2025 01:43:35 GMT  
		Size: 1.4 MB (1420337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c121b022a27f99e36f3ec7756fc794d10502feedd80ffe25571261315a321ff`  
		Last Modified: Wed, 13 Aug 2025 01:43:36 GMT  
		Size: 8.3 MB (8258719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ea94d1cb2c41e7377a60b32002839fec6b81f9ac5c0562df38de557467c43c`  
		Last Modified: Wed, 13 Aug 2025 01:43:35 GMT  
		Size: 1.4 MB (1397988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b56b31422bd8bace2d32e04b3b5bb8ee7424c4986ab5775be804b7a6c9dea05`  
		Last Modified: Wed, 13 Aug 2025 01:43:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c798199c95340171b328eea53ffec29853d8de362608bce1809335c565563d`  
		Last Modified: Wed, 13 Aug 2025 01:43:35 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054d45caedba6ba8a4703c995e2de4e9f75eb6307da32a5dea79fc61ef7038d7`  
		Last Modified: Fri, 15 Aug 2025 02:14:22 GMT  
		Size: 123.2 MB (123238449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b0905bc1ba4816132466ba10a416daf12e79fba318e62e79d410bb73f8f5d5`  
		Last Modified: Fri, 15 Aug 2025 02:14:14 GMT  
		Size: 9.4 KB (9443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001215b48f98452289f8f8509c8451bde661051eb509fec7a23fd47217af27c4`  
		Last Modified: Fri, 15 Aug 2025 02:14:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883e6cf6acb3fbf7825a39b9f9e809a11eabb99258b9b535b4cbf07fba272644`  
		Last Modified: Fri, 15 Aug 2025 02:14:13 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588f9085254d90937c2d9eb1d418e658957138907588396e94a58e3f945b2c84`  
		Last Modified: Fri, 15 Aug 2025 02:14:13 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd78a2ffa481bc19aa6d0a58f615526a7f501835c93e69543e128db516c63a7`  
		Last Modified: Fri, 15 Aug 2025 02:14:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:f6ad1063132d83519ea0eabea8bd4a127cdc4c0d5a7d69eef3c29fc55be29eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5704040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f19129def9c38088cc7bbd7795c30a91d93c77ba8e30faa37ff3f556538e5e`

```dockerfile
```

-	Layers:
	-	`sha256:2bb813a77fc6764ae6ae51537e2fb33eba4734f493acc817020e0e5d8a8af9f0`  
		Last Modified: Fri, 15 Aug 2025 05:07:42 GMT  
		Size: 5.6 MB (5649743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf068b2c76fbfd931f6f4aab8ff6bf6ecf0cf87746f843004b86348815253b7`  
		Last Modified: Fri, 15 Aug 2025 05:07:43 GMT  
		Size: 54.3 KB (54297 bytes)  
		MIME: application/vnd.in-toto+json
