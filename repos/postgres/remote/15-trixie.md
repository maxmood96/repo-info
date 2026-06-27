## `postgres:15-trixie`

```console
$ docker pull postgres@sha256:3b0d656f5fff31c7d8a64f500a703dcf3f35e98ce78f602831a73059a5e6a012
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

### `postgres:15-trixie` - linux; amd64

```console
$ docker pull postgres@sha256:6ab12ad4395ee49ab49fe19530f7e183c5a9c97fc47cf687b3e281bec5f91ee4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158088475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c897be1d0cc67e81272660c9af09d0a21add664036ab144b4f9fc6b35af06df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:33:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:33:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:33:39 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:33:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:33:43 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:33:43 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:33:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:33:47 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:33:47 GMT
ENV PG_MAJOR=15
# Wed, 24 Jun 2026 01:33:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 24 Jun 2026 01:33:47 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Wed, 24 Jun 2026 01:33:59 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:34:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:34:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:34:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 01:34:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 01:34:00 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 01:34:00 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:34:00 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:34:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:34:00 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:34:00 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:34:00 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c76fda38addaff47184c4b74f6fbce9d3cefce2d6660ef100ca10d27e22e09`  
		Last Modified: Wed, 24 Jun 2026 01:34:15 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e26febf095361f33992388b20275b445d7095303862415d9e98a1328c2568a`  
		Last Modified: Wed, 24 Jun 2026 01:34:19 GMT  
		Size: 6.4 MB (6443007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb73b0851f19862102f6c3004131ce68fc72c43ae83b7c1f12711686f2d1a81`  
		Last Modified: Wed, 24 Jun 2026 01:34:18 GMT  
		Size: 1.3 MB (1256768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2f93082245bb51e120e4251146f9cb40e0d826203fa0a0be110d52e339eaf8`  
		Last Modified: Wed, 24 Jun 2026 01:34:19 GMT  
		Size: 8.2 MB (8203887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6155ae5ef8f2315c7a98d111aef58b9dabe95b677498942e5c03d0ac3b237`  
		Last Modified: Wed, 24 Jun 2026 01:34:19 GMT  
		Size: 1.3 MB (1311608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e089b4b16146533a1de18db5915952f153f1078169fac6a97397e446d41513c1`  
		Last Modified: Wed, 24 Jun 2026 01:34:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd2ba93954ad62fe409badb962cd8f1fec3b3fbb047da3efdad0569452e4db4`  
		Last Modified: Wed, 24 Jun 2026 01:34:20 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812a8e197711e4df4ed48cc3ee16c666959ac840fa82bd71531ade8feb568311`  
		Last Modified: Wed, 24 Jun 2026 01:34:23 GMT  
		Size: 111.1 MB (111066903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86237adaf9e94c77a451ca746eb2b734e32be601f9ff049bb76a9193412e844`  
		Last Modified: Wed, 24 Jun 2026 01:34:20 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055beb516cf601cbe01bdfb876e987ead72c372fbe6f207e5fe6908d37ab622`  
		Last Modified: Wed, 24 Jun 2026 01:34:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ed54b206b0a74b715a3be130db2e230eaeda275dd29de98bbe63676debd5f5`  
		Last Modified: Wed, 24 Jun 2026 01:34:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c96c0be41fc792e66e8e0641505beb6a329788ee6783738ba872e34bc78df`  
		Last Modified: Wed, 24 Jun 2026 01:34:22 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aa476d8eeea9da2f31e6ea8da8d91ded3e77e71f5daee1b08c8435b554d24a`  
		Last Modified: Wed, 24 Jun 2026 01:34:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:9bcbd1ac66df21e85920817a77dc3b86846f145896e17ebffd1c95f551eebcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5696568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9e08ca08ede1c843802514573289e90acd3d6b282592a7b0cc27fca4a55e5d`

```dockerfile
```

-	Layers:
	-	`sha256:7ea8d4677b76a03dec35b472c1cda380dd12a070333cc1151277b4bbfea490e2`  
		Last Modified: Wed, 24 Jun 2026 01:34:19 GMT  
		Size: 5.6 MB (5642704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a71141989d15bd43184da21fd6026a531cc86a11c86824fc238e0032b67667`  
		Last Modified: Wed, 24 Jun 2026 01:34:19 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v5

```console
$ docker pull postgres@sha256:1a2e75738edfaf677ad1bfa654d913bf0c7d86c68b671c17918cc7e4ce277741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152116515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38090fdd2ce31a5f1075d5ff320382953ac12a73f2f95ba37fbb42259379f4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:56:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:56:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:56:29 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:56:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:56:38 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:56:38 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:56:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:56:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:56:46 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:56:46 GMT
ENV PG_MAJOR=15
# Wed, 24 Jun 2026 01:56:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 24 Jun 2026 01:56:46 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Wed, 24 Jun 2026 02:13:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 02:13:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 02:13:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 02:13:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 02:13:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 02:13:17 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 02:13:18 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:13:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 02:13:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:13:18 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 02:13:18 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 02:13:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e1a655938ebf253e2ae1439c4772703f1647cd1068fab506ffd9a7bc52981f`  
		Last Modified: Wed, 24 Jun 2026 02:13:36 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b484fbe27983dcd5809d750ec277cd511f4ea95941c56e33f83c2adba2af8f51`  
		Last Modified: Wed, 24 Jun 2026 02:13:37 GMT  
		Size: 5.9 MB (5932389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eedd87c50f58bfae4a7c554172906e4f5ce3616e092269e610b2e14858a5b98`  
		Last Modified: Wed, 24 Jun 2026 02:13:36 GMT  
		Size: 1.2 MB (1227568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af038c51d9a7936056ae349cda53c03d92b6472b2975de1840bc6cc0128ed185`  
		Last Modified: Wed, 24 Jun 2026 02:13:37 GMT  
		Size: 8.2 MB (8204327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85c41973d6ba3dbc205523d7d836da9f479dd2502d1231f99b679a03e328ba9`  
		Last Modified: Wed, 24 Jun 2026 02:13:38 GMT  
		Size: 1.3 MB (1317342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75752772d1e51aec65fc399fda94059f59eabd35a12c6c4b4ee0262e3bc7f88`  
		Last Modified: Wed, 24 Jun 2026 02:13:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15be8f9126d8c92d401cd5187dbddc19981810d6a1325e5276f9aafc7c9f44a2`  
		Last Modified: Wed, 24 Jun 2026 02:13:38 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e19e4c086cfe8fa50a2f6c389f2934b0a71a515dd1cbc2f6972d651391ddb0`  
		Last Modified: Wed, 24 Jun 2026 02:13:44 GMT  
		Size: 107.5 MB (107454786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5d6634b327be0e178ad51935f66d7d079d7d31643fe37ac28c0141166b2141`  
		Last Modified: Wed, 24 Jun 2026 02:13:39 GMT  
		Size: 9.9 KB (9881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ec957ce88cd5ed564618f5be30d527579b385dbe61fe80968b4759af894bfc`  
		Last Modified: Wed, 24 Jun 2026 02:13:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe4e1ae729b34561d32ea720be9bde176f281cc8fdd0ecdde7a451ca41db033`  
		Last Modified: Wed, 24 Jun 2026 02:13:40 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940389bcebf21d37ccb01066e1237b70783b7040ccfa68401a27c330cfecd4a3`  
		Last Modified: Wed, 24 Jun 2026 02:13:40 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec5135f104432f946a458f9b74e331662ea949b42fde69711ee70296306d1ec`  
		Last Modified: Wed, 24 Jun 2026 02:13:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:4e69805376f9e5529a11784ed88b0eaa20139d3440642582354430cae1cd83c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fe77e7411b947af33b13fd56e619c97bfc9973be43a03ac17f3085a309f5bb`

```dockerfile
```

-	Layers:
	-	`sha256:ead15b76561d2009e710d7bfd5be342965e5a4aad5f3cc5b245d6db48aad836f`  
		Last Modified: Wed, 24 Jun 2026 02:13:37 GMT  
		Size: 5.7 MB (5659346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b30d0967558a5e0d22d19c51e3d0c7a5ea2ea54f5cb8c0e1b781fa57e722d35c`  
		Last Modified: Wed, 24 Jun 2026 02:13:36 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm variant v7

```console
$ docker pull postgres@sha256:cbae19bde4665002cc3504c6d30ca097df4a4842e6bdb9950838a9a418a1f896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147171638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6023b333e7ced07b3e5042fe71022d69f95dfcbe6fc371ba128bab88b4d410f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:09:15 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 02:09:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:09:32 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 02:09:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 02:09:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 02:09:39 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 02:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:09:44 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 02:09:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 02:09:44 GMT
ENV PG_MAJOR=15
# Wed, 24 Jun 2026 02:09:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 24 Jun 2026 02:09:44 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Wed, 24 Jun 2026 02:24:26 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 02:24:26 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 02:24:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 02:24:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 02:24:26 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 02:24:26 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 02:24:26 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:24:26 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 02:24:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:24:26 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 02:24:26 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 02:24:26 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca1aecf423d1eaedb93b2942e2f5387a4522cad4b1ad58792fe97623766cfac`  
		Last Modified: Wed, 24 Jun 2026 02:24:43 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f85a86d6dc20af31cc7586c348f34df41ad90758445d202f9313d90f2db00a`  
		Last Modified: Wed, 24 Jun 2026 02:24:44 GMT  
		Size: 5.5 MB (5497393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bf6afc7395f8e93a24fc4ccd79d21f36eaaced64fae3ba15219cd78feaf6f1`  
		Last Modified: Wed, 24 Jun 2026 02:24:44 GMT  
		Size: 1.2 MB (1222462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f951ba4cd745b2bcb761af1ca8ffa0435fa8432bee37386193a07fe18bd48508`  
		Last Modified: Wed, 24 Jun 2026 02:24:44 GMT  
		Size: 8.2 MB (8204109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f965060737850054f4599d0f69b571cb1b5353372e284e3b0e2c2bda84a829`  
		Last Modified: Wed, 24 Jun 2026 02:24:45 GMT  
		Size: 1.2 MB (1172658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11e5942a8aeb2139a7ffc90e86a4fd26773e556475b64c8e16ad584629d4a00`  
		Last Modified: Wed, 24 Jun 2026 02:24:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83e97313b804f42bfcaee61f9521fcfc4f195608e9cf3c5524162e2cd94978a`  
		Last Modified: Wed, 24 Jun 2026 02:24:45 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e6433bae77b48fcf1a560cf504232617c9997ac75e5b21d189fcb1a77111e2`  
		Last Modified: Wed, 24 Jun 2026 02:24:48 GMT  
		Size: 104.8 MB (104843069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893c3d24a71c2764cf278c520f8e75b53248885592b734448688f9664313694e`  
		Last Modified: Wed, 24 Jun 2026 02:24:46 GMT  
		Size: 9.9 KB (9895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd96fdd2d8c44a297e8a10284a096331c38a9e3fee89136874091577edc0a31e`  
		Last Modified: Wed, 24 Jun 2026 02:24:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa3ea706cb9d799153960235069ef8e023a3bff44cce975b64415cc26eda41a`  
		Last Modified: Wed, 24 Jun 2026 02:24:47 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70db2f628de0302d032c982c138e2dba0d13e876677afbfb2e166eb7085d766`  
		Last Modified: Wed, 24 Jun 2026 02:24:47 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39d2c602d79c74b4b4f503839a2ec04c21f23cec2b57db4c2556da4df0c496e`  
		Last Modified: Wed, 24 Jun 2026 02:24:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:9a1fd17467eed18345aed7ebd30293282a6e312415c897b309234a81ba3604b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5712738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d556d4a73719ef87b6cfb548720b3434073054379636d53a7a0275fd18d643e`

```dockerfile
```

-	Layers:
	-	`sha256:2b1ec41aeffd5568444603f3aff68af794bcf938413283c8574133f34995c91f`  
		Last Modified: Wed, 24 Jun 2026 02:24:44 GMT  
		Size: 5.7 MB (5658651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55b77f112a1ea99af421a3e8efd46f6f939c361c71e320c007947679728e51a5`  
		Last Modified: Wed, 24 Jun 2026 02:24:43 GMT  
		Size: 54.1 KB (54087 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:0b1022a07ed77e09af42ca3f1ccb284be1926c5bb258f0e8469eee0a001a89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156715098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675cbfdb612f6138f4d3ae94d546a311bf5d61d3172a7371601889daf5e1f218`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:34:33 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:34:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:34:46 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:34:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:34:51 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:34:51 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:34:55 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:34:55 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:34:55 GMT
ENV PG_MAJOR=15
# Wed, 24 Jun 2026 01:34:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 24 Jun 2026 01:34:55 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Wed, 24 Jun 2026 01:36:02 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:36:03 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:36:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:36:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 01:36:03 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 01:36:03 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 01:36:03 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:36:03 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:36:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:36:03 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:36:03 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:36:03 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984fde83aabd68afa22e905d25a6089a433fae9fa6bb22a294280f74cd47bde5`  
		Last Modified: Wed, 24 Jun 2026 01:35:38 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7811ac9c53626821d5efdab21e9feb9a897d9886e008bc44c0530dc19d158c55`  
		Last Modified: Wed, 24 Jun 2026 01:35:39 GMT  
		Size: 6.2 MB (6235088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02469ff3041d518ea56a335104c2c52a8b1fbc36d29a226fbd0b040a35a21ab9`  
		Last Modified: Wed, 24 Jun 2026 01:35:38 GMT  
		Size: 1.2 MB (1209605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3641aa2c0bf3bbc7d4689c8698f8b5405e15e1f2b26436367245913d5b290032`  
		Last Modified: Wed, 24 Jun 2026 01:35:38 GMT  
		Size: 8.2 MB (8204026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f2d8f08e720f7f3c246aa20e1b6697057bc67007accdc7cb3cd09aafc70555`  
		Last Modified: Wed, 24 Jun 2026 01:35:40 GMT  
		Size: 1.2 MB (1220586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fdb1fc8bc8b198f642d5d86a64e39ac2686cf0c11831a2e12728f1757fa0ab`  
		Last Modified: Wed, 24 Jun 2026 01:35:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36c7db37db274fc63aa3cd0370be584072a18eb63cd8e5ca2d90ac83732755c`  
		Last Modified: Wed, 24 Jun 2026 01:35:40 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c8c66b53c2af8511d323df7e7e528ab58075ade5b478c38293d259dfb28458`  
		Last Modified: Wed, 24 Jun 2026 01:36:24 GMT  
		Size: 109.7 MB (109676350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85cfd63765a9c49df699d942880b9697be6b282de5c9bd013e4121160e4d0ba`  
		Last Modified: Wed, 24 Jun 2026 01:36:21 GMT  
		Size: 9.9 KB (9890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31a1fb43697b8be6ccc6cfb21a97e7bd1ed2909f0ef10fed36659116328e48a`  
		Last Modified: Wed, 24 Jun 2026 01:36:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ed2d6eb31333d8b62a472bce8cc1417ddb932b11a54db179d18259ab80c172`  
		Last Modified: Wed, 24 Jun 2026 01:36:21 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b7e3d9413941ca544d63c5a41dd2e750151bccf68b3e27e76e754c0f534631`  
		Last Modified: Wed, 24 Jun 2026 01:36:23 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a76ddba63ff717460689d39272b85b0d42d34c944203d29f88b8b98ef1ce8c2`  
		Last Modified: Wed, 24 Jun 2026 01:36:23 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ad7a9d65e38dbedae729492681623aeb8d345e431b86d6c70d571f5840961fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a625e9343ccb49bcfc7acb07c1c8ab4bf257a6607b5f1c942b4a06cacca3c40`

```dockerfile
```

-	Layers:
	-	`sha256:7292cd29c60c0fa5d8b8d4998959d778d04c5b3e6639cf38d928ff6734faa0b3`  
		Last Modified: Wed, 24 Jun 2026 01:36:21 GMT  
		Size: 5.6 MB (5649042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93df50bc0209adb6c2ccc83d248c8fd52db830946da129e68abb417de56f4e44`  
		Last Modified: Wed, 24 Jun 2026 01:36:21 GMT  
		Size: 54.1 KB (54133 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; 386

```console
$ docker pull postgres@sha256:bf8d297d55bee51b468b60afe0cdad5ce89174be5d99827be6cc723ad16a2ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167186890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e494c178a801a2601e417952faf0827aa3773a434efa1ca47791b1926a47ff48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:32:20 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:32:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:32:35 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:32:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:32:40 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:32:40 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:32:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:32:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:32:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:32:45 GMT
ENV PG_MAJOR=15
# Wed, 24 Jun 2026 01:32:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 24 Jun 2026 01:32:45 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Wed, 24 Jun 2026 01:44:09 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 01:44:09 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 01:44:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 01:44:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 01:44:09 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 01:44:09 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 01:44:09 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:44:09 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 01:44:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:44:09 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 01:44:09 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 01:44:09 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdf686e4235f8623391dc3a3e0288631e2f3cb310f403aa3c1b4a2ff5cb192d`  
		Last Modified: Wed, 24 Jun 2026 01:33:16 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa5cbeaba06f5b76cfa9625b3384706c661e6f699bb2c7fa3fe8437e04ba03a`  
		Last Modified: Wed, 24 Jun 2026 01:44:30 GMT  
		Size: 6.6 MB (6631469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d003af83614c3db87973320b081f5a1015887d734d292b6a5f4c6ad35bd559cf`  
		Last Modified: Wed, 24 Jun 2026 01:44:30 GMT  
		Size: 1.2 MB (1225860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5625ef8da96321f417b097b5c5f25e24dece8057af0bc2cff86e55991299ec6`  
		Last Modified: Wed, 24 Jun 2026 01:44:30 GMT  
		Size: 8.2 MB (8204083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e206b88bde192adec926189489fba648abfda618d014679e7d144ebab7961a`  
		Last Modified: Wed, 24 Jun 2026 01:44:30 GMT  
		Size: 1.3 MB (1308279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6229aac93a9ab1036fd637147c3ce694a11eff9d9b9bb66f14c41fb3cd3f6bcf`  
		Last Modified: Wed, 24 Jun 2026 01:44:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852d19141bcd624523a0970a3a690d1396e323d34703165add0c46241135aaaf`  
		Last Modified: Wed, 24 Jun 2026 01:44:31 GMT  
		Size: 3.1 KB (3140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b0b39444e5c0576fa3f01bf6fd0fb5c66f705321506e37d8344185ae3e1c74`  
		Last Modified: Wed, 24 Jun 2026 01:44:34 GMT  
		Size: 118.5 MB (118495105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef08e5470156b8fe5d229a704ab4d907773bb21b4c8359acf3d2ee5941f0f4e`  
		Last Modified: Wed, 24 Jun 2026 01:44:32 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6caebf346602fbae7c6b2b6a8eac80c577085aed65b70d1a69d96d0bd9a644e`  
		Last Modified: Wed, 24 Jun 2026 01:44:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f1a294c939a21bdfbe535531c112667f00aa6b35d2a4daa79138c73a284db5`  
		Last Modified: Wed, 24 Jun 2026 01:44:33 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d830abb6bf3cea10240cc559be9a4b0074ba13e482a5b27d38d00dc19fbbee`  
		Last Modified: Wed, 24 Jun 2026 01:44:33 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53779bedb97da06894bcec38642d42fc40b0484122b8e096af85656a23c5d1ce`  
		Last Modified: Wed, 24 Jun 2026 01:44:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:1438f6c2798d297065a7b003e987016511e4a20bdef12fa4467d0484f9956ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5712049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30636b61bb96f4f45e44ad5cce29ac6c57bc793ea2e782961c22e58d172a6821`

```dockerfile
```

-	Layers:
	-	`sha256:145b6d158bd6a0c86dde17ad29982b48230cfbe3e5d997047f239922b921de56`  
		Last Modified: Wed, 24 Jun 2026 01:44:30 GMT  
		Size: 5.7 MB (5658239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a586aaf43fc3b72d48b29069688d4778be5856106b650e2d2705c5b5c4b9e1a`  
		Last Modified: Wed, 24 Jun 2026 01:44:29 GMT  
		Size: 53.8 KB (53810 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; ppc64le

```console
$ docker pull postgres@sha256:b287d47fed4ede0d015889a0974b2bb673a23e5240565a2fba3c37558bd29026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170336612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9841c7e32498ec5bbb749859a5b156b9248ef0453cc6b24dc7253cc8a6ee57f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 03:02:27 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 03:02:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:02:55 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 03:02:55 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 03:03:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 03:03:05 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 03:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 03:03:21 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 03:03:21 GMT
ENV PG_MAJOR=15
# Wed, 24 Jun 2026 03:03:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 24 Jun 2026 03:03:21 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Wed, 24 Jun 2026 03:11:03 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 03:11:04 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 03:11:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 03:11:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 03:11:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 03:11:05 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 03:11:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:11:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 03:11:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:11:06 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 03:11:06 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 03:11:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986ec99518a807bfad5f7f46ab0d7169e6bb8464c56530a6857da4833bcf42a0`  
		Last Modified: Wed, 24 Jun 2026 03:04:48 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b235d4ec390c403864dac84f73f8717b274ee67ad58efd50aa20676e32950ab`  
		Last Modified: Wed, 24 Jun 2026 03:04:49 GMT  
		Size: 7.1 MB (7076761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097461e8a5ef2da1a84e8b66d0907cb5d87f6f558b864dbccab0f456fe833694`  
		Last Modified: Wed, 24 Jun 2026 03:04:48 GMT  
		Size: 1.2 MB (1214756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38e02605252f06f6ad4fd846fa34fd2c8bfce121536074a31620b544092b0a1`  
		Last Modified: Wed, 24 Jun 2026 03:04:49 GMT  
		Size: 8.2 MB (8204060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5c026a4459463a6e5145ad624a4164b37786a4e4dd7bf9759e4e855d64bcc3`  
		Last Modified: Wed, 24 Jun 2026 03:04:50 GMT  
		Size: 1.4 MB (1394880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566c45b1c57ad093b48578c726e36fc3978d088b4357bba48905f926320f23c0`  
		Last Modified: Wed, 24 Jun 2026 03:04:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2db7823b7c0860e15b3f9662e8a0370ef70f939cbbb9d59e62f37739e85d1cc`  
		Last Modified: Wed, 24 Jun 2026 03:04:51 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e92a395095dfd879f44ef624e7239fa31d81c7cbc8d097f79eb50427c8191b`  
		Last Modified: Wed, 24 Jun 2026 03:11:49 GMT  
		Size: 118.8 MB (118818880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f78e072ffdc36dbc4e4844f94d481755ddd8d26dd48a94aeb497276f428fa`  
		Last Modified: Wed, 24 Jun 2026 03:11:46 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da50732c7e39935cffcd1ccfbe37e551f24836d433eecebd936372516d5f762f`  
		Last Modified: Wed, 24 Jun 2026 03:11:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa2af09cda71bbb08fb6b82ed17130e9fd6bd31a25897d800a60db80547804d`  
		Last Modified: Wed, 24 Jun 2026 03:11:46 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8cfa0f4e69ecddc8f0748f67ecaa4069bfdcd467791b1a97a5c1a9ce114b98`  
		Last Modified: Wed, 24 Jun 2026 03:11:47 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6a9a86cfc32edf7e763d02de8f593df2a06c11ad8355c2847861d922f92a43`  
		Last Modified: Wed, 24 Jun 2026 03:11:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:448e2795d452f8afce54d8b3276293aaef539417f9d979971532d1f9af4f8290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1b6da1a5a653c1891e1d9d804df5a83de7b7f80e5a0178e4fe42b9f737618a`

```dockerfile
```

-	Layers:
	-	`sha256:0c4be2ab0ee146ef9125ad3062e08d537acda435ee7f3e848d6dcb3124bf1d97`  
		Last Modified: Wed, 24 Jun 2026 03:11:46 GMT  
		Size: 5.6 MB (5649317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:419c4f1c5065e2a09c4966b040ed9195238ace6603c45edced93f8e699b3f924`  
		Last Modified: Wed, 24 Jun 2026 03:11:45 GMT  
		Size: 53.9 KB (53930 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; riscv64

```console
$ docker pull postgres@sha256:29bdec88ad6b210674921ecacdfa978da2515ed7839c9b2a539a9201d3fb12d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90031649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56c4eecea7bb8e741ec6965b7eaf71a3c9a36a403ca6bcd68cf6b31c2822198`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Thu, 25 Jun 2026 17:20:07 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Thu, 25 Jun 2026 17:21:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 17:22:04 GMT
ENV GOSU_VERSION=1.19
# Thu, 25 Jun 2026 17:22:04 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 25 Jun 2026 17:23:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Thu, 25 Jun 2026 17:23:05 GMT
ENV LANG=en_US.utf8
# Thu, 25 Jun 2026 17:23:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 25 Jun 2026 17:23:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Jun 2026 17:23:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 25 Jun 2026 17:23:49 GMT
ENV PG_MAJOR=15
# Thu, 25 Jun 2026 17:23:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Thu, 25 Jun 2026 17:23:49 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Sat, 27 Jun 2026 09:32:44 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Sat, 27 Jun 2026 09:32:45 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Sat, 27 Jun 2026 09:32:45 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Sat, 27 Jun 2026 09:32:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 27 Jun 2026 09:32:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Sat, 27 Jun 2026 09:32:46 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 27 Jun 2026 09:32:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Sat, 27 Jun 2026 09:32:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Sat, 27 Jun 2026 09:32:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jun 2026 09:32:46 GMT
STOPSIGNAL SIGINT
# Sat, 27 Jun 2026 09:32:46 GMT
EXPOSE map[5432/tcp:{}]
# Sat, 27 Jun 2026 09:32:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adbcc74bc464c350395b0ed6c1768df2fe221b068feb6158693ad4ec07cd00e`  
		Last Modified: Fri, 26 Jun 2026 19:26:26 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34ed43918633e51bd4b0dfe515e8421bf7b4d99c7a97135953368b017f8e34f`  
		Last Modified: Fri, 26 Jun 2026 19:26:28 GMT  
		Size: 6.3 MB (6293016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75577e804f36a67f7f9edf858af5711ac30d48485a836696cb03b019ecd36ac3`  
		Last Modified: Fri, 26 Jun 2026 19:26:26 GMT  
		Size: 1.2 MB (1202088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7531413cc31124ad057b4194a1eb2086a683b6b4d169970cf67852cdf74c7eb`  
		Last Modified: Fri, 26 Jun 2026 19:26:29 GMT  
		Size: 8.2 MB (8203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f9b21c12f76de08f6c105f2b2e8ba8d94e03c0a18063b3314a7d36fd79db64`  
		Last Modified: Fri, 26 Jun 2026 19:26:28 GMT  
		Size: 1.4 MB (1402395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f5cd849b9c5cab9341c5d47ce0147c065a4a959e62f1844d1fa79d44437dd3`  
		Last Modified: Fri, 26 Jun 2026 19:26:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4834cab7a2c6eca063fcf59846c4f1194e5de56dcc92340991a3bbb7949a5b83`  
		Last Modified: Fri, 26 Jun 2026 19:26:30 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4535fadeda562ce5f78a72af41fcca97758dab202647f96b1f981403e5dbc8`  
		Last Modified: Sat, 27 Jun 2026 09:35:18 GMT  
		Size: 44.6 MB (44627108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569dd325548e20b06c52a8999155f1879cc540ca41449348b01b8d805a49429a`  
		Last Modified: Sat, 27 Jun 2026 09:35:11 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400e9807e36171653693fb0f582b9ab9159202af82c8f98d9cf9db156e600846`  
		Last Modified: Sat, 27 Jun 2026 09:35:11 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7015f10c71b5ddbbca5c530fb7762eb3fbdf8780eb3d435ce8f769f23d7e120`  
		Last Modified: Sat, 27 Jun 2026 09:35:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceac7079c3d6c5ff8abea542d1e47fcc0268ae0ce398ebde9e97d7c991aad50e`  
		Last Modified: Sat, 27 Jun 2026 09:35:12 GMT  
		Size: 6.1 KB (6102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c47dea839a42e2969e3add4990a0865e9e78671158842bb7b2b5b25ef01d7`  
		Last Modified: Sat, 27 Jun 2026 09:35:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:ea7ea13220ebaa0d528be40a947e7f8e6fd313ce9029d3d1ba04afb3d44a2737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507dbbfb1b7c63b5afb826e8eff4a9f48451ae728043520e206b1c411306a25d`

```dockerfile
```

-	Layers:
	-	`sha256:979dacfec69157b074ef31c64c4a1f05658a22397c9327d776d5949a42146bbd`  
		Last Modified: Sat, 27 Jun 2026 09:35:11 GMT  
		Size: 5.0 MB (5020754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8900a29b083997c52d41dc9758d33196d012903e783756db08e8926813f7c2d3`  
		Last Modified: Sat, 27 Jun 2026 09:35:10 GMT  
		Size: 53.9 KB (53924 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-trixie` - linux; s390x

```console
$ docker pull postgres@sha256:206e4f74a986b7a864662a619f1695e54b20b3c45caf81ef46c4f385b8645767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172615941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0e65233d10f392d06d1e2c0b0b685c576995ca2a3fd13d641f1b8510ea6822`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:57:59 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 24 Jun 2026 01:58:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:58:12 GMT
ENV GOSU_VERSION=1.19
# Wed, 24 Jun 2026 01:58:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 24 Jun 2026 01:58:19 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 24 Jun 2026 01:58:19 GMT
ENV LANG=en_US.utf8
# Wed, 24 Jun 2026 01:58:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:58:23 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 24 Jun 2026 01:58:24 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:58:24 GMT
ENV PG_MAJOR=15
# Wed, 24 Jun 2026 01:58:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/15/bin
# Wed, 24 Jun 2026 01:58:24 GMT
ENV PG_VERSION=15.18-1.pgdg13+1
# Wed, 24 Jun 2026 02:39:39 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt trixie-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 24 Jun 2026 02:39:39 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 24 Jun 2026 02:39:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 24 Jun 2026 02:39:39 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 24 Jun 2026 02:39:39 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 24 Jun 2026 02:39:39 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 24 Jun 2026 02:39:39 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:39:39 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 24 Jun 2026 02:39:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:39:39 GMT
STOPSIGNAL SIGINT
# Wed, 24 Jun 2026 02:39:39 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 24 Jun 2026 02:39:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f8b3edc75b49ced11dab27f4148cad3479e0ca4d1bef3a3372749607386048`  
		Last Modified: Wed, 24 Jun 2026 02:13:10 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9af1a36d970a9aa144153569a33418a335c9f9fa39e21a0cc4822586b42480`  
		Last Modified: Wed, 24 Jun 2026 02:13:11 GMT  
		Size: 6.4 MB (6408505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67240597dd615f7661bbea5c29258b345c44ac1ab6bb6353553953f634b3b31c`  
		Last Modified: Wed, 24 Jun 2026 02:13:10 GMT  
		Size: 1.2 MB (1230274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe0ebce0cd5e64ec821f7bc63f955b565a014c44a3e15ddbf8fb5de3b298b72`  
		Last Modified: Wed, 24 Jun 2026 02:13:11 GMT  
		Size: 8.3 MB (8258957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b62f6fa5bb2b55a8c5023e16a41664043d46f4d418a482eb291c58f249ad3f7`  
		Last Modified: Wed, 24 Jun 2026 02:13:12 GMT  
		Size: 1.4 MB (1398189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e3b23c8c098994d89f5ec00fd029fe0265f484d55050145dd15dc6dc11ad6d`  
		Last Modified: Wed, 24 Jun 2026 02:13:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5a3c3534096eaaed44cd33e5dc26c06d3585042dbe09953547256135f24b66`  
		Last Modified: Wed, 24 Jun 2026 02:13:12 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2db2a7253d1d428cf12769ea0b6c2464efe023fbb74cc333ac7927647f1c4f`  
		Last Modified: Wed, 24 Jun 2026 02:40:13 GMT  
		Size: 125.4 MB (125447742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac3b87534e0d92b9bb3ccf4fbe9c61991e73c3b248366afd221125f53fb7f77`  
		Last Modified: Wed, 24 Jun 2026 02:40:11 GMT  
		Size: 9.9 KB (9888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225085a822663d87cb5058f18adb961a426a94b1178bce331cacb019ef1c0d3c`  
		Last Modified: Wed, 24 Jun 2026 02:40:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d9b6f57427f89f7f95baab01c954302bd417955e2305d17095742ff5e680a2`  
		Last Modified: Wed, 24 Jun 2026 02:40:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cceff0da09025fddd5c8c48f9eb9a4c8cdc3fdbcaedf3f15e4429d518a0f52`  
		Last Modified: Wed, 24 Jun 2026 02:40:12 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475cc5f0a2021d8fc42efda60f17d2caeef596dd8dc160e00034cbf9a5e93290`  
		Last Modified: Wed, 24 Jun 2026 02:40:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-trixie` - unknown; unknown

```console
$ docker pull postgres@sha256:3372c3a1c6089a461f815eb150c7b159dd3eb4423fb4cc4b256efd10e00d15e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9683e18f7fa4b0b68212f05b6a2f5ab336296ec51adbdd6dfbdf40c029816d4`

```dockerfile
```

-	Layers:
	-	`sha256:65644a94d3233a5abe45044e956cc11ab78d3184263155cf3128ce3907c0ce6c`  
		Last Modified: Wed, 24 Jun 2026 02:40:11 GMT  
		Size: 5.7 MB (5659377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4f076703b1173fcd024cf192287c666bc78300ac30ba01bb2d4f8c16bc447f`  
		Last Modified: Wed, 24 Jun 2026 02:40:11 GMT  
		Size: 53.9 KB (53864 bytes)  
		MIME: application/vnd.in-toto+json
