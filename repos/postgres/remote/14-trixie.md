## `postgres:14-trixie`

```console
$ docker pull postgres@sha256:473783dca8870bbde3a32370c72a9de9406f37d048c05d7b5c40f93e7c23d827
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

### `postgres:14-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:9d5c1864742c653a8d992eed718d712ddd456315619dc60bdefff02fdeddfceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (156971260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75312cdf08fe74d02a44e01ddf4fe96751be7b38d510306d84d1493f38e5d410`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:03:55 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:08 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:08 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:04:13 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:16 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:17 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:04:17 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:04:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 12 Feb 2026 21:04:17 GMT
ENV PG_VERSION=14.21-1.pgdg13+1
# Thu, 12 Feb 2026 21:05:57 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:05:57 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:05:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:05:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:05:57 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:05:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:05:57 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:05:57 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:05:57 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:05:57 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:05:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cf9c3371344e1e0395a76699ab3b04af0fe9bbc6fa282ae056f5ab48a719cf`  
		Last Modified: Thu, 12 Feb 2026 21:04:49 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64dbdf800a20b16f4600802b0f94b9e8319437143ef8000d0edc5f5d87d658f`  
		Last Modified: Thu, 12 Feb 2026 21:04:49 GMT  
		Size: 6.4 MB (6437944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2710e764d89a97b2c18caa5e3f6a7eb95b78d65ac9d5c172894351a4237e40dc`  
		Last Modified: Thu, 12 Feb 2026 21:04:49 GMT  
		Size: 1.3 MB (1256747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a02fe2f5f58a855df985f39d38ec26f5f3f9f5a5c7c90dd1ae382428ee44e`  
		Last Modified: Thu, 12 Feb 2026 21:04:50 GMT  
		Size: 8.2 MB (8203806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ace4c983c3e1e2aa028fb2d43257959137961ca109b27203cad5e3019e31566`  
		Last Modified: Thu, 12 Feb 2026 21:04:50 GMT  
		Size: 1.3 MB (1311634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64f280cfa2b7e198ed7c19f23deabe02a50f43b8ecb78fce0fa62f32fa2a708`  
		Last Modified: Thu, 12 Feb 2026 21:04:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5e741a30cefaa1c4b7b491bd9af618bc141646c2ce72aa3b48c8ef7556e958`  
		Last Modified: Thu, 12 Feb 2026 21:04:51 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8ced8da69c72ae3bf39c8ac31a6a32d904328954bb9c68b150964f7e94a3e2`  
		Last Modified: Thu, 12 Feb 2026 21:06:18 GMT  
		Size: 110.0 MB (109962150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30da6a0319df04ca6ff1f3f3cd12cbfceefa52c07f498b2ddad28e50f9f50f15`  
		Last Modified: Thu, 12 Feb 2026 21:06:15 GMT  
		Size: 9.6 KB (9630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146c4548d20d3dd258b8adf751705589e8cb88ddeb566dc151b236b1b41173bd`  
		Last Modified: Thu, 12 Feb 2026 21:06:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51329b6ec5083c37ab6d2cf8585d3396c4df083d1e6f253e04cdd95611ed5d31`  
		Last Modified: Thu, 12 Feb 2026 21:06:15 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1b7745835fef165689b7f5862714db98e94b5ec6b5ec0f665b75c9378deb9d`  
		Last Modified: Thu, 12 Feb 2026 21:06:16 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0472b5544fb085fd8bcd2a37945d8e96e48bfb9a490e47140a64ae7076361e27`  
		Last Modified: Thu, 12 Feb 2026 21:06:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:15c2890a7fddffaf4f2ff439322b48eca65386b3a612c393e976ecbfd0e0245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5647307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaf66d11b8254ffa4fb4ed92cc883a4ca14040f966a733a7f621f71336bfe70`

```dockerfile
```

-	Layers:
	-	`sha256:cb6db9529db163e04a2dec7fa710b0fa4c3b674e51d18bba9cfc3cdc35ff4bae`  
		Last Modified: Thu, 12 Feb 2026 21:06:15 GMT  
		Size: 5.6 MB (5593445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1063e5e463ec34e6edfaf24e2462a826a5453ec967153e75116fe1cd213386a8`  
		Last Modified: Thu, 12 Feb 2026 21:06:15 GMT  
		Size: 53.9 KB (53862 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:e039d65689617805ebe4261376bfc3271ed9b8d46a6f0393ba8f364a057638aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150999767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe15517c6612f43204c9ecf558b3bc07683ad51b76ee7d3abf9a9e08d2717ab2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:16:18 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:16:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:16:38 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:16:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:16:47 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:16:47 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:16:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:16:54 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:16:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:16:55 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:16:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 12 Feb 2026 21:16:55 GMT
ENV PG_VERSION=14.21-1.pgdg13+1
# Thu, 12 Feb 2026 21:32:42 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:32:42 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:32:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:32:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:32:42 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:32:42 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:32:42 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:32:42 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:32:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:32:42 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:32:42 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:32:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967a44a6d901719642448c103d225c767637fa3eeee6140c46e4eb6cec2822c`  
		Last Modified: Thu, 12 Feb 2026 21:33:01 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03de129cbadb3fea5d9a6d9975f6198035191c87086f2f27ca88bb76c6f63ce2`  
		Last Modified: Thu, 12 Feb 2026 21:33:01 GMT  
		Size: 5.9 MB (5930330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bc3a3fc054d5277b9a752d21fee9a84f1aedc24d840dd09a568de5b693d32a`  
		Last Modified: Thu, 12 Feb 2026 21:33:01 GMT  
		Size: 1.2 MB (1227511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14962e19b182e8c10c59ce1417f13fabd89448cc626ba86c5e5667288120530`  
		Last Modified: Thu, 12 Feb 2026 21:33:01 GMT  
		Size: 8.2 MB (8204255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b49a6ea139f5b5c7053a99f7311fdf61317d31032f897dcff173556c7ef58`  
		Last Modified: Thu, 12 Feb 2026 21:33:02 GMT  
		Size: 1.3 MB (1317294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d35cfaf0f9b9f7e9731c644109119c2c69526353e170f0740730221a1b2365`  
		Last Modified: Thu, 12 Feb 2026 21:33:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d995f9762215162dfd7c65753ba1c98ddef398953a2ef0f9fec5c669af4baea`  
		Last Modified: Thu, 12 Feb 2026 21:33:02 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93cc95e817a168364c4554ca5c6ee15115c071680d2235b600655e589fe80e3`  
		Last Modified: Thu, 12 Feb 2026 21:33:05 GMT  
		Size: 106.4 MB (106352444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494f6eb2f83aeef6ee4927819d34bb7bea6073d194615b4591c87472e14d6ed0`  
		Last Modified: Thu, 12 Feb 2026 21:33:03 GMT  
		Size: 9.6 KB (9625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7104286ddef0a6da886a32cc238565916d42e41ecc96ee1c51a59fbb9f18132`  
		Last Modified: Thu, 12 Feb 2026 21:33:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a607468edc2ec7f2bdcfe597fd40bf40b7704f74aefd2d49f291819c4090ac9c`  
		Last Modified: Thu, 12 Feb 2026 21:33:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5329eb4a5ddd5921dddbf499c485daa2438d424afc578037d66e00cae6d3be`  
		Last Modified: Thu, 12 Feb 2026 21:33:04 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc134b55ad4f3c6d469025ac9c2683cedf211e6b92a8268778b913e3b3339a8`  
		Last Modified: Thu, 12 Feb 2026 21:33:04 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:76979b7762603340beed81dbf376f1281d0e0c111172efd1efef9bffe8c5cc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5664170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbcc539a8bab22bb5bc27779fd6617eab260ba721d650a5d70227034fbaab62`

```dockerfile
```

-	Layers:
	-	`sha256:f691546138097e1533c4a8f14a52570e1344792deee1a43206af28861599dec2`  
		Last Modified: Thu, 12 Feb 2026 21:33:01 GMT  
		Size: 5.6 MB (5610083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6e73976c73648cd19028614112d5c2469761531b67ef502f795bdefbd829ecf`  
		Last Modified: Thu, 12 Feb 2026 21:33:01 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:fdb9cc538910413a4fba9f2a1a45043f00b7559323a4f6d6683ed2be7a72eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146098080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73278ead75c2420ccc3ba46836271dec91209aa5930bd1ae4adfffbd7a7a2d17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:32:51 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:32:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:33:07 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:33:07 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:33:13 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:33:13 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:33:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:33:18 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:33:19 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:33:19 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:33:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 12 Feb 2026 21:33:19 GMT
ENV PG_VERSION=14.21-1.pgdg13+1
# Thu, 12 Feb 2026 21:47:14 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:47:14 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:47:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:47:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:47:14 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:47:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:47:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:47:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:47:14 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:47:14 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:47:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a4c528ad85e20815ebdfc8e457c884924e8dfde9a91624f6d6e3d0ae78be90`  
		Last Modified: Thu, 12 Feb 2026 21:47:31 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41410ccc05a500a458d91094b553a853f45f192d1c6b6bb695eb8119b7c1037f`  
		Last Modified: Thu, 12 Feb 2026 21:47:32 GMT  
		Size: 5.5 MB (5496443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd85d7de80b01bc89d20291a8ffbd556a3847311461b304f5185d56e0700e53`  
		Last Modified: Thu, 12 Feb 2026 21:47:32 GMT  
		Size: 1.2 MB (1222383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74ae64137286c28876bde543d3e0df31d29c1be0765115721da8736c9d353f`  
		Last Modified: Thu, 12 Feb 2026 21:47:32 GMT  
		Size: 8.2 MB (8204021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f556e7fedf83bc5ab9536ed252b64b848dfc36a06003bc5e06a5d821d346309`  
		Last Modified: Thu, 12 Feb 2026 21:47:33 GMT  
		Size: 1.2 MB (1172612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b493ac6f0aad208c6175702df5c494d1eecbe98e8387dd665df32c5c0d23e9a7`  
		Last Modified: Thu, 12 Feb 2026 21:47:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e412cd4427f32daec1effa1e3842b435fa7b6537b3be3dba9c4d63cca207869c`  
		Last Modified: Thu, 12 Feb 2026 21:47:33 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5712d948f43fc40df9c49cae880dc2683c1b7a7532eabbb5333114babc5913f`  
		Last Modified: Thu, 12 Feb 2026 21:47:36 GMT  
		Size: 103.8 MB (103768481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef56a2e78a2eecf159e1118b990f1f62a0e1e0e4d5918c329ee630788bfe8b92`  
		Last Modified: Thu, 12 Feb 2026 21:47:34 GMT  
		Size: 9.6 KB (9639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2badcd0bc47e64da466d61d547944c5481bc13b4300e6c31326d7c7dabe7cf`  
		Last Modified: Thu, 12 Feb 2026 21:47:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f4a8be884fbd9b2c4047d72151a6341a44917680a0b32c847e590c3465dc2f`  
		Last Modified: Thu, 12 Feb 2026 21:47:35 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892c783e71f0416238d4328cb81d6737df43066750ae4d637b4a51b5a1997634`  
		Last Modified: Thu, 12 Feb 2026 21:47:35 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4b40b266f871880853c65db437c5f6ba591165796462d901992d7f20f9cd0`  
		Last Modified: Thu, 12 Feb 2026 21:47:35 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:6acf737829bcfa7e8d41d9b0c30d1597b407ea063b98573f2c5ccb5d7dcbdbd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a162ef7459fc8df1749c1570ea6d91603956778c47b47638e57aa9c16ef87fe`

```dockerfile
```

-	Layers:
	-	`sha256:6f553da789d78242e5e347650b52bcfdf6bc77c10b494409f4fdcd4ee9d2171c`  
		Last Modified: Thu, 12 Feb 2026 21:47:32 GMT  
		Size: 5.6 MB (5609388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:670e7fc173ea0ebb8c598b6b948f0221412bd643cbb2520a90890634afc2d4dd`  
		Last Modified: Thu, 12 Feb 2026 21:47:32 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:26b5aecc91f0acaa3264757e6182343ebd7f8a96a4931a60bc6937c78b99d0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155598239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b131d647e29eed1bf8763071c16a2a5e8ce273f41ef44b5285ab0b63b5dcbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:04:03 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:04:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:16 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:04:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:04:22 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:04:22 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:04:25 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:04:26 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 12 Feb 2026 21:04:26 GMT
ENV PG_VERSION=14.21-1.pgdg13+1
# Thu, 12 Feb 2026 21:06:28 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:06:29 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:06:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:06:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:06:29 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:06:29 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:06:29 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:06:29 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:06:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:06:29 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:06:29 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:06:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b542344c2dd49abb167d2ec8a91435b093268a690f47de257e1b2eae5191e36`  
		Last Modified: Thu, 12 Feb 2026 21:04:59 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f22be18ff73a8bcb8d4fa46a6aee0de16932b0f37eb38646eb1a119b759e9d`  
		Last Modified: Thu, 12 Feb 2026 21:05:00 GMT  
		Size: 6.2 MB (6231026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13d2984009d21b4c1af262473530d16912df24b74b677a89fb879b5514ae312`  
		Last Modified: Thu, 12 Feb 2026 21:04:59 GMT  
		Size: 1.2 MB (1209511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062eb1ee0cd276dd0ae7530c24db1e2d7342c0790ecd1a5526eab36838802a63`  
		Last Modified: Thu, 12 Feb 2026 21:05:00 GMT  
		Size: 8.2 MB (8203905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e35784eed7152b6049866c7d9e3fa6e43bb068a1528bb8bd46385db39d49abe`  
		Last Modified: Thu, 12 Feb 2026 21:05:00 GMT  
		Size: 1.2 MB (1220542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac2aa55d9c41aad4e147f44ef6d7cfd2d5153f8c552892fd21d7c531aae00eb`  
		Last Modified: Thu, 12 Feb 2026 21:04:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d45713fedaaeae3ff7d299f7cf52cabda796569104cb1c4252d1936c4b794e`  
		Last Modified: Thu, 12 Feb 2026 21:05:01 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9becd16f20c43f7bf3714b3a2d60b80e4bb2d9a413deb56c658118a9da46ba`  
		Last Modified: Thu, 12 Feb 2026 21:06:50 GMT  
		Size: 108.6 MB (108572813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dafb900bde299a201bee22960904a0151e26cb408bd57146d7effd32322b43b`  
		Last Modified: Thu, 12 Feb 2026 21:06:47 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98dd8d0ce127fc34da9776a5f19fc6228c356effa3d3eca7880c160263516fe9`  
		Last Modified: Thu, 12 Feb 2026 21:06:47 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834062da726b4768001435f2bc18b8911ee14bacd8312488ce94efa9854e7527`  
		Last Modified: Thu, 12 Feb 2026 21:06:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f12bd1b37cde99a79bcc9a90fbecbea0f7810e303b73207272b0fe5c43604`  
		Last Modified: Thu, 12 Feb 2026 21:06:48 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be2ba3d371f3cb4fd1c83eb6b9403097b2797fbd454c80b15d55a2c9bf2a13e`  
		Last Modified: Thu, 12 Feb 2026 21:06:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:152fd57b45f248298d7668df96bba6492e0ceaa3d0da54ba8a30ec5d339ab9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5653924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee02d73805da8258d482129e20cb882cbe0ef05154ed4afa46c8eb902fbe5e5`

```dockerfile
```

-	Layers:
	-	`sha256:ee77d64082fb2fdf67da2ed1ccafa8098dd27f12bfe6cfd17d63fddf8240df42`  
		Last Modified: Thu, 12 Feb 2026 21:06:47 GMT  
		Size: 5.6 MB (5599791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4213553dbdf43caa52acad721f468389617de4cf305f714f0cb3de0d8136f35`  
		Last Modified: Thu, 12 Feb 2026 21:06:47 GMT  
		Size: 54.1 KB (54133 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; 386

```console
$ docker pull postgres@sha256:eebf350112dd29a95031d75ba01c02da02844ba50cc2f0bd25759f073102ff0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166035477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fdfab6c7e1efe362dae4d7e487c6139b418e909188228e6dee58bee58ccf26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:12:49 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:12:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:13:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:13:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:13:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:13:07 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:13:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:13:10 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:13:11 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:13:11 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:13:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 12 Feb 2026 21:13:11 GMT
ENV PG_VERSION=14.21-1.pgdg13+1
# Thu, 12 Feb 2026 21:22:35 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:22:35 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:22:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:22:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:22:35 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:22:35 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:22:35 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:22:36 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:22:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:22:36 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:22:36 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:22:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b56386fcaad5fb72e5ab2820f5e2ab473c0c167db86bf648b51ec556a08198`  
		Last Modified: Thu, 12 Feb 2026 21:22:53 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbb60b63a450c28e380e18bf46fa8009e68a1bb74ce5a68e324bb5bd4a6be28`  
		Last Modified: Thu, 12 Feb 2026 21:22:54 GMT  
		Size: 6.6 MB (6630523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27881d9faeb6cd5a317d1325a699fb6d2c1ce142dcc1bc3beaef0b2224cd900a`  
		Last Modified: Thu, 12 Feb 2026 21:22:54 GMT  
		Size: 1.2 MB (1225839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d6b0089a975e941235973af0f846dffcbfb50249d26710274dab560e911c00`  
		Last Modified: Thu, 12 Feb 2026 21:22:54 GMT  
		Size: 8.2 MB (8203941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b8df2d5e47179f7e6af1525e4646e736e2bb2af160f56b2cf69f6b411ffb84`  
		Last Modified: Thu, 12 Feb 2026 21:22:55 GMT  
		Size: 1.3 MB (1308265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b543609b89c432f63ef61f029c7aa71a0b56b7fb894054f6434ad9c95f02540`  
		Last Modified: Thu, 12 Feb 2026 21:22:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12d37182b6ec842680f8597ae3e2b0b99f7c5983880bae80092551a87148a84`  
		Last Modified: Thu, 12 Feb 2026 21:22:55 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b074e208eecd7856ef0d8e08dda42411c5d65a080ae444a680a2bd16ae41b994`  
		Last Modified: Thu, 12 Feb 2026 21:22:58 GMT  
		Size: 117.4 MB (117352675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8387a3f8a6fdc323ae7515791bf8b7092fef17e3355596f720e4d62b4b9a5fed`  
		Last Modified: Thu, 12 Feb 2026 21:22:56 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7505af23066880660fd3a4ead4e8cea7cf893c273474c25338dac889613426e8`  
		Last Modified: Thu, 12 Feb 2026 21:22:56 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cdd72dba15e0de7db14df99bcc8eedf8e551b9885365e8591b2c923d37d82c`  
		Last Modified: Thu, 12 Feb 2026 21:22:56 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8deeb2de6371478c6ab9919081126a9463cbc9f965386bd210b4fc1d08a7797a`  
		Last Modified: Thu, 12 Feb 2026 21:22:57 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62a5c3740ac94ab8b65dc62f43f552521d168c36059490cbf288dabaff3f02c`  
		Last Modified: Thu, 12 Feb 2026 21:22:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:320a32e4e91226881fc3c513c7344ca041f7024a384726e68728282fc598d84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5662785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a6c0085f94eb7119912dbd22bc7432e84c39843e9b15fad6fe206889c1b687`

```dockerfile
```

-	Layers:
	-	`sha256:4fd807d15d355268ce7f8246b5f42539cd11565da9da0b05c9bb048b74d9f977`  
		Last Modified: Thu, 12 Feb 2026 21:22:54 GMT  
		Size: 5.6 MB (5608976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71959b64e16fae2b4dedae22a728c5de92430b163097a5d9b62a49f11b988ad1`  
		Last Modified: Thu, 12 Feb 2026 21:22:53 GMT  
		Size: 53.8 KB (53809 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:f2e069f59db1f8dfe7d439059c82e07f42256ef973af22aa37a29e0d0bba0afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.2 MB (169162466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e76124a988cc6ddb71bf4ade9c1da0cbce71f42a0e9b87bbd12865c4993da4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:02:45 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:03:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:03:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:03:37 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:03:37 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:03:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:03:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:03:47 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:03:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 12 Feb 2026 21:03:47 GMT
ENV PG_VERSION=14.21-1.pgdg13+1
# Thu, 12 Feb 2026 21:31:47 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:31:51 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:31:51 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:31:51 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:31:52 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:31:52 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:31:52 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:31:53 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:31:53 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:31:53 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:31:53 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dd2116d4f00610191cab66c1981409e66c43cfcea0b7afce48664af9ada05a`  
		Last Modified: Thu, 12 Feb 2026 21:05:15 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99cf5a0f5205f034311e8f9c0c3a94a51781cb93e8f59f0ed6560400db6aeed`  
		Last Modified: Thu, 12 Feb 2026 21:05:35 GMT  
		Size: 7.1 MB (7076719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173747098b4670bdf4262d42a1b879833541a3e367f8432e0a2a119e0be551d2`  
		Last Modified: Thu, 12 Feb 2026 21:05:34 GMT  
		Size: 1.2 MB (1214809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92305f81f4a0a40d11db267bcf684c4a77eb2f095c690e267e6da2fea074bb22`  
		Last Modified: Thu, 12 Feb 2026 21:05:35 GMT  
		Size: 8.2 MB (8204037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136d6666bbf7d6240fbfe28141bdbed8a99a9cfc32497ac23e1bdad9a2ea2886`  
		Last Modified: Thu, 12 Feb 2026 21:05:35 GMT  
		Size: 1.4 MB (1394967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cda6fb4e1a3fc351a02d477d60c2a575674d6b5113368d1d651e093e4792f5`  
		Last Modified: Thu, 12 Feb 2026 21:05:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09b1640c0f3a3a530ecf3570c85b5a629532c446304c345cf8472675cb2915e`  
		Last Modified: Thu, 12 Feb 2026 21:05:36 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3776c2f0ada31b930942ebc6743d017646e44d1e97d59c7769259ab64413a2d0`  
		Last Modified: Thu, 12 Feb 2026 21:32:43 GMT  
		Size: 117.7 MB (117651369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aeed9b6c0e9f8c706b7f4a9d7498d7513e640d7d13fa84a287c37d548d194a2`  
		Last Modified: Thu, 12 Feb 2026 21:32:40 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850a25d50d96473406d03dab0f3774311cac48f2715b8135f4287ce8c490f6de`  
		Last Modified: Thu, 12 Feb 2026 21:32:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e778a238162168ff4d5173311a4abd2289bdcfd7b118916b78057f75438d6a1b`  
		Last Modified: Thu, 12 Feb 2026 21:32:40 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3360b644a67e15698b260ed9c2f86df7c683dda14713808f0b820129fbd7e94c`  
		Last Modified: Thu, 12 Feb 2026 21:32:41 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789c76c830157d0a353b99b05d1a7726f9496717d8783962b100565a32c315ef`  
		Last Modified: Thu, 12 Feb 2026 21:32:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:037297bd0771c2d0f6bdbed9375f600822447d95efab3badf6187712e8f049dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5653988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638c86adb1951a6446515b2fb1f1a8fd539485a9d5209d6bdb4d11d262f432d8`

```dockerfile
```

-	Layers:
	-	`sha256:08900e9fadaf93841ace4c94500dc52e02a53027ef98bfe1eaef806d1bec51d4`  
		Last Modified: Thu, 12 Feb 2026 21:32:40 GMT  
		Size: 5.6 MB (5600058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d90524e2674addce6e8558f9c663fe08a5ef074c9a718979be8c082527c05f1`  
		Last Modified: Thu, 12 Feb 2026 21:32:40 GMT  
		Size: 53.9 KB (53930 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:10179d599c5c6dfd58b477f655cb30a91ff259c1b4f198ce09e9baf017e795ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89257683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586aec20d59583ee82b57267cec1e57b2c37831f0505633a5e941c00da70fe43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 04 Feb 2026 16:13:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 04 Feb 2026 16:14:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 16:15:14 GMT
ENV GOSU_VERSION=1.19
# Wed, 04 Feb 2026 16:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 04 Feb 2026 16:16:15 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 04 Feb 2026 16:16:15 GMT
ENV LANG=en_US.utf8
# Wed, 04 Feb 2026 16:16:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 16:16:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 04 Feb 2026 16:16:58 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 04 Feb 2026 16:16:58 GMT
ENV PG_MAJOR=14
# Wed, 04 Feb 2026 16:16:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 04 Feb 2026 16:16:58 GMT
ENV PG_VERSION=14.21-1.pgdg13+1
# Fri, 13 Feb 2026 14:34:15 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Fri, 13 Feb 2026 14:34:16 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 13 Feb 2026 14:34:16 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Fri, 13 Feb 2026 14:34:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Feb 2026 14:34:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Fri, 13 Feb 2026 14:34:17 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Feb 2026 14:34:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 14:34:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 13 Feb 2026 14:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Feb 2026 14:34:17 GMT
STOPSIGNAL SIGINT
# Fri, 13 Feb 2026 14:34:17 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 13 Feb 2026 14:34:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80995be55917dc7fd201d347bc9226e2f5ac4bf648270056077ffdd82365b78c`  
		Last Modified: Wed, 04 Feb 2026 18:24:09 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1f5c6b2d99f755313f7c8a99b0dc4359c317ad0b8bf85fa05a15235111d7c2`  
		Last Modified: Wed, 04 Feb 2026 18:24:11 GMT  
		Size: 6.3 MB (6292229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3419a5cae79de9fcd3de7a8c5585cda9f74e580063c21f2ba132beaaf144525a`  
		Last Modified: Wed, 04 Feb 2026 18:24:09 GMT  
		Size: 1.2 MB (1202087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1011f782d19ba43309db24778d82c70cb389a070476ff5dae98b8b45210498d`  
		Last Modified: Wed, 04 Feb 2026 18:24:12 GMT  
		Size: 8.2 MB (8203651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0485b03c21170701329d20fbb35c7b9ca2b9d9a7d4437c48576a357aed50c301`  
		Last Modified: Wed, 04 Feb 2026 18:24:11 GMT  
		Size: 1.4 MB (1402345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e055b637555d4df19ff25f1e2fbb73523accc9fa0389284938730df0384953bb`  
		Last Modified: Wed, 04 Feb 2026 18:24:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d5fd337755cc5ee8443095f73c397172e5f877bb14a60fe985381ee14c8dd5`  
		Last Modified: Wed, 04 Feb 2026 18:24:12 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea5c2c40fcf69fb8c27a00ad5d9473dc190f561520046a252d066be9f4b0294`  
		Last Modified: Fri, 13 Feb 2026 14:36:45 GMT  
		Size: 43.9 MB (43860599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867fbc8ce62d7872cd7075ac933b8fe96a543ce7ed444808b548aa09f2159830`  
		Last Modified: Fri, 13 Feb 2026 14:36:38 GMT  
		Size: 9.6 KB (9630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc49ac829bb4fe812ad32de360212cb8e6767885fb31349ef2cadc592da56a1`  
		Last Modified: Fri, 13 Feb 2026 14:36:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c7fd6ab3bd239ba003122e47cc377d52e7681a80c9b0d980c65f7631d929a5`  
		Last Modified: Fri, 13 Feb 2026 14:36:38 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea322a84da50bdcd112a89d3caef7d11054f20751877c449c3c6df9890d6b43`  
		Last Modified: Fri, 13 Feb 2026 14:36:39 GMT  
		Size: 5.8 KB (5842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d742e353e7c21e5155fcd85bf64fcb8921a7c9c6df5c4854fc2c831854667e`  
		Last Modified: Fri, 13 Feb 2026 14:36:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:aab45eae7aea3a14cf1835b7436fb693a824f1278afb0cdcf0efddbb2fab59e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5053573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627e0d51c9406f5d8d0de525f36449d1bd95d0fef965316c3553c569194b5cbf`

```dockerfile
```

-	Layers:
	-	`sha256:a97ad20a7dab091b950c21a63929b57637ccae67e71a01036879071967b4c5dc`  
		Last Modified: Fri, 13 Feb 2026 14:36:39 GMT  
		Size: 5.0 MB (4999650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63fd1f19bde7592cfa84ca67a1eb8994433cc2dbb623a7b5854b5f698c6bec4f`  
		Last Modified: Fri, 13 Feb 2026 14:36:38 GMT  
		Size: 53.9 KB (53923 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:05df716d59bea9691422fe64e2e8dd74a2fa4ad2a4a0586364362d39d2e7ba5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171466002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0512cfad520d4f7d7734276ae7dacb9eb4d82c76a645d885125ed8cab9f815c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 12 Feb 2026 21:20:47 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 12 Feb 2026 21:20:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:21:02 GMT
ENV GOSU_VERSION=1.19
# Thu, 12 Feb 2026 21:21:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 12 Feb 2026 21:21:07 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 12 Feb 2026 21:21:07 GMT
ENV LANG=en_US.utf8
# Thu, 12 Feb 2026 21:21:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Feb 2026 21:21:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 12 Feb 2026 21:21:12 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 12 Feb 2026 21:21:12 GMT
ENV PG_MAJOR=14
# Thu, 12 Feb 2026 21:21:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Thu, 12 Feb 2026 21:21:12 GMT
ENV PG_VERSION=14.21-1.pgdg13+1
# Thu, 12 Feb 2026 21:48:54 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Thu, 12 Feb 2026 21:48:54 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 12 Feb 2026 21:48:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Thu, 12 Feb 2026 21:48:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 12 Feb 2026 21:48:54 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Thu, 12 Feb 2026 21:48:54 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 12 Feb 2026 21:48:54 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 12 Feb 2026 21:48:54 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 12 Feb 2026 21:48:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Feb 2026 21:48:54 GMT
STOPSIGNAL SIGINT
# Thu, 12 Feb 2026 21:48:54 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 12 Feb 2026 21:48:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5c2cc6c8c624e8a29faeb4bf0ea1007226ed28aea25b7d120ee24b80602e03`  
		Last Modified: Thu, 12 Feb 2026 21:33:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1816ef1e9b4ab32f9a5109168db210423ac1d74ddec20bfa0095d02fb4160d6`  
		Last Modified: Thu, 12 Feb 2026 21:33:44 GMT  
		Size: 6.4 MB (6408738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6296ffec2849898efe4761e17b70e33b1d95648631d6e029d7e017df67fd93`  
		Last Modified: Thu, 12 Feb 2026 21:33:43 GMT  
		Size: 1.2 MB (1230202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211ce09ff20283e66f9f11918ceb7eba3e60efcc291b1309e5a881f7e15d422f`  
		Last Modified: Thu, 12 Feb 2026 21:33:44 GMT  
		Size: 8.3 MB (8258989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6791acce429a59d6b5990370a59bf72f4c34d9f6e3758c2293faaef7c0a2bed0`  
		Last Modified: Thu, 12 Feb 2026 21:33:44 GMT  
		Size: 1.4 MB (1398234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88bb109baae3c2a29ca44039528260593f1f171f2cc4343840ed8ec3fd86d0bc`  
		Last Modified: Thu, 12 Feb 2026 21:24:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052607a3a65ff6fca8c9ec9f792b6efc4aa2caad6e432cf99e962bd0cd676740`  
		Last Modified: Thu, 12 Feb 2026 21:33:45 GMT  
		Size: 3.1 KB (3145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3518c6f43cad6445663211691271a0814a9f6d38343a1c2ee0d16a616739ad16`  
		Last Modified: Thu, 12 Feb 2026 21:49:25 GMT  
		Size: 124.3 MB (124311309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ef03a01bae72e2b4e297db8cd41979f7ed262c9d438cae3141d36a4e1f5a94`  
		Last Modified: Thu, 12 Feb 2026 21:49:23 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d0f6a7c1c806a4696aa333942b85e0ec103b449684e29eab76438deafeab70`  
		Last Modified: Thu, 12 Feb 2026 21:49:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e925ed1591f8626fdf0c3791bbc4f2b9d825e41d3dcd9b75e8cb0fecc84151a`  
		Last Modified: Thu, 12 Feb 2026 21:49:23 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c85cefc2ccd274a82e9a2ed400c2facbddbc00fad62ea0c56bb856c420dfb3d`  
		Last Modified: Thu, 12 Feb 2026 21:49:24 GMT  
		Size: 5.8 KB (5841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abff1d0f98e492452bdae1ccec9caf569208b5168c078cf6be7d402cc5530ca2`  
		Last Modified: Thu, 12 Feb 2026 21:49:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:5ef7e6585f783350e453ae7a1f105c3d3ade6236d777ab41998923daba359f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11168e646fd83e585003f76c2f4489441dc083d8922d778a1b86ff023fcc2a2d`

```dockerfile
```

-	Layers:
	-	`sha256:6f4c85d5c5891a12751efd8848588048f8ec06e640be95b2aa5ddf2dfeb39df8`  
		Last Modified: Thu, 12 Feb 2026 21:49:23 GMT  
		Size: 5.6 MB (5610114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfd5c611e8d65f9818e92d7acd8e2049e5ee2df8ffb5f538de43df5db34625da`  
		Last Modified: Thu, 12 Feb 2026 21:49:24 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json
