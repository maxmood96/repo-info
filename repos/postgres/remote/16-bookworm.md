## `postgres:16-bookworm`

```console
$ docker pull postgres@sha256:89201b84fadb3fad9dd194536de92ed6e08d19c77b1a208793ffb11bf870210f
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

### `postgres:16-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:c808c2f18da5c6342ecec37166706607cdcfdc4be2154d04f29e8f1c1e9aba5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155071654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963ac447204ea971d065418c943c4ee6d56192f32895d4e0d2547dbcf4b40f84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:35:12 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:35:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:35:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:35:30 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:35:30 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:35:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:33 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:35:34 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:35:34 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 00:35:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 00:35:34 GMT
ENV PG_VERSION=16.14-1.pgdg12+1
# Thu, 11 Jun 2026 00:35:48 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:35:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:35:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:35:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:35:48 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:35:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:35:48 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:35:48 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:35:48 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:35:48 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:35:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab24941b0b74e87a4940105f05d6f3d93e6e05da3933087bccd304bd7998cc4`  
		Last Modified: Thu, 11 Jun 2026 00:36:08 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638c12ab4a8182597becb8e0d945ded640c4cd708b1bdaa2df1a21cbe842c188`  
		Last Modified: Thu, 11 Jun 2026 00:36:09 GMT  
		Size: 4.5 MB (4534231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9ecc11200ada822bdd6d5cd5beab5e9f304271553fe64028d97ee3e3a263b2`  
		Last Modified: Thu, 11 Jun 2026 00:36:08 GMT  
		Size: 1.2 MB (1249512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3813a0e6985cf28c023c89b3cafa98c51d0a7ea625e980a795d849f40ed8da`  
		Last Modified: Thu, 11 Jun 2026 00:36:09 GMT  
		Size: 8.1 MB (8066438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc36b2b0ef2b85b77347f4a12dcd004e1147eec1fd44aa488c660d9840156fd`  
		Last Modified: Thu, 11 Jun 2026 00:36:09 GMT  
		Size: 1.2 MB (1196398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24814b050df4173d0c2f44b2465a3a40852aca75612de067db096606f6573e66`  
		Last Modified: Thu, 11 Jun 2026 00:36:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ac54672ccea339e2a6ff220c01cc5116d7710ced49232d166d3b6213e8d978`  
		Last Modified: Thu, 11 Jun 2026 00:36:10 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d88456ddcc3d74cbb337b10f8dd7bc5f322ca4877935b8233a6bfa904cb6b96`  
		Last Modified: Thu, 11 Jun 2026 00:36:13 GMT  
		Size: 111.8 MB (111766487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74123993bbdc8b882c8c12ddc7de4fe8ff1bc872f4f15eb1d05d6f2d6cdfa8c5`  
		Last Modified: Thu, 11 Jun 2026 00:36:11 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f41db9c89e30439e78fa5b2c05c066b4f8aa294a20d5a25dfc0292455b79cd`  
		Last Modified: Thu, 11 Jun 2026 00:36:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf441b540abff0d1a300a53ceffc0898cf7469cbb88315c51fe49acd36143f4`  
		Last Modified: Thu, 11 Jun 2026 00:36:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53240774f08ffa2af60419244e0b231249cb2283fa4f536b7817559f305adf6b`  
		Last Modified: Thu, 11 Jun 2026 00:36:12 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807014ba51b18e57909831b3f3d483e7e1cbc8dd3b80e33caf2dd8307408101`  
		Last Modified: Thu, 11 Jun 2026 00:36:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:de917761efad6d1dcaca541fe3526ac24cba183cc528a09227707b682170524e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5962888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79e8a1ea211c37cebf11fc7966f66cfdc33b0021c8a42f39a3deec6ed94fef7`

```dockerfile
```

-	Layers:
	-	`sha256:85c32b22afe47356423980cee9fe06d85a80308214a5f3944f4aadde270af2de`  
		Last Modified: Thu, 11 Jun 2026 00:36:08 GMT  
		Size: 5.9 MB (5909592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70909632b3781245dc4e63b8d15cf3ed3e7238344440067006397dda78fd1cb5`  
		Last Modified: Thu, 11 Jun 2026 00:36:08 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:17ae5bc2823a3ddb99c37559c499045e91c5b33c0e33c8de16e61f9489ea7c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148090171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9536734ccfa147239cdd834fdbe8942ff79edaf2bf630dd5c8638d262d6f66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:48 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:44:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:05 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:45:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:45:12 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:45:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:45:18 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:18 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 00:45:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 00:45:18 GMT
ENV PG_VERSION=16.14-1.pgdg12+1
# Thu, 11 Jun 2026 01:13:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:13:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:13:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:13:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:13:36 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:13:36 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:13:36 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:13:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:13:36 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:13:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:13:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:99eb1512995af32b91c63bcd418e886af77e3c7ca088226161af558763425461`  
		Last Modified: Wed, 10 Jun 2026 23:38:28 GMT  
		Size: 25.8 MB (25773188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c149542d536d695da06e29922f43be6a96fab117769d360a14a1936275393e2f`  
		Last Modified: Thu, 11 Jun 2026 00:58:02 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebc44148484b5f5268303277aa7dc2d7f6b7c4c9d47af23a9d426f9815498de`  
		Last Modified: Thu, 11 Jun 2026 00:58:02 GMT  
		Size: 4.2 MB (4151334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839cbe5cdc623b5df4c39020b9d4b6e0f695e7702b781339ade89195902456b0`  
		Last Modified: Thu, 11 Jun 2026 00:58:02 GMT  
		Size: 1.2 MB (1220097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f9282d99f40fe1d3d54a1e8c02928055f06991ebd27d4e8461f8c66c6c4564`  
		Last Modified: Thu, 11 Jun 2026 00:58:02 GMT  
		Size: 8.1 MB (8066599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db6b915ffde89e309a42e8460696969cd3a4127a3e63f9bad39c7c1fcc78723`  
		Last Modified: Thu, 11 Jun 2026 00:58:03 GMT  
		Size: 1.2 MB (1195105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e7404f4bcca2695dbb1f3f2b2f18387f8694ec2b3c4600f70d991b3767007f`  
		Last Modified: Thu, 11 Jun 2026 00:58:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78f279ac66883a22a187288e343ad44adb1c3b1603a550c7d2900d65912dab3`  
		Last Modified: Thu, 11 Jun 2026 00:58:04 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07aa1b351aa9e0cfc032e19fa6328421362536618acf9fa545fe609ef95cb564`  
		Last Modified: Thu, 11 Jun 2026 01:13:57 GMT  
		Size: 107.7 MB (107662880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2736b00eee193a0638c8650d8db5909ad315194cf5f424e68d2d0632226d4f`  
		Last Modified: Thu, 11 Jun 2026 01:13:54 GMT  
		Size: 10.0 KB (9973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0443b47bde73057751a28459e8847be0153b11f1002ae807f4fda92205d418`  
		Last Modified: Thu, 11 Jun 2026 01:13:54 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f70a72542993ae225955eecf38df6e8df5c71a0d5cca7f7e6440550196694a`  
		Last Modified: Thu, 11 Jun 2026 01:13:54 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc4cc0827a6902388c39af2ce3c97004cf25462c3c417999917e8eb770425`  
		Last Modified: Thu, 11 Jun 2026 01:13:56 GMT  
		Size: 6.1 KB (6093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb20845e1be485286f419a4752eaf894962a967cae802b4bd707ac657fe0383`  
		Last Modified: Thu, 11 Jun 2026 01:13:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:0e8691f2de8c1a41fe50eab2f35ac8e8cf0f82b4ff8b88e91722897986190b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f49d05c945ab802872b88426d649ede4a690fb45b3ce1675219468366cc7324`

```dockerfile
```

-	Layers:
	-	`sha256:ade8d0d8b4e1eedb844e8ec67dd877e81397f79622883a040c9f3c80e98aa94f`  
		Last Modified: Thu, 11 Jun 2026 01:13:54 GMT  
		Size: 5.9 MB (5927689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd09838b6f48476b8961bce71fd58c256eb0fec7e54c5f572729489829ad9ed2`  
		Last Modified: Thu, 11 Jun 2026 01:13:54 GMT  
		Size: 53.5 KB (53502 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:aa92a9b2f2fbc39836d988f715aa720039b66cb04102b1e4d9a2463592e9bab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143112032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb122015c08fa41b7ca2f9ebf1e4e627fb4ef11f4bd6387989033c213cc36ed8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:07:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 01:07:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:07:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 01:07:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 01:07:50 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 01:07:50 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 01:07:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:07:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 01:07:54 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 01:07:54 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 01:07:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 01:07:54 GMT
ENV PG_VERSION=16.14-1.pgdg12+1
# Thu, 11 Jun 2026 01:22:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:22:47 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:22:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:22:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:22:47 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:22:47 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:22:47 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:22:47 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:22:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:22:47 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:22:47 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:22:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8ae2378435d99f39097aa4fd0d6c58c08445becca3153d53205b2cc5054b09c2`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 23.9 MB (23944473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69df9754290b3704fe5d1b4aef2efe241be53f29e04c39ade5c7f5e96a7c2196`  
		Last Modified: Thu, 11 Jun 2026 01:23:04 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d898615d714ac04a6ecffaa69ab070f47a55f8763f627a95c74f7d615b3455`  
		Last Modified: Thu, 11 Jun 2026 01:23:05 GMT  
		Size: 3.7 MB (3742672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f54c8f618a3e0d90e1a0205fe21bc7ee2d13bfd72ba663d1168b50de7e0071`  
		Last Modified: Thu, 11 Jun 2026 01:23:05 GMT  
		Size: 1.2 MB (1215996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4620aa12945169507de8bd85ad26e58e4170db90e3f32046ba23c343f10bacf`  
		Last Modified: Thu, 11 Jun 2026 01:23:05 GMT  
		Size: 8.1 MB (8066395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ae92a1a8265d82d5242e190bd20e21444b0b60b9c70dc58468ad5268c4994`  
		Last Modified: Thu, 11 Jun 2026 01:23:06 GMT  
		Size: 1.1 MB (1067276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f11590887e74523ab1eb115d8a5cc13e41461c45c7c4556cad482169c605b19`  
		Last Modified: Thu, 11 Jun 2026 01:23:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b97f8a0115126318288214a31227c1887677948b45f63dcadbbcbc4f356ba0e`  
		Last Modified: Thu, 11 Jun 2026 01:23:06 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29545a3bf56011291d7500182d12545a6ccc4f7f4436dc55089ad0bacff01977`  
		Last Modified: Thu, 11 Jun 2026 01:23:10 GMT  
		Size: 105.1 MB (105054245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b16a161a64e95a71806c2f12927df7820f0a9f44416686f34f88eec0256aec8`  
		Last Modified: Thu, 11 Jun 2026 01:23:07 GMT  
		Size: 10.0 KB (9972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bee03e8287d927fb4469d5ba8802a4ab05270d4547aa28bfbc4b0da5c5de47f`  
		Last Modified: Thu, 11 Jun 2026 01:23:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645cd840cde599525124ef387681f79604c555b20afbc0f82eb4885d6417441a`  
		Last Modified: Thu, 11 Jun 2026 01:23:08 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7143a2be86ba3d394c421699f046176d61cab79cd4ef3aaead13ea6f7a7ead21`  
		Last Modified: Thu, 11 Jun 2026 01:23:09 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc55507eb21e32d92acd35f8f963692113015d3f2c8ea9ff35d4f2bc36490af`  
		Last Modified: Thu, 11 Jun 2026 01:23:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a4d3c7f60533f223f181bf1de59bae112cff7b825165559d79bdfa3ac35619d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06eb4cb1c5cdb11d404b12b0aef953551b689f9e622d84ccc43ed026017292fe`

```dockerfile
```

-	Layers:
	-	`sha256:d08410915bd0f9d9ea84a19c2a19f33582e97e3bbc17ffe33d3a865a26f33ed7`  
		Last Modified: Thu, 11 Jun 2026 01:23:05 GMT  
		Size: 5.9 MB (5926944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a18df4d028cf0a7d5eaeaf5bb1b3998ae9d54e1effe10e068dcefc8cd2769821`  
		Last Modified: Thu, 11 Jun 2026 01:23:04 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:f71d1a7a93444df92d7ecbddd79ea3931dba07006a8ab741bdeed77e1f1249a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153069152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560cf23fde98172534a8ae2025da1da435d898cf77889c14a10cd891575593f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:35:41 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:35:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:35:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:35:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:35:57 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:35:57 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:36:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:36:00 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:36:00 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:36:00 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 00:36:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 00:36:00 GMT
ENV PG_VERSION=16.14-1.pgdg12+1
# Thu, 11 Jun 2026 00:37:04 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:37:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:37:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:37:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:37:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:37:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:37:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:37:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:37:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:37:05 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:37:05 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:37:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a9062254aef8aa6df82900475d32a3fd4079a415538a4e050df24bdf87be01`  
		Last Modified: Thu, 11 Jun 2026 00:36:39 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd8cdd78f9da2bc11d8aec8ddeebe45b60ae0feaa87482da012bab293755f54`  
		Last Modified: Thu, 11 Jun 2026 00:36:40 GMT  
		Size: 4.5 MB (4519569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd07612818c7e1cdbe488303677ac02228a8300b125cb25616fa7598d2ddcb7`  
		Last Modified: Thu, 11 Jun 2026 00:36:39 GMT  
		Size: 1.2 MB (1203305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9584fb3c1c579b7b6701b2f6b03875d3f0d7ed31f6efefde6c652f218462a8`  
		Last Modified: Thu, 11 Jun 2026 00:36:40 GMT  
		Size: 8.1 MB (8066477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3605f7424ed23690d361a1a7c1b6474bc171785f3dd6cf4265520ae9e00077`  
		Last Modified: Thu, 11 Jun 2026 00:36:41 GMT  
		Size: 1.1 MB (1109063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bed65b0bcb7151fe36390e8498857117ca754b8a9ac0557802c84e8127ebe3`  
		Last Modified: Thu, 11 Jun 2026 00:36:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6e22b3d2cfebea1832aec044634ef90afd636a8ea8117ae46e4041f7c5027a`  
		Last Modified: Thu, 11 Jun 2026 00:36:41 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88b2cf0dd7fa58d4d10bc9f7189505bfe46c99c0f41631f0f3813fdcbcede07`  
		Last Modified: Thu, 11 Jun 2026 00:37:27 GMT  
		Size: 110.0 MB (110027475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341c4104268d9c5a4182458373242dabf8451be56fb4fedc12bd9423eff0becc`  
		Last Modified: Thu, 11 Jun 2026 00:37:23 GMT  
		Size: 10.0 KB (9959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738df5346aeef5432d385e2e7147983bde651c25d6c0b594612ec7bf808e1aae`  
		Last Modified: Thu, 11 Jun 2026 00:37:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7b36cfe180fc31feb35661930b3984eb2133be3bbdf50ad8264ae5ebcacd90`  
		Last Modified: Thu, 11 Jun 2026 00:37:23 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e57b1b90c2e499aab945888f95d8e16c3526bd4a71f9e43c0b17d22cabacbd6`  
		Last Modified: Thu, 11 Jun 2026 00:37:25 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3a3a5cff406053116c6fc9d02bfeb7955431de0914723f8a9a2f3fbfba608d`  
		Last Modified: Thu, 11 Jun 2026 00:37:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d34bd4bdb0232724a8ce1e987fb8758912d154a48a69a22cb98f6f3fced38bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5969444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956108ded366a0219d49380780245af43468061af5d32c592f7bfc7b772b4548`

```dockerfile
```

-	Layers:
	-	`sha256:bc2efc0a786a48a0bbecfebdf4bf498d2cefd8fe1a30dd5fb43c2096bc08aa98`  
		Last Modified: Thu, 11 Jun 2026 00:37:24 GMT  
		Size: 5.9 MB (5915903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd2380da22d27eb61b4908dfacd9162df200884838f7015adb461919013b71e`  
		Last Modified: Thu, 11 Jun 2026 00:37:23 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:4cfa6ebbce34fcd4c1eb8be44430ba1c659a1612e945b223b22eed44dcae534e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163888055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11bb07bbc087ba8aa48cdb606ee00321b9031779ae50e570c514aad0bb53914`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:32:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 11 Jun 2026 00:32:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:32:56 GMT
ENV GOSU_VERSION=1.19
# Thu, 11 Jun 2026 00:32:56 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 11 Jun 2026 00:33:01 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 11 Jun 2026 00:33:01 GMT
ENV LANG=en_US.utf8
# Thu, 11 Jun 2026 00:33:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:33:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Jun 2026 00:33:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:33:05 GMT
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 00:33:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 00:33:05 GMT
ENV PG_VERSION=16.14-1.pgdg12+1
# Thu, 11 Jun 2026 00:44:23 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 00:44:23 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 00:44:23 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 00:44:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 00:44:24 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 00:44:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 00:44:24 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:44:24 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 00:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:24 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 00:44:24 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 00:44:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c5815a8a64d614f5ff892e7e80fccffffc39dcad5da2d12fe503f72214d6b`  
		Last Modified: Thu, 11 Jun 2026 00:44:44 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4f8536eb82061696accf08bbf5985785da6dcb437198a7bfbf5ba81b7846ee`  
		Last Modified: Thu, 11 Jun 2026 00:44:44 GMT  
		Size: 5.0 MB (4966083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071754fa27d22b6f548c362ad971ac7000bc4621888618af06bb28c69b27b947`  
		Last Modified: Thu, 11 Jun 2026 00:44:44 GMT  
		Size: 1.2 MB (1218644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34732a93a34e1f85b63def3b1255e1eed56cbac7a5d743d849085edbe4a528ad`  
		Last Modified: Thu, 11 Jun 2026 00:44:44 GMT  
		Size: 8.1 MB (8066460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9ced0576ba33cd404fd5c88e698070a577428ab9d2402ecca1bf8f7f3be0f`  
		Last Modified: Thu, 11 Jun 2026 00:44:45 GMT  
		Size: 1.1 MB (1137474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada26be53ef763537b0525eb73606b56462a2c916d3c77637475c0a00615aa4a`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1de0fa6da775c96dbb0afa30f16e6d43c88130e98bc7b41001e497a7c3e207`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1365430d153e96c08f10626af21bd13ccbcac07b7dcbb994ff02ee2277535d20`  
		Last Modified: Thu, 11 Jun 2026 00:44:48 GMT  
		Size: 119.3 MB (119252664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3737747786aca8b671fdc020a6456c0146890eedbd487bb56b98b2a5e170d3`  
		Last Modified: Thu, 11 Jun 2026 00:44:46 GMT  
		Size: 10.0 KB (9970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68452cd200410a94aa888eeee99194f5fdb90f0b5ace9c32f9769605318b39a`  
		Last Modified: Thu, 11 Jun 2026 00:44:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3405c5792ba35331d5c93e4f5400326b86e3d6185d924cf0165ccab49fd267`  
		Last Modified: Thu, 11 Jun 2026 00:44:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f2f8cb981a1c171dc500e4457f1a4f3d6ba8f4431210305f67c4bb82c9f900`  
		Last Modified: Thu, 11 Jun 2026 00:44:48 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab7547ed842f522d1cb1051bfb2066399be62895040ee0c7925fa79252c809`  
		Last Modified: Thu, 11 Jun 2026 00:44:48 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b0dead208df76ac97cc840c4f51944549a89a4ff090fe4a34af7310567e550c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5979084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9206b029ad042f9a87561f5d20b31c6e45f9108295c11c9b24cc736ef49907d`

```dockerfile
```

-	Layers:
	-	`sha256:cbc82542fc2696718b36d6c4cec3aecb1c84fa1b088d5447601cdcb5830287b5`  
		Last Modified: Thu, 11 Jun 2026 00:44:44 GMT  
		Size: 5.9 MB (5925832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f22f69a4494212af34f3b1e9cafc84a2be4c0746dae79534e13329210520ed1`  
		Last Modified: Thu, 11 Jun 2026 00:44:44 GMT  
		Size: 53.3 KB (53252 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:516eb413b311a8b932e4f55858f1ff1abc2e23c95bff126d9c49b75a226c3f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153943280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8f50656d49f88c7e097b75bfc88445e486a7363c313f4762209915085c2412`
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
ENV PG_MAJOR=16
# Wed, 20 May 2026 03:49:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Wed, 20 May 2026 03:49:29 GMT
ENV PG_VERSION=16.14-1.pgdg12+1
# Wed, 20 May 2026 07:22:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 07:22:48 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 07:22:50 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 07:22:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 07:22:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 07:22:51 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 07:22:53 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 07:22:55 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 07:22:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 07:22:55 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 07:22:55 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 07:22:55 GMT
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
	-	`sha256:8b644ac44bb050482adc420dd05e695482a13061b13ec2d4fdec413d2c4d3374`  
		Last Modified: Wed, 20 May 2026 07:25:01 GMT  
		Size: 110.5 MB (110515740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7239b8c834e9203a77b40a8b0ad1e3dbae45951dbf4ee237322f71c173ab53bf`  
		Last Modified: Wed, 20 May 2026 07:24:50 GMT  
		Size: 10.0 KB (9976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e8c5830ac134dbabb956898f937294c130af27a2aebd0febb59b5db6db0f78`  
		Last Modified: Wed, 20 May 2026 07:24:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45758cca49b5cfc4fa426319a79dcbe5676f25f22d1a97027eea02116ebffd4`  
		Last Modified: Wed, 20 May 2026 07:24:50 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b027e619d913ac3c05d4c590adeb27f7ec810cc706c920dc922cac323b646b7`  
		Last Modified: Wed, 20 May 2026 07:24:51 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46eb23fb3fba912ffa026eb5f5a2d313fb37ae79af02c3887f95a1196f08b030`  
		Last Modified: Wed, 20 May 2026 07:24:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ddf03fa3acfd0e87ac4c709659ce3bdbcee641b16f6c89102302dec145cd4e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 KB (53162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec6d3c5c7c7b8a33154d90768eb2c725548f85e6b8c23e2d5d9e2250ad21fd8`

```dockerfile
```

-	Layers:
	-	`sha256:e67313974956016b5ca180f80bbf54a90045c1a63c4c5eb65ec679d8584b4bb0`  
		Last Modified: Wed, 20 May 2026 07:24:50 GMT  
		Size: 53.2 KB (53162 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:e8c8f9241fe0d6d7591b475b44d5b7cbd45ea9df11b54d1e4522905e323f38fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167846743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233f0c3f8d54fa613c60f068697ddd7fb5681951db4b95136fd42ea829f8aa3a`
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
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 04:25:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 04:25:31 GMT
ENV PG_VERSION=16.14-1.pgdg12+1
# Thu, 11 Jun 2026 04:30:27 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 04:30:28 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 04:30:28 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 04:30:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 04:30:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 04:30:29 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 04:30:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:30:30 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 04:30:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:30:30 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 04:30:30 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 04:30:30 GMT
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
	-	`sha256:3658fc0040cdb191a975637ee467b7498020973d12a54cabdae06fddcbfbce4b`  
		Last Modified: Thu, 11 Jun 2026 04:31:11 GMT  
		Size: 119.8 MB (119816822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a3367be1dddeb14d970cac21a75f211d4793c0763f30d457f3dee2eb004d48`  
		Last Modified: Thu, 11 Jun 2026 04:31:09 GMT  
		Size: 10.0 KB (9966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08b5cf30380c3c0b88c6811159ed4924b46ceaf95c53858f8d11651098b10be`  
		Last Modified: Thu, 11 Jun 2026 04:31:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8210ec8928e4da5370567e009cae9fc80a7b7206a2ca11a2926cc9d5098527cf`  
		Last Modified: Thu, 11 Jun 2026 04:31:09 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fb06a54831fc9bbbd6ecf9d989ec8ea0d3c02cd953d7a9c1abaf1d493baae3`  
		Last Modified: Thu, 11 Jun 2026 04:31:10 GMT  
		Size: 6.1 KB (6095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acd8440386171798e2c380fca856860373b0c2db8feb1184c62b27af5fbd822`  
		Last Modified: Thu, 11 Jun 2026 04:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:61c05760642d9f80d6874293e88d49221cc1f6aef515d55a7ea0814dec4ca972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7d2944d3815e9aeea8367707c7f338e572b4c76ec444eba4fc0f51b8758646`

```dockerfile
```

-	Layers:
	-	`sha256:0038f39448901a151eebd10367f5c0fc1679e6000282a4cead9577aea45d1398`  
		Last Modified: Thu, 11 Jun 2026 04:31:09 GMT  
		Size: 5.9 MB (5916953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32ea16916a82da0956575cf121b12fe8fff398d9fa92e7b3ff9b38f38c947c22`  
		Last Modified: Thu, 11 Jun 2026 04:31:09 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:1a5ec036a84612b84d05f6e70af30da226f4538b92064c232b70ee0abaddb66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164304353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffc7aaa877ae8a7e455082e49a1873a88d4a7287fa24a36f59f6d4f5269f85e`
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
ENV PG_MAJOR=16
# Thu, 11 Jun 2026 01:02:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/16/bin
# Thu, 11 Jun 2026 01:02:13 GMT
ENV PG_VERSION=16.14-1.pgdg12+1
# Thu, 11 Jun 2026 01:27:43 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 11 Jun 2026 01:27:43 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 11 Jun 2026 01:27:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 11 Jun 2026 01:27:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Jun 2026 01:27:43 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 11 Jun 2026 01:27:43 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Jun 2026 01:27:43 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 01:27:44 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 11 Jun 2026 01:27:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 01:27:44 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jun 2026 01:27:44 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 11 Jun 2026 01:27:44 GMT
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
	-	`sha256:71f179a20192c7dfd2d3673fc504847a31f09e0de6ed116db768d2f0d780e88b`  
		Last Modified: Thu, 11 Jun 2026 01:28:17 GMT  
		Size: 122.6 MB (122558063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bfb02a4056211f402be3f4b66ac34072433549230839866cd2b1f681f6e2c4`  
		Last Modified: Thu, 11 Jun 2026 01:28:14 GMT  
		Size: 10.0 KB (9969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9497e9538a76248bbc0a35ee2dc130ccb7b3618ad9a69740117023f3a53494ba`  
		Last Modified: Thu, 11 Jun 2026 01:28:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a7203ebee108a60a9efecc8a7b277fe7311821dbee372c60a6c9bb4cd86922`  
		Last Modified: Thu, 11 Jun 2026 01:28:14 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a1fefa22e429289971b79b2b9f8038648e6374f300e8a8aa7602ff6ae13124`  
		Last Modified: Thu, 11 Jun 2026 01:28:15 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da0efd594935e6730b225baa5474f01d2ff86ee1a5b7f94d36fec65b64910a5`  
		Last Modified: Thu, 11 Jun 2026 01:28:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:a7d61faba9de292780d802da07ba7bb6e905efbdff2fef2bb6ccb5e863053223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23550a95662dc00b50fcb5cd823f96518d2cc43e0181c47169acc3eea6225d41`

```dockerfile
```

-	Layers:
	-	`sha256:4877f732fa14a3f64ab37b85e1cacff729abb28da8bee69ddb1878fe4849a2bb`  
		Last Modified: Thu, 11 Jun 2026 01:28:14 GMT  
		Size: 5.9 MB (5922308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5539085c4f189964fcef8111e284cc36a7244c582e47be06019ebd2a19cf16`  
		Last Modified: Thu, 11 Jun 2026 01:28:14 GMT  
		Size: 53.3 KB (53293 bytes)  
		MIME: application/vnd.in-toto+json
