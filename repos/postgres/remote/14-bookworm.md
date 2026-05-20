## `postgres:14-bookworm`

```console
$ docker pull postgres@sha256:70b9c8977b5fb87bd55c9e29472d778d76d56a6266143d47259da13d78a72afa
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
$ docker pull postgres@sha256:5e34dc9c8d5473b012a8180b54cec26d150a8fdceefb1a1580bbef2cc79339f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151920970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073b0fd7fdad3bf5d91a6bf889ffdc34e4dfb587aea8470573f8dda6439a83b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:15:41 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:15:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:15:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:15:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:15:56 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:15:56 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:15:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:15:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:15:59 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:15:59 GMT
ENV PG_MAJOR=14
# Tue, 19 May 2026 23:15:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 19 May 2026 23:15:59 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Tue, 19 May 2026 23:16:55 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:16:55 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:16:55 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:16:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:16:56 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:16:56 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:16:56 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:16:56 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:16:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:16:56 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:16:56 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:16:56 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e682f392bdecf73bec731a2549e72bed22b5df207b8ac598a48eaa53cd20f89c`  
		Last Modified: Tue, 19 May 2026 23:16:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4774905b259895e87f4f347c856397d87e40ea2a45607dbd578b7aefdc719eb3`  
		Last Modified: Tue, 19 May 2026 23:16:33 GMT  
		Size: 4.5 MB (4534259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643e54c5943b6ff0482cce26a9208f6575d8007096f890355381c990d38e3154`  
		Last Modified: Tue, 19 May 2026 23:16:33 GMT  
		Size: 1.2 MB (1249566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa561da32d905c574ed4b6924ce8fb907c8b8f1cb52ee7ea931920a197084ded`  
		Last Modified: Tue, 19 May 2026 23:16:34 GMT  
		Size: 8.1 MB (8066417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8856edf487c2d9a75a2a6edda2182ee000f41a6be0a346c5d2c49d8019417df0`  
		Last Modified: Tue, 19 May 2026 23:16:34 GMT  
		Size: 1.2 MB (1196406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef90fbefae529be0694ed44fcdf035ae1c806b95dffeb82b97a6d0f4bfe16722`  
		Last Modified: Tue, 19 May 2026 23:16:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfbcf8da7b0340a9993ae68cf8479089b850f865019d1811186f7e410cb9be9`  
		Last Modified: Tue, 19 May 2026 23:16:35 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9cb42f01a1458c30a9180010f6a7817f857fc97a6e0616c409c91f4e60dc21`  
		Last Modified: Tue, 19 May 2026 23:17:17 GMT  
		Size: 108.6 MB (108620254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bb8e3366361fe6f71cb6c44dcfdc3d2cd42258fddb11f8fef656ab2b665780`  
		Last Modified: Tue, 19 May 2026 23:17:14 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eef7393de24780df7e8f2a448f952814b2315ec9bf3b8d7ff3013f44bf03a39`  
		Last Modified: Tue, 19 May 2026 23:17:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0b28ecac91b3f35d9e3dbd2e82d615a68e3343be0b057b49e51cf1b41d5521`  
		Last Modified: Tue, 19 May 2026 23:17:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c09d9cb0dc8d3ef5b4ecc84f3444e9871c7b4101d93e746eb3ea8c1a15928b`  
		Last Modified: Tue, 19 May 2026 23:17:15 GMT  
		Size: 6.1 KB (6096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c70f537ef2734c595bdcb3599bc2c78e58e4a008643e759831fc4ee9d2b26a`  
		Last Modified: Tue, 19 May 2026 23:17:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:06e3d1268fc2f803baab5a2aa76db243a3000871ef15c062dea9356d03c750a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5847590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d5aa24e7a4116cd47aa72b5d79b079093ce3e9c5cfde7bee70f6f75a2ec365`

```dockerfile
```

-	Layers:
	-	`sha256:c1e5265fbc951d2e238c3699efedb9b04c4cfb4ffc69e23035d3be4a58b8cea9`  
		Last Modified: Tue, 19 May 2026 23:17:14 GMT  
		Size: 5.8 MB (5794295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80882689bd3d6089f86bda9409196990f36cd6e941492ec04708bd455801bae9`  
		Last Modified: Tue, 19 May 2026 23:17:14 GMT  
		Size: 53.3 KB (53295 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:47a48fdab6eeb6ccc5f61c86f08758b6ecc51eb573974cd0ea76bb758469fc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144875448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8a528a16522a2f26400d1de72f71cd7c25ceb381b34e7e64c3b6742463e248`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:41:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:41:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:41:35 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:41:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:41:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:41:42 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:41:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:41:47 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:41:48 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:41:48 GMT
ENV PG_MAJOR=14
# Tue, 19 May 2026 23:41:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 19 May 2026 23:41:48 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Tue, 19 May 2026 23:56:00 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:56:00 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:56:00 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:56:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:56:01 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:56:01 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:56:01 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:56:01 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:56:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:56:01 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:56:01 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:56:01 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95d0b744f76ccc2c099ef63703820197559e4d2142b971ca67d8d34f9c018e3`  
		Last Modified: Tue, 19 May 2026 23:56:19 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879a44d4312d84d7c366e12a2caad167cacce03f54194e00158ef78666010a24`  
		Last Modified: Tue, 19 May 2026 23:56:19 GMT  
		Size: 4.2 MB (4151302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e4dcaae015d1905aa6d27548386e8800fdf1bd0048f17c3ed899282a7a26c3`  
		Last Modified: Tue, 19 May 2026 23:56:19 GMT  
		Size: 1.2 MB (1220127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ffb57ce71739b2a5e8be4ece5d107fcb288f9000ea0c5b04f70fcbaff6aeb5`  
		Last Modified: Tue, 19 May 2026 23:56:19 GMT  
		Size: 8.1 MB (8066554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2aa8cf637fa968e32183aa0985e6aab0d988c85ad903937cc67f6cae7c498`  
		Last Modified: Tue, 19 May 2026 23:56:20 GMT  
		Size: 1.2 MB (1195051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ea86fc587be9a3a5434af197cd88ab76617082b68d4d033c54b9eae60d8a76`  
		Last Modified: Tue, 19 May 2026 23:56:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e837db6dbdcbbde87284df84f1e6ff4b7ddaf2ad67b18de60451a0806e78e80e`  
		Last Modified: Tue, 19 May 2026 23:56:21 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a31dd1dedc0cd92b027ef5183e879f7ecb73b164cf01b310bffca86e4927065`  
		Last Modified: Tue, 19 May 2026 23:56:25 GMT  
		Size: 104.5 MB (104453582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fa13c32cf18e471208f6ca9ad6803637f5ca7d232dbc66a39a267f00009764`  
		Last Modified: Tue, 19 May 2026 23:56:22 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4e7d4e26714226af09a3cb20bc08e758bcfe8b4c3b17716f6d49d8726eeadc`  
		Last Modified: Tue, 19 May 2026 23:56:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48382541ca53b3243beef36d2d5e81c32d89591ebda7f29f0235eef450d1b2ed`  
		Last Modified: Tue, 19 May 2026 23:56:22 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14694cf9bdb05db636777f6804448e17953d568b9b21aa02eec8baa18b44cf09`  
		Last Modified: Tue, 19 May 2026 23:56:23 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e908601329ff80b0b0e3853d4052da1771462362d3496cee37a35fa217585d`  
		Last Modified: Tue, 19 May 2026 23:56:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:313f0a2e6e0b3549aa2e446ae6fd2f0a056059d8577ea6f90594b058155b0d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5863623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d1bea69df8dcbab0666bb2bdfa84b4a0a3557325772603d15ff6834398549a`

```dockerfile
```

-	Layers:
	-	`sha256:cfbb8c299de176d1f9c39fbe58a8984e2b7e43740fcce0ec975b19c52a9f9882`  
		Last Modified: Tue, 19 May 2026 23:56:19 GMT  
		Size: 5.8 MB (5810120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4cbda68b0c7e062aebd2a595ae4823f7014c1fbf354db78b137a87c95ce92e9`  
		Last Modified: Tue, 19 May 2026 23:56:19 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:43d79146c08fb2d7e44ba7552778237063d6999cfd9459d06812e7cbec33c6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139950356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f20f1983e0805e4f8f2468fa7b98c50d5a8f6093021df5e0a6f9fc05a94976`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:48:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:48:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:48:33 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:48:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:48:39 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:48:39 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:48:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:48:43 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:48:44 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:48:44 GMT
ENV PG_MAJOR=14
# Tue, 19 May 2026 23:48:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 19 May 2026 23:48:44 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Wed, 20 May 2026 00:02:46 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 00:02:46 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 00:02:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 00:02:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 00:02:46 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 00:02:46 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 00:02:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:02:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 00:02:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 00:02:46 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 00:02:46 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 00:02:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23a0b04207738c7ae1c60950efe40cf1af77b40f7bdbe6ad0cf1808c2408f34`  
		Last Modified: Wed, 20 May 2026 00:03:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c43e8e871624f82d2d487f6fbb7055f42937cfa29594850af736c45a3ececa`  
		Last Modified: Wed, 20 May 2026 00:03:04 GMT  
		Size: 3.7 MB (3742682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc7569dbb58a57b26dc35047deaa3e4bf069db065e7d3c1d6cf27a0392c4c73`  
		Last Modified: Wed, 20 May 2026 00:03:04 GMT  
		Size: 1.2 MB (1216011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742034559cf89398378aa3209938d683a2dcc77475ff0952d7bc126920e0320`  
		Last Modified: Wed, 20 May 2026 00:03:04 GMT  
		Size: 8.1 MB (8066394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77df6c51f07b90ebd5def69f93745da94b544674b194895fa662c7b368a5de6c`  
		Last Modified: Wed, 20 May 2026 00:03:05 GMT  
		Size: 1.1 MB (1067240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e911c8abd33c5472e03b7bef917ba45e8fa69726791ea3c13d159f5e1526dc`  
		Last Modified: Wed, 20 May 2026 00:03:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f600b5d725e775da1e1d1006b7f910f79663feec42fdad5535af13825560f4ec`  
		Last Modified: Wed, 20 May 2026 00:03:05 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e62ddb07df724e41c8a1a763efb6b2f327c372c0669f387f167df666f91419`  
		Last Modified: Wed, 20 May 2026 00:03:08 GMT  
		Size: 101.9 MB (101895845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceeb2368d0ad1cf84f638128208a89bb353cf632232daa5ae70a91ec5016c68c`  
		Last Modified: Wed, 20 May 2026 00:03:06 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c569b2fd1d854429cf1dcaa03c16601578c81b1f16ab6fa3ae08057372bb09`  
		Last Modified: Wed, 20 May 2026 00:03:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc2003512d2ef87cd67097fe5d6a2a2c69e6496cec92a11d550adfe60c2e3d9`  
		Last Modified: Wed, 20 May 2026 00:03:07 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02dabf1c65608e92fbe661be47f2565c78a9224764604f89b52b3e051e7aca46`  
		Last Modified: Wed, 20 May 2026 00:03:08 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e368bb1dbeb10e34719a2e51bb509997c7eaca334dae10dedae462a3f988b1c`  
		Last Modified: Wed, 20 May 2026 00:03:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ce388f505cfe7af546d5c6b6ad9280bccd0b7e7ae9e4cbb71b0de7a9e5db4357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5862878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66914b983d6ac1059ecaa1d8270e88ea872e8e783fb07d10a37c6f52f1dcbe83`

```dockerfile
```

-	Layers:
	-	`sha256:75fd736a838ec477e98fb89003f6f618ecb2052763e88bf2cf9e493fa6607d34`  
		Last Modified: Wed, 20 May 2026 00:03:04 GMT  
		Size: 5.8 MB (5809375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef1d8689a333afcb97748c1c26dfdfbd0a4b02c807f850d913834ca1d11c6b5`  
		Last Modified: Wed, 20 May 2026 00:03:04 GMT  
		Size: 53.5 KB (53503 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:fa9feba99a97e16b90c16168ce7b847c7005032d9a1b613a23e9baf32424c928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149939678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bba644d1ff5ea1cbfc59964e6a1f154b94c70171fedf27a2e3304a0ace2e8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:18:19 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:18:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:18:30 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:18:30 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:18:34 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:18:34 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:18:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:18:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:18:38 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:18:38 GMT
ENV PG_MAJOR=14
# Tue, 19 May 2026 23:18:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 19 May 2026 23:18:38 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Tue, 19 May 2026 23:19:34 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:19:34 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:19:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:19:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:19:34 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:19:34 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:19:34 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:19:34 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:19:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:19:34 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:19:34 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:19:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ac1c1fc1a6174be23efe805973f171a5048f6db151a550cfb351a08c1952aa`  
		Last Modified: Tue, 19 May 2026 23:19:09 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1b0144f589a6eff1121677cc4bb212543967395893151e85c80cfc6c7d635a`  
		Last Modified: Tue, 19 May 2026 23:19:09 GMT  
		Size: 4.5 MB (4519536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8b1834dd4f7a4dd8d6142137ee153a2a7a2565bc16894660259afacadd027e`  
		Last Modified: Tue, 19 May 2026 23:19:09 GMT  
		Size: 1.2 MB (1203298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7513b92dcb4577fae52494066b4c556a86e289988e016b4c50643969bcd4ea9f`  
		Last Modified: Tue, 19 May 2026 23:19:09 GMT  
		Size: 8.1 MB (8066473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3db376ecd51855e2bc31603a4f6f62c1f44328565f0608a3b0d6d9cd7f3fd97`  
		Last Modified: Tue, 19 May 2026 23:19:10 GMT  
		Size: 1.1 MB (1109039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c2157f25c5512156531cbc8eab7fec4f1a85cb5af79b8e0caa099fc6d1ad66`  
		Last Modified: Tue, 19 May 2026 23:19:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef0e398b2a830d64b993f5d82364de01ab216c46222b3fd1fb8d75d3067c7e3`  
		Last Modified: Tue, 19 May 2026 23:19:10 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eefded17f971902deea300738e82a2fa132c47dc97527e2064804462f0cb659`  
		Last Modified: Tue, 19 May 2026 23:19:56 GMT  
		Size: 106.9 MB (106905747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca00ff934b9fa3cb2510779b80404ae31bd58163f42c170b1d7e1f8130d1df8a`  
		Last Modified: Tue, 19 May 2026 23:19:52 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5beb76e5e3d9fc8c5daee161af7da156ad073b324e5c2b9765e00328e83dd224`  
		Last Modified: Tue, 19 May 2026 23:19:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed74a3f6f4dcfbb5feb0bba082dc18c9007f7e419f8d2e3fb4d86bd053460fc`  
		Last Modified: Tue, 19 May 2026 23:19:52 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67e9d677e3c19001952b2eee78724c04fce3769a434b18f8fa7c3ebab2deb37`  
		Last Modified: Tue, 19 May 2026 23:19:53 GMT  
		Size: 6.1 KB (6098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcd8052307243f85cb94d152a3bd94dd71da3bb7ba133407874c01ee87418b9`  
		Last Modified: Tue, 19 May 2026 23:19:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2ca666768485873023cf0a797273880a8189e45c54753a27970d1cc39a0b62ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5854147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a663150ca5561a2c59f6167b450bccd6bd3fd1f84c256ecdc5ea1839bf6b9e3`

```dockerfile
```

-	Layers:
	-	`sha256:2f5f7a0364494a8ac7e42881aff583c64ccde536d418153b99409e85f71ed60f`  
		Last Modified: Tue, 19 May 2026 23:19:52 GMT  
		Size: 5.8 MB (5800606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:277e869e8faa2c2ca1ce82a8b23d4549baa9b8f0e453499fd3b617a08b37b27e`  
		Last Modified: Tue, 19 May 2026 23:19:52 GMT  
		Size: 53.5 KB (53541 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:a37d740454e62684ffafeb97d9d0b186de8628e6f2d3957616eb9d261ee98157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160597843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fe0d39786a62de4f5e565c2e8a15d5ab2333b933d0ffea8a07650bed886650`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:15:26 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:15:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:15:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:15:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:15:42 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:15:42 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:15:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:15:45 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:15:45 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:15:45 GMT
ENV PG_MAJOR=14
# Tue, 19 May 2026 23:15:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 19 May 2026 23:15:45 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Tue, 19 May 2026 23:26:17 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 19 May 2026 23:26:17 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 19 May 2026 23:26:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 19 May 2026 23:26:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 May 2026 23:26:17 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 19 May 2026 23:26:17 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 May 2026 23:26:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 19 May 2026 23:26:18 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 19 May 2026 23:26:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 May 2026 23:26:18 GMT
STOPSIGNAL SIGINT
# Tue, 19 May 2026 23:26:18 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 19 May 2026 23:26:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c27750324068a115fb3e57c35c95ffcc6cc213dac9a5cc902d3244254a3641f`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a71830b82cdb6f13182d576f6cec9aa227e99062fba34ff44fe62c05969a0a`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 5.0 MB (4966077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8609894eb983f3a4cc25a033599a066e9072ece2abef00dd2843702cdc1d15`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 1.2 MB (1218640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf02ff3c9ae3ab2750d85716b94281d6a30f51bdd0a5963ac1a9404937892f2`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 8.1 MB (8066431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e54aa704967cf3e8d2740fff0de3dc1f1533ed9ae6058cf4fb58b80420e3988`  
		Last Modified: Tue, 19 May 2026 23:26:39 GMT  
		Size: 1.1 MB (1137479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43240f0b9ea031748d4e967d0c864a7b4324a1bf790dc31c2b5bea9b1c2a4791`  
		Last Modified: Tue, 19 May 2026 23:26:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcc221c26ffca161eb33a5ddc0b1c48d8854869529ef5eedbed421ee147e878`  
		Last Modified: Tue, 19 May 2026 23:26:39 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52117792ae19908a2fe93b8f9631107b56b16b5671a30ee6eb83b8849cfa7f99`  
		Last Modified: Tue, 19 May 2026 23:26:42 GMT  
		Size: 116.0 MB (115970086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76390b631ae6cf47420d04c43d3e4cb89d7303a4069de5b03c5a341071a6cb4`  
		Last Modified: Tue, 19 May 2026 23:26:40 GMT  
		Size: 9.5 KB (9530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d24784d07dc9dbf37e6406af5d7b7ea68ca96d4d12a31e400c2f9851cfc8f1a`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617468633c2e7e5291bf85ce2d1191df9e1b39c3a1313c1d07d144f2797d3094`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99366b1f9a8acc3af9e6ffc570d514f83312b218177982e648b2977373ee2738`  
		Last Modified: Tue, 19 May 2026 23:26:42 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfccddb8e54d8d552b98fb8f40c8f575955a6460be07b6b63c468be5753089d`  
		Last Modified: Tue, 19 May 2026 23:26:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:1c0d9f759516d8255c26379d6d75927c3b09ca62b8fc2d6f6171a8dccf532e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5861515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6e00ff59107bb5f20546fe18e132f4c67fae859b52a769422a37f69108e288`

```dockerfile
```

-	Layers:
	-	`sha256:c0ab7c97bd314db5b37ad5ab2fb8167940efcc7846abb47433be027295aef759`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 5.8 MB (5808263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb76b5c5936712308b20fde0e7a00b6b75b24c325218231e46d76cfa7e5bf63d`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
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
$ docker pull postgres@sha256:6e0a2603f73574c037c6263a9d764c65119fa378185037fded4f75ed579a5a1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164601744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6098be6a16cce60292910de995038f435386691489ea0b3ad57f4b354eff72b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:54:56 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Wed, 20 May 2026 00:55:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:55:19 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 00:55:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 00:55:28 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Wed, 20 May 2026 00:55:28 GMT
ENV LANG=en_US.utf8
# Wed, 20 May 2026 00:55:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:55:35 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 00:55:36 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 20 May 2026 00:55:36 GMT
ENV PG_MAJOR=14
# Wed, 20 May 2026 00:55:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Wed, 20 May 2026 00:55:36 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Wed, 20 May 2026 01:02:12 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 01:02:12 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 01:02:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 01:02:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 01:02:13 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 01:02:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 01:02:14 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 01:02:14 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 01:02:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 01:02:14 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 01:02:14 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 01:02:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce87ef6f1a5847b278239303e6b089da44d7a69824f6cfe040383cad9c3992c2`  
		Last Modified: Wed, 20 May 2026 00:56:52 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdae2aab66573294d2fcc04d501289426669ccb0bc353022e4c72da06d162241`  
		Last Modified: Wed, 20 May 2026 00:56:53 GMT  
		Size: 5.4 MB (5368572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a553d4b217c22cbbc8a14b1d6c1654c49bdbb2d010c2e36a1c5bb9113dfb5f89`  
		Last Modified: Wed, 20 May 2026 00:56:52 GMT  
		Size: 1.2 MB (1208168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654c472e3936e298a8ba1664efdb8192df3c9d1e9f791c763838c95a24d3dfcd`  
		Last Modified: Wed, 20 May 2026 00:56:53 GMT  
		Size: 8.1 MB (8066498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e8ae067614dbf4c9e50c65a6c1225017e3a70dc00692e6dc3e95d8726e8a0d`  
		Last Modified: Wed, 20 May 2026 00:56:53 GMT  
		Size: 1.3 MB (1283632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f019cff237b5fde7d065a46017e8f8b30a1c7407dd67f08c0edfe29445fe14d`  
		Last Modified: Wed, 20 May 2026 00:56:54 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5523beddb72fec062b4eb265a14bb9530bb2acc7e5ec344037c613e1ab3b15`  
		Last Modified: Wed, 20 May 2026 00:56:54 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3690ffa413caa27c28a5dfd91acc31a27224703f9432cc5028fab419ecf793b`  
		Last Modified: Wed, 20 May 2026 01:02:58 GMT  
		Size: 116.6 MB (116578594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ffe9e6d42963e6a17e4d6cac1f1cdd8ed7b7c646b2f9c4f3f74706f24311d7`  
		Last Modified: Wed, 20 May 2026 01:02:55 GMT  
		Size: 9.5 KB (9537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4fe17b1c363e2b4bc9b6a2b19640cc8dea2dbc667574e86be6bfde5d09fa46`  
		Last Modified: Wed, 20 May 2026 01:02:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d9a70094dbbfb26fe89efb8a76bc70b4ce20cefcb7b6ca7f761b1980cc6d8`  
		Last Modified: Wed, 20 May 2026 01:02:55 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf4ae36444d890e3c23a3142fafb442eb9f80c0ea1ec333a8588ddf8280388f`  
		Last Modified: Wed, 20 May 2026 01:02:56 GMT  
		Size: 6.1 KB (6097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f51f06bc663fd8de9d142101a579b1d2ec9bb0413797be2f675e3b6080f939`  
		Last Modified: Wed, 20 May 2026 01:02:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:ab6196bbacd68d4486c52451a8f5c979f2d184b0bcb2f4275ef1e18248820deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5855006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56464d850972e4d15f02df3acec0999b6a3321d3a69e41e8fad8893c4fd3e1d`

```dockerfile
```

-	Layers:
	-	`sha256:f0f1356045e4ba379ac4773e7cd83c57956545795930ef5f37a06540fb586448`  
		Last Modified: Wed, 20 May 2026 01:02:55 GMT  
		Size: 5.8 MB (5801656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ba996c415374c94ad8f9939491971ddb54a56aef21a523834fc8351779320b`  
		Last Modified: Wed, 20 May 2026 01:02:54 GMT  
		Size: 53.4 KB (53350 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:943cb178ca4bab8985053271bbe39cf3598111f32ff4bc57f283b06fe7dc785f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161062440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6284ede4b632196b5a55d44e957b4ab4a4c4688c6a6583fdab0d8431bc34f87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:41:28 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 19 May 2026 23:41:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:41:39 GMT
ENV GOSU_VERSION=1.19
# Tue, 19 May 2026 23:41:39 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 May 2026 23:41:45 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 19 May 2026 23:41:45 GMT
ENV LANG=en_US.utf8
# Tue, 19 May 2026 23:41:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:41:48 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 May 2026 23:41:49 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:41:49 GMT
ENV PG_MAJOR=14
# Tue, 19 May 2026 23:41:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/14/bin
# Tue, 19 May 2026 23:41:49 GMT
ENV PG_VERSION=14.23-1.pgdg12+1
# Wed, 20 May 2026 00:22:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Wed, 20 May 2026 00:22:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Wed, 20 May 2026 00:22:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Wed, 20 May 2026 00:22:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 20 May 2026 00:22:06 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Wed, 20 May 2026 00:22:06 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 20 May 2026 00:22:06 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 00:22:06 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Wed, 20 May 2026 00:22:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 00:22:06 GMT
STOPSIGNAL SIGINT
# Wed, 20 May 2026 00:22:06 GMT
EXPOSE map[5432/tcp:{}]
# Wed, 20 May 2026 00:22:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7eedde2b577281f658b3914aa8430ec2a2c2dcc2e5a23c3339e89d756c1b31`  
		Last Modified: Tue, 19 May 2026 23:55:43 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b55af12d70d802bbfe6246c103b1dcdd487b0d81884b14fae2e1e7edafe020`  
		Last Modified: Tue, 19 May 2026 23:55:43 GMT  
		Size: 4.4 MB (4391167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc53f60120b62eb59a960bc6e46b7556b9ac81f943dc8a0a90fdb705aed35ed`  
		Last Modified: Tue, 19 May 2026 23:55:43 GMT  
		Size: 1.2 MB (1222802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ddc4a4b1118cb9941b0182e034483a0c434b40ac1c59b3357d8031c252cac5`  
		Last Modified: Tue, 19 May 2026 23:55:43 GMT  
		Size: 8.1 MB (8120764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0701081c2db9bf86a079226689b199c06b35e1d84751ac8bd5154ce0a2c5035f`  
		Last Modified: Tue, 19 May 2026 23:55:44 GMT  
		Size: 1.1 MB (1097079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e58d2ed738e9405b007353cdc46efa6bc900f0a7c45e56165c552005c1d863`  
		Last Modified: Tue, 19 May 2026 23:55:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190eb41e80eceff92536dabdf17170cc03e061b00d23c6011d058086a530599f`  
		Last Modified: Tue, 19 May 2026 23:55:44 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945509107fe8657278c9f0ba9dc362cd306dc8e895ccc8fc63e136ec3341af12`  
		Last Modified: Wed, 20 May 2026 00:22:40 GMT  
		Size: 119.3 MB (119321492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a183370b8b14af468a9eae89a1df1efb53912ff51e84324c01feefc016a8cb6`  
		Last Modified: Wed, 20 May 2026 00:22:37 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d311cfad00bda8467ef9cbdfc227444715886e26fbd203d7e21ef2c1278294de`  
		Last Modified: Wed, 20 May 2026 00:22:37 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5acd12b9c92e05485d78107c98c9412912c977b807c9f3d5f350d41fbef78639`  
		Last Modified: Wed, 20 May 2026 00:22:37 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8716bfddc5d32ced2c570ce514956fd0cf9c51ea78f60a6b0381f75c02a0658e`  
		Last Modified: Wed, 20 May 2026 00:22:38 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f34f65dbd4dbe40f5db88979cc784be7da0fd20b68c11bd1543e9b34480984b`  
		Last Modified: Wed, 20 May 2026 00:22:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:6d9c2138e89da3db95ca8d32bf52e2b536386dd85e975ecd7019668ea8b9b89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5858035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec66d5b02d0011aebaef98db9293918c486be568809a991cc78dd630af99157`

```dockerfile
```

-	Layers:
	-	`sha256:40ef3b13209702e39d56e83194e789a30238ae9f8fada307205136a7ed696aef`  
		Last Modified: Wed, 20 May 2026 00:22:38 GMT  
		Size: 5.8 MB (5804739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5898b0c026abcac67d7969fd0292f669df8d55d1db836390a5ef950e5c885183`  
		Last Modified: Wed, 20 May 2026 00:22:37 GMT  
		Size: 53.3 KB (53296 bytes)  
		MIME: application/vnd.in-toto+json
