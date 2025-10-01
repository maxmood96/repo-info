## `postgres:13-bookworm`

```console
$ docker pull postgres@sha256:e3411523d6b9c0a146f1a845098269124f6ea1bef4e56ac2509b34d463f8fcc6
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

### `postgres:13-bookworm` - linux; amd64

```console
$ docker pull postgres@sha256:b939274cd4e6730f6febfee0680e7d6258c248d72371fd2d6cd5985d881c905b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150746140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fd7a815125a13efe02f8e233097316c17008515e1ced9446aabd673e0914ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Sep 2025 19:31:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64a9f8030f8adf48eca7e13ce878d25f4fe5988a6c14608f7a96514776e4aa8`  
		Last Modified: Tue, 30 Sep 2025 00:09:17 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238fee4ed1bdd31ef2e68b3d864c8793a119bae29e1b178ad00d7e232a54a7fc`  
		Last Modified: Tue, 30 Sep 2025 00:09:18 GMT  
		Size: 4.5 MB (4534073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26090e2498a4561318749d1f30dc86a742a957dbb23ce65e84d2a8595769beeb`  
		Last Modified: Tue, 30 Sep 2025 00:09:17 GMT  
		Size: 1.2 MB (1249522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2153858a522e3054bc6fc6c8aec36f55c70dc0838707ae00aefc4c690071c23`  
		Last Modified: Tue, 30 Sep 2025 00:09:18 GMT  
		Size: 8.1 MB (8066506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656725cefbc5be1f8ad8fe1aa09f1cc06f4cc57deaba4a85783fc5cc58710856`  
		Last Modified: Tue, 30 Sep 2025 00:09:17 GMT  
		Size: 1.2 MB (1196403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a084b9cfa16a0b44ceec30097121175aad80e82a6db40b7616eedd9e1fe36056`  
		Last Modified: Tue, 30 Sep 2025 00:09:17 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c687abc90f0dd1fc6a91406b7754d77e011e91c02d1d7c6d9cbab0539887987`  
		Last Modified: Tue, 30 Sep 2025 00:09:17 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568e40a879ef5e9ccef981458a40a1b7d0b9bd8e42131b1f648e0eeca8d0862`  
		Last Modified: Tue, 30 Sep 2025 00:09:26 GMT  
		Size: 107.5 MB (107451137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410986422423f813a4c1bb57daefbc8f0a82817591675d81aa54a427b5b617b3`  
		Last Modified: Tue, 30 Sep 2025 00:09:17 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da17b88110af77cf390a16445dab710cacf6a84fc1147660044e59901472dcc3`  
		Last Modified: Tue, 30 Sep 2025 00:09:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8859cc4e4e283a6697c5d713400a0f54d536b8b44072bd5ce76aa1a8f08afc73`  
		Last Modified: Tue, 30 Sep 2025 00:09:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f26d009c5fbf89e4272feea9ac82abfe0626f8aab04e957ebfa982c700a641e`  
		Last Modified: Tue, 30 Sep 2025 00:09:18 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d07f56e43b5d701449fd9cc6109aba2681d82b971477827c3cf1d3e3ada3c5`  
		Last Modified: Tue, 30 Sep 2025 00:09:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:804a8fe0a01500da8ebda719fd947c599e3b31a47ded5a06cce5f3be43e26604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5806612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9805c77f88789a6a77f3461aff3b2dee598bf3bad8a296f6da9a7bf1710e0f45`

```dockerfile
```

-	Layers:
	-	`sha256:a7ff9112f9970437933ecbeff6e6c625791170aab238dfbfbcc6edcf5026f2da`  
		Last Modified: Tue, 30 Sep 2025 02:07:36 GMT  
		Size: 5.8 MB (5752889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:276d2f1e28c6ac7cde84ca7c7275c522312362f1a695ecbc344de1eb76bf9ef5`  
		Last Modified: Tue, 30 Sep 2025 02:07:37 GMT  
		Size: 53.7 KB (53723 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; arm variant v5

```console
$ docker pull postgres@sha256:c8d3fa4b7f3f6c44b1df3fcb6f186336ef204c6c6d8d09153ebd7a3bf081d99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143661205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3271cab72f0862163df55a7c66159f85ed5680c2986d0700e177436d42bf53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Sep 2025 19:31:05 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e1e8cf6a98b379fbf689c13a9736cd1289212f7d1817f7bef04f737d92c4359f`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 25.8 MB (25757437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc133a7ef810f347383721f94bb0255059227bcc6a71d9be294d71c30c270c3`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555fc2ede5ba805c84f0aa2a689cc7da1060bb8703c46076256fecbe765d361`  
		Last Modified: Tue, 30 Sep 2025 00:59:37 GMT  
		Size: 4.2 MB (4151177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2cc58b320cc877790db01affdd7e61bed042597bd19d0bf89612fe091b04e`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 1.2 MB (1220048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ba166533461722b988b6a7d9be1c9392369359769ada15d7440638e5b83688`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 8.1 MB (8066612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c85b0c42dc3a3a96ad157adf6997867074d3efeed7e58e9ac3546288bf8961`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 1.2 MB (1195018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1948adefe1e5d7c99b04cac32d273b612bb75e273721aed61b02a9e3edf3d0`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f7d6c5246765594119b23bea5b0937cb0bf349a91954c3c6e3e84fb3a4ca4e`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5be7f2aefec7c9ea94c2ae0499dfdcc1fff2b056fc49f338bfd90214b7303f1`  
		Last Modified: Tue, 30 Sep 2025 00:59:41 GMT  
		Size: 103.3 MB (103250731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c21ebdfc6ea11b43c1556d32f46e8dcaa4d23d89c84b49ef15ae1aee085a86b`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3447f927314fc160525f59b322d4e0ba95f5687647d5455b501a4fbb936b77e3`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22669ae0cc26555310e3c2440ea9328dd174c11411e7837f1d432f144e2f2b6`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a793b819f772734849077f356181475837e5e9d7540b8f8963bf11bf2f3e97c3`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 5.9 KB (5926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e34e89d37ee5b12e3ec50c6a3dee5b3ea318c5bc5126641ce28d8a4576629a`  
		Last Modified: Tue, 30 Sep 2025 00:59:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2669fe0e1a621f2217f0ca8105469028f7198aca333d36516e3abe8597c6df08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5822645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e065401134e7916c672b42adeb058cf66a3e8d6d80f9fb55a46e7687342f9310`

```dockerfile
```

-	Layers:
	-	`sha256:d1cb5f3288033d459231efd4a70baa2843913893ee8be63e65ec8c46c78c6671`  
		Last Modified: Tue, 30 Sep 2025 08:07:35 GMT  
		Size: 5.8 MB (5768714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f011abac9f5c9643f36456edd06b52d2bac6b8d10cfa63a34501f2e3cca02d22`  
		Last Modified: Tue, 30 Sep 2025 08:07:36 GMT  
		Size: 53.9 KB (53931 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; arm variant v7

```console
$ docker pull postgres@sha256:59085ca8f270539b75941c2382caeede64e46159d83cd7002edf01a415e53839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138810896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2f7f3499a98484f7640999199ade78f9a8a27403be8710fee64748c541a49c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Sep 2025 19:31:05 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4c0d784fb90dddd991d201014e92ef1ebfe9a20d0f2ea56e2701fb9e8219be91`  
		Last Modified: Mon, 29 Sep 2025 23:34:19 GMT  
		Size: 23.9 MB (23933930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c6233b7cfd0964c1cedff64fbd0aeed788d6e21c29e1fb679d708173f64ef2`  
		Last Modified: Tue, 30 Sep 2025 00:40:04 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fd3dedbacf9c234dfc80ec39c17a8fd230a1890033049ae6cde30d61cbf974`  
		Last Modified: Tue, 30 Sep 2025 00:40:04 GMT  
		Size: 3.7 MB (3742639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb0a60a49b8a90474298a14f64cede5abec410ec08cd75a85c98dd1ad9ec654`  
		Last Modified: Tue, 30 Sep 2025 00:40:01 GMT  
		Size: 1.2 MB (1215993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b81333f799af6d9f977d6e1d4f25d75ae2cf9c89ed1cb76aaf25cedf55d456`  
		Last Modified: Tue, 30 Sep 2025 00:40:06 GMT  
		Size: 8.1 MB (8066475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41986645fa3d50e48504710c900289b5f794a6d0b01488649a64c8be670384e4`  
		Last Modified: Tue, 30 Sep 2025 00:40:01 GMT  
		Size: 1.1 MB (1067240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceea90045973d57512c56fb2f1e8a3f2b55482eb094ee29c44967eae5c5b4b6b`  
		Last Modified: Tue, 30 Sep 2025 00:40:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda43623811b2e4234fe63c997c791bd5dc49077aafb92fcb68d01919f5bccfa`  
		Last Modified: Tue, 30 Sep 2025 00:40:02 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bedac767bda735e74f5c5c9357022c9bcc9c64ebaa21be956768c652ffc1bb3`  
		Last Modified: Tue, 30 Sep 2025 01:10:43 GMT  
		Size: 100.8 MB (100764438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30530eb63948c579899ad466f7ca3b24822cbcf075570744f7c62d412f742c83`  
		Last Modified: Tue, 30 Sep 2025 01:10:33 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7405fdc6bff1e3459aa80373cd895bb857e9fd453e8fafe9d4ac79e4d69edb`  
		Last Modified: Tue, 30 Sep 2025 01:10:33 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c8369d99dc635cf9a927e54fb189e059f0e58426ce3744a619e2aff7ca64f9`  
		Last Modified: Tue, 30 Sep 2025 01:10:33 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efba58dfdbef9556ba3a3bebbdf8fe0dc919b40d7bb4fe23083460767d663972`  
		Last Modified: Tue, 30 Sep 2025 01:10:33 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd51b54949583186f201fd960d67c21877a4962a7f4ecb1c76ca588d6d4e41d`  
		Last Modified: Tue, 30 Sep 2025 01:10:33 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:b7186384145c5d46aa2e623863ef11b8e5c7427edc1ac6bf30166bf5de108631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5821900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd7787ab3eafa75d15391562157bf3a4a14f06de9849e27ea2d43980b075bed`

```dockerfile
```

-	Layers:
	-	`sha256:b81d22bad2bfcf5cb5139ee9c342bd26967da7a6d3bab4004840fb4e2a430cf8`  
		Last Modified: Wed, 01 Oct 2025 20:08:37 GMT  
		Size: 5.8 MB (5767969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5da491a7dc8659d0bfe421e57b7a558b1de1bb4601bd5a94b53f1f35f53b05f1`  
		Last Modified: Wed, 01 Oct 2025 20:08:38 GMT  
		Size: 53.9 KB (53931 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:32ef355593e600e5b0acbb81cb714984747413fce8d6047e1efed3c804ae2d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148731012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ae876da80a355b1a83db37944fb27e8f95a934a5a365198db33b207114e693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Sep 2025 19:31:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e7dc6ad9bee08a8609bf47a1f5804f07b15d270d81eecad02fcf5ac09dfe93`  
		Last Modified: Tue, 30 Sep 2025 00:12:33 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b6662d0132a123d73c3b199bfe81496907dc788be6b7cdb306a9425b070355`  
		Last Modified: Tue, 30 Sep 2025 00:12:34 GMT  
		Size: 4.5 MB (4519803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e40e7f1a6551c20b9b11c38c5c48fda0db3edac4228a65f0d0359722414433`  
		Last Modified: Tue, 30 Sep 2025 00:12:34 GMT  
		Size: 1.2 MB (1203238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4258e16f03b770d7cdc18713e73a0006a114a56cc9ccce291563baa1f2cbd4`  
		Last Modified: Tue, 30 Sep 2025 00:11:57 GMT  
		Size: 8.1 MB (8066509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee888aaeb3d8014261b314767733f1ef5ed8d7cb841a34b32ac9048793d85ee`  
		Last Modified: Tue, 30 Sep 2025 01:05:16 GMT  
		Size: 1.1 MB (1108939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d6816dd41efa4a8515e6bfbbeeefe7b7aeeded0bb57821874d91cd2104a24a`  
		Last Modified: Tue, 30 Sep 2025 01:05:15 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a893f7ea70e38a5b881c9e0a2c95ce0f3d985734b4c9458c57a718db73eab14b`  
		Last Modified: Tue, 30 Sep 2025 01:05:15 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699ec3d73b20ca4a38d54454bd0249d7f474c224e98876bc110c6029b885db25`  
		Last Modified: Tue, 30 Sep 2025 00:12:02 GMT  
		Size: 105.7 MB (105710208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2d681ba635eee38bbb8f4625436c57af8409fc935d52d36726b92a32d482a8`  
		Last Modified: Tue, 30 Sep 2025 01:05:15 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d2de937e849424513be0e83ae472a427944a672c7a66ce5295ddce645a716e`  
		Last Modified: Tue, 30 Sep 2025 01:05:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa3410461b1122b18533d544ade34ba4b04d497290468496721b302d2869670`  
		Last Modified: Tue, 30 Sep 2025 01:05:15 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99656360adec4dccfe2881b0e9cffd7532f0a7ee1339af84d7f10feb8e6e08f7`  
		Last Modified: Tue, 30 Sep 2025 01:05:16 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9be3dcf27d3ec5209a6739361b11fa628dc6d4ca999cde797b6f21b56ba102`  
		Last Modified: Tue, 30 Sep 2025 01:05:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:2b4e6a8d79deb0d72f7dfd28d3d8ba238a34e4d54fa78a6d20713fe3144b11fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5813169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc016f442b2f419ded85df9450ceb86cb7c84f99a070d14c3d5f7b34f2148b3`

```dockerfile
```

-	Layers:
	-	`sha256:97d3d81c39f23759ce26599221f1d7cd9984cf5c5c9cbfb40bb4ced55a9151b9`  
		Last Modified: Wed, 01 Oct 2025 20:08:43 GMT  
		Size: 5.8 MB (5759200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723905078a47ae4b69aea69aed5fd353dbdd24a09e7b779968901fbfa023840a`  
		Last Modified: Wed, 01 Oct 2025 20:08:43 GMT  
		Size: 54.0 KB (53969 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; 386

```console
$ docker pull postgres@sha256:bdf272d32030e3492d8d80531f46f41bca56330531580e16baeb9b5c650a5b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159552796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa0ea1744a5aa70a71fb11adf3f901dcb710d6736df8100bd3907e8b5948f39`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc85206f42611fb95fc01e8e93ab79245bf8ea168099193d9691b1564743aa6`  
		Last Modified: Tue, 23 Sep 2025 21:35:21 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fa256524feb94dc844cbe046acf947432e26344a9e0048444319a45dac7871`  
		Last Modified: Tue, 23 Sep 2025 21:35:24 GMT  
		Size: 5.0 MB (4965277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03771d85a56e5f276bfc87fc559d294c7226c6d89611ee993b319001439e57bb`  
		Last Modified: Tue, 23 Sep 2025 21:35:24 GMT  
		Size: 1.2 MB (1218587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd60f36b6ac9bde1ab469ebb41c443ba9613dfe446839ea6c7bbe12d95ff40a6`  
		Last Modified: Tue, 23 Sep 2025 21:35:27 GMT  
		Size: 8.1 MB (8066458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e6d7395e9ada9155e4755081f7cd0fb2fa7b5214383e91b64b561b9f7fd6b6`  
		Last Modified: Tue, 23 Sep 2025 21:35:27 GMT  
		Size: 1.1 MB (1137378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1d3e29e88794234f53dedd689f297dec909cdf8b92af304209497415241078`  
		Last Modified: Tue, 23 Sep 2025 21:35:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516c23b60a79e631a36c87fd53f30a5c1c63b1df8f64f383fb355c5cd8424a28`  
		Last Modified: Tue, 23 Sep 2025 21:35:15 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caff5ae45cca7a4c64ffb34521410ab77422b465263f0485df8d132556cc2b8`  
		Last Modified: Tue, 23 Sep 2025 21:45:09 GMT  
		Size: 114.9 MB (114935273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb93e9706f96ad6f593a2d7d74983cf8c08af36a5e20e223c0a6880aef44b82c`  
		Last Modified: Tue, 23 Sep 2025 21:45:00 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eef15c38386880e4cd7ba05c88843287958cc398d07145043b3733be1ed8ae`  
		Last Modified: Tue, 23 Sep 2025 21:45:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfe0be68f6670914b91e4807f8e23079f1aa55a3f8bf3c6cfa3b961984cfae3`  
		Last Modified: Tue, 23 Sep 2025 21:45:01 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc1f14802906fbc7406883d1cca0d36020f80d8409acb0a18d88d58fd33956d`  
		Last Modified: Tue, 23 Sep 2025 21:45:01 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6415b7002e9c95231212687d6f4c080d03803b2211003ce3c8b4ef2a755f0`  
		Last Modified: Tue, 23 Sep 2025 21:45:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:834c5c68cc466faaf901ed36f4976f95ae4ac9655df0909d86d3a0bb12feb9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5902798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03079c57aa57c29646b66d9898cfbab926ddf58c7a18091eb3646fd1eaf9e561`

```dockerfile
```

-	Layers:
	-	`sha256:c3b1147dce3f56c0a979e23db7201bed30453a2c4723bf23182745e47c19cfc2`  
		Last Modified: Tue, 23 Sep 2025 23:08:53 GMT  
		Size: 5.8 MB (5849118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92cae9faf579d545e2f3948057893bfd514c65a44764f28ac4c5849d9388d4bf`  
		Last Modified: Tue, 23 Sep 2025 23:08:55 GMT  
		Size: 53.7 KB (53680 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; mips64le

```console
$ docker pull postgres@sha256:3490dcb1c29deefdd7623c5f86c191f40442e3b7247010af2e3190214db62ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149565063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ae39863ef5aea4427574133b3fa257801b286814b32113166389f830e45f7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Sep 2025 19:31:05 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:73d0a1261a90ced7c792643cb457a2c9f7bbeca1bcb84939b4029c5a1f01f26c`  
		Last Modified: Mon, 29 Sep 2025 23:34:06 GMT  
		Size: 28.5 MB (28513676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d10de371f209c727ac7bb012b4d1ae77293dd115df15e46d99c8906685f7bc`  
		Last Modified: Tue, 30 Sep 2025 07:49:40 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51dc08b8fefc299e23f62291a740a6503e8024a47aec51f1c8188254e5aebc3`  
		Last Modified: Tue, 30 Sep 2025 07:49:40 GMT  
		Size: 4.5 MB (4475423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8925e9737c6a53c1079fbe25aeb57d7cc0d67494dd0b106a4ede817d7e356ed9`  
		Last Modified: Tue, 30 Sep 2025 07:49:41 GMT  
		Size: 1.2 MB (1159164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b0b86761fa1b99021362bcff00b5a29604b076cd885305b8255cca752933dc`  
		Last Modified: Tue, 30 Sep 2025 07:49:44 GMT  
		Size: 8.1 MB (8066690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed61a062b9af0ebd72d636f120d6e1c03bc3985a4305e169304de63b52725741`  
		Last Modified: Tue, 30 Sep 2025 07:49:41 GMT  
		Size: 1.2 MB (1182915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e467bb51148e774913eedeeed34d1fd03c9b290a8256fb6d468c0c109a1dc749`  
		Last Modified: Tue, 30 Sep 2025 07:49:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2422393ffddacc15070620014939ddee7917b45ab02de9469126b47eb5169ce`  
		Last Modified: Tue, 30 Sep 2025 07:49:41 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8c2099198586d185b194ebc34411a5f6d2f097fa61ebd7a92cc533f6f5f34a`  
		Last Modified: Tue, 30 Sep 2025 13:26:29 GMT  
		Size: 106.1 MB (106147011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b4fa9a9bc34302e93799f96f52560213fbc11347056cd77b3c42c4235b8486`  
		Last Modified: Tue, 30 Sep 2025 13:26:07 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f69bea3f54f6b68af1d481230b3b7e78f3af239be16f1bce7a4c4e185488ef`  
		Last Modified: Tue, 30 Sep 2025 13:26:06 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74d6b694119f2d0cb9332cb809b84f5fffff47d53deecc3f014ab1f265e6821`  
		Last Modified: Tue, 30 Sep 2025 13:26:07 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749fb79ab0e4f31f91b5a9e5129e165afdc5c904065d51188ca085139e4efa2d`  
		Last Modified: Tue, 30 Sep 2025 13:26:08 GMT  
		Size: 5.9 KB (5929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cf1add0d2a93b1b919475b5597ef040e225cea6d636adca77de2d07bba9beb`  
		Last Modified: Tue, 30 Sep 2025 13:26:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:3f7d54635661f76476d3dad9cf548ff1e6c575353f796eab78707ac9ab51c48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 KB (53590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf97a25f2070a335c289ff4ccaa7877fb6aaebac9b0f62bf29a69998441c7f2f`

```dockerfile
```

-	Layers:
	-	`sha256:2faff107076e2f2b3c0bfbcb3ff8955b11eaa675caf1e0326f92fb03b1477f6c`  
		Last Modified: Tue, 30 Sep 2025 20:14:27 GMT  
		Size: 53.6 KB (53590 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; ppc64le

```console
$ docker pull postgres@sha256:1bdc583291c917f56ed3feb0026b6187c1e3709d679cb9a3407bd9152865960c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163295303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2783f0566ea1c68ed8f2de99f6e42dcb31b78bff7b7ea42a91559f1cce02f36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Sep 2025 19:31:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b34e22ac0a8b42eb22eafbdd5e9ef44021aa9cd038797e21159ecd39f62ca2`  
		Last Modified: Tue, 30 Sep 2025 01:50:14 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438cc51fcb7698854b75c55e213dd7c754603b5aa15056df39c271e555eef637`  
		Last Modified: Tue, 30 Sep 2025 01:50:15 GMT  
		Size: 5.4 MB (5368501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1098c2fe99169d7503137a4d4eed2222cca76089d19e950df81b799a3382cf0`  
		Last Modified: Tue, 30 Sep 2025 01:50:15 GMT  
		Size: 1.2 MB (1208255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:387229d007cf7cee4a9bb80422ffa80ad66bb3a11100a84a65c5784338da6d76`  
		Last Modified: Tue, 30 Sep 2025 01:50:16 GMT  
		Size: 8.1 MB (8066638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053a523ac38cb67fe0c4d13c2b98085a3bee3c6a084a1f0b1d2d524facfdb684`  
		Last Modified: Tue, 30 Sep 2025 01:50:16 GMT  
		Size: 1.3 MB (1283674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d91a3cbde68406e87007653fb55f7978dcab3c9556d371dc32e73144a0d0147`  
		Last Modified: Tue, 30 Sep 2025 01:50:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69849b33835cc7713ae86fdf120d96bdbdb3e3539e44ac31d406089d66048ed`  
		Last Modified: Tue, 30 Sep 2025 01:50:16 GMT  
		Size: 3.1 KB (3138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173cd29b888ee48144e15651a4abb1215c96b7fe7b5bfb689c5fc6a4b927225`  
		Last Modified: Tue, 30 Sep 2025 02:00:26 GMT  
		Size: 115.3 MB (115279365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f71b4ba7738b0848a122a4458ed55fda3619c5d1fd34f9f24a782a45ee3719`  
		Last Modified: Tue, 30 Sep 2025 02:00:21 GMT  
		Size: 9.4 KB (9353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caad21638a837d42918a362533781503736efbdfdcf7586a937b8fd7fe52fef2`  
		Last Modified: Tue, 30 Sep 2025 02:00:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13495ea93a08aa40d7a189c3409fe409b0c39c80c38113449ff919ccd2a0a17`  
		Last Modified: Tue, 30 Sep 2025 02:00:21 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5a5ff9e91b4c5e6ca3f3f014714c0a46e04c4e2c4ad68c83e1cc2aeb2ad43c`  
		Last Modified: Tue, 30 Sep 2025 02:00:21 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d06e73628a8ccaf908404f627602ab98a0766b85975fa1dfcf683be59e78d8`  
		Last Modified: Tue, 30 Sep 2025 02:00:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:82ec0cb41ea9c44dcd95c41d9004902c563a8135994b2193921ab6987c3dae18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5814028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14bc57a4d02bcdb56c31eb7dd7f0a5919302b7aa7c3169631f0e6a5ec1d5ad1`

```dockerfile
```

-	Layers:
	-	`sha256:67440caec07c47b0c376827ad9326b5255891cf358d93de338c7997b0e1c6a47`  
		Last Modified: Wed, 01 Oct 2025 20:08:54 GMT  
		Size: 5.8 MB (5760250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0607a50552c6ebbe825b9720da6d74eeb25f9a14997532309351dd9ba19002a`  
		Last Modified: Wed, 01 Oct 2025 20:08:55 GMT  
		Size: 53.8 KB (53778 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-bookworm` - linux; s390x

```console
$ docker pull postgres@sha256:2a839ce047f8acb0c903d7b020c4a6e09a6d9f425589e59d4a5f2d7c31dacfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159852006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f549a8f89bdcf7198b921f43f8b15d65cda2b8419a62b32368ded16d417073`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 23 Sep 2025 19:31:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	groupadd -r postgres --gid=999; 	useradd -r -g postgres --uid=999 --home-dir=/var/lib/postgresql --shell=/bin/bash postgres; 	install --verbose --directory --owner postgres --group postgres --mode 1777 /var/lib/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		less 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	if [ -f /etc/dpkg/dpkg.cfg.d/docker ]; then 		grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 		sed -ri '/\/usr\/share\/locale/d' /etc/dpkg/dpkg.cfg.d/docker; 		! grep -q '/usr/share/locale' /etc/dpkg/dpkg.cfg.d/docker; 	fi; 	apt-get update; apt-get install -y --no-install-recommends locales; rm -rf /var/lib/apt/lists/*; 	echo 'en_US.UTF-8 UTF-8' >> /etc/locale.gen; 	locale-gen; 	locale -a | grep 'en_US.utf8' # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV LANG=en_US.utf8
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libnss-wrapper 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 	key='B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8'; 	export GNUPGHOME="$(mktemp -d)"; 	mkdir -p /usr/local/share/keyrings/; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /usr/local/share/keyrings/postgres.gpg.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_MAJOR=13
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/postgresql/13/bin
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PG_VERSION=13.22-1.pgdg12+1
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -ex; 		export PYTHONDONTWRITEBYTECODE=1; 		dpkgArch="$(dpkg --print-architecture)"; 	aptRepo="[ signed-by=/usr/local/share/keyrings/postgres.gpg.asc ] http://apt.postgresql.org/pub/repos/apt bookworm-pgdg main $PG_MAJOR"; 	case "$dpkgArch" in 		amd64 | arm64 | ppc64el) 			echo "deb $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 			apt-get update; 			;; 		*) 			echo "deb-src $aptRepo" > /etc/apt/sources.list.d/pgdg.list; 						savedAptMark="$(apt-mark showmanual)"; 						tempDir="$(mktemp -d)"; 			cd "$tempDir"; 						apt-get update; 			apt-get install -y --no-install-recommends dpkg-dev; 			echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list; 			_update_repo() { 				dpkg-scanpackages . > Packages; 				apt-get -o Acquire::GzipIndexes=false update; 			}; 			_update_repo; 						nproc="$(nproc)"; 			export DEB_BUILD_OPTIONS="nocheck parallel=$nproc"; 			apt-get build-dep -y postgresql-common-dev; 			apt-get source --compile postgresql-common-dev; 			_update_repo; 			DEBIAN_FRONTEND=noninteractive 			apt-get build-dep -y "postgresql-$PG_MAJOR=$PG_VERSION"; 			apt-get source --compile "postgresql-$PG_MAJOR=$PG_VERSION"; 									apt-mark showmanual | xargs apt-mark auto > /dev/null; 			apt-mark manual $savedAptMark; 						ls -lAFh; 			_update_repo; 			grep '^Package: ' Packages; 			cd /; 			;; 	esac; 		apt-get install -y --no-install-recommends postgresql-common; 	sed -ri 's/#(create_main_cluster) .*$/\1 = false/' /etc/postgresql-common/createcluster.conf; 	apt-get install -y --no-install-recommends 		"postgresql-$PG_MAJOR=$PG_VERSION" 	; 		rm -rf /var/lib/apt/lists/*; 		if [ -n "$tempDir" ]; then 		apt-get purge -y --auto-remove; 		rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list; 	fi; 		find /usr -name '*.pyc' -type f -exec bash -c 'for pyc; do dpkg -S "$pyc" &> /dev/null || rm -vf "$pyc"; done' -- '{}' +; 		postgres --version # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN set -eux; 	dpkg-divert --add --rename --divert "/usr/share/postgresql/postgresql.conf.sample.dpkg" "/usr/share/postgresql/$PG_MAJOR/postgresql.conf.sample"; 	cp -v /usr/share/postgresql/postgresql.conf.sample.dpkg /usr/share/postgresql/postgresql.conf.sample; 	ln -sv ../postgresql.conf.sample "/usr/share/postgresql/$PG_MAJOR/"; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/share/postgresql/postgresql.conf.sample # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 3777 /var/run/postgresql # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 23 Sep 2025 19:31:05 GMT
RUN install --verbose --directory --owner postgres --group postgres --mode 1777 "$PGDATA" # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 23 Sep 2025 19:31:05 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Tue, 23 Sep 2025 19:31:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Sep 2025 19:31:05 GMT
STOPSIGNAL SIGINT
# Tue, 23 Sep 2025 19:31:05 GMT
EXPOSE map[5432/tcp:{}]
# Tue, 23 Sep 2025 19:31:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d48d314d4c4ad33b7f3f8a91af0de4fa9191497ad35b65135e22f849c79fa77`  
		Last Modified: Tue, 30 Sep 2025 01:43:08 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cb5cf9730db1f8d0432592e9a0487585578c243c8ff054591077265b20cd4a`  
		Last Modified: Tue, 30 Sep 2025 01:43:09 GMT  
		Size: 4.4 MB (4391259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e57ed66ef6a49004560c81c56ba2b027f0ad72448adfc8b3f5af5a1ee44bb6`  
		Last Modified: Tue, 30 Sep 2025 01:43:08 GMT  
		Size: 1.2 MB (1222771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eec6d347aebf4ee1aa4431a08de8e9841df88ad708ebf73e585f17cc918d063`  
		Last Modified: Tue, 30 Sep 2025 01:43:09 GMT  
		Size: 8.1 MB (8120694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00f9087bc347a60749002ae1cb46d8d3ea80bb9a074463d729761d05078feef`  
		Last Modified: Tue, 30 Sep 2025 01:43:08 GMT  
		Size: 1.1 MB (1097018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b8c872ec929275fa054b1dbf9fb365de67171baa61027cbb54b430a969045`  
		Last Modified: Tue, 30 Sep 2025 01:43:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a521c4a60db5584ce5b77818beb26a1c3f38ac85c51bbc911ab57d2c7af7c763`  
		Last Modified: Tue, 30 Sep 2025 01:43:13 GMT  
		Size: 3.1 KB (3139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e9e44d7f14c76e6e2d94f536c2e75e78b58b75e426cd40f3e482f7ae8fffd6`  
		Last Modified: Tue, 30 Sep 2025 02:51:18 GMT  
		Size: 118.1 MB (118115766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8f126e1157601e573e3d1387f8fbbfcae50241127de27e1a4b4da84019fba7`  
		Last Modified: Tue, 30 Sep 2025 02:51:13 GMT  
		Size: 9.4 KB (9351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a4a8d8d05c405bdd1dbe4b1b8c26a8d3fce41c442eb844bd05e28a0c4cfc5e`  
		Last Modified: Tue, 30 Sep 2025 02:51:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bf920187117b836f0f316bad23294f4db9c0a75f967cbdb561291dd564b482`  
		Last Modified: Tue, 30 Sep 2025 02:51:13 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb05af7a3163eef4a21d010e7dfb8604c3b9652d7e8269e234769d5057f9122`  
		Last Modified: Tue, 30 Sep 2025 02:51:13 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ab3eef97676eb519bf92d069dd58bc69122b6fb68957cb2bf78a1c1c0bc3f1`  
		Last Modified: Tue, 30 Sep 2025 02:51:13 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-bookworm` - unknown; unknown

```console
$ docker pull postgres@sha256:d151b9158488ee49f61b71541c1224da77626b8f6877cc6559cfcb3d89bb41fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5817057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ddbd1bf7472cbe529baba8126333b1a8f46394358268814755ad4adc0e19e8`

```dockerfile
```

-	Layers:
	-	`sha256:5934dc2c55667f88f2785b99455f2f90f1e93bfa206788d889f0ae3823bbb9bc`  
		Last Modified: Wed, 01 Oct 2025 20:09:00 GMT  
		Size: 5.8 MB (5763333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:103b09137837b1f7c2ca26ec938c6f9130a45cbdfd1d84dab9e816df03766040`  
		Last Modified: Wed, 01 Oct 2025 20:09:01 GMT  
		Size: 53.7 KB (53724 bytes)  
		MIME: application/vnd.in-toto+json
